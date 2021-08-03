# **High-level HTTP:**

- The HTTP Request Lifecycle:(1)

  - Local Processing
  - Resolve an IP
  - Establish a TCP Connection
  - Send an HTTP Request
  - Tearing Down and Cleaning Up

- User Datagram Protocol (UDP) is a lightweight protocol, but the tradeoff is that it offers no guarantees in terms of delivery, and there is no acknowledgement other than a response being sent and received.

- Transmission Control Protocol (TCP) ensures delivery and ordered data transmission.

- > TCP connections are opened using what’s known as a three-way handshake.(1)

- The request is made up of a request line, request header, and a body.(1)

# **Java HTTP Request example:**

- We perform HTTP requests in Java by using the built-in Java class **HttpUrlConnection**.

- Create a request:(2)

  ```java
  URL url = new URL("http://example.com");
  HttpURLConnection con = (HttpURLConnection) url.openConnection();
  con.setRequestMethod("GET"); // set request type it can be: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE

  //Adding Request Parameters
  Map<String, String> parameters = new HashMap<>();
  parameters.put("param1", "val");

  con.setDoOutput(true); // set to true so we can add parameters to a request
  DataOutputStream out = new DataOutputStream(con.getOutputStream());
  out.writeBytes(ParameterStringBuilder.getParamsString(parameters)); // transforms a Map into a String
  out.flush();
  out.close();

  // Setting Request Headers
  con.setRequestProperty("Content-Type", "application/json"); // add header
  String contentType = con.getHeaderField("Content-Type"); // read header value

  // Configuring Timeouts

  //These values define the interval of time to wait for the connection to the server to be established or data to be available for reading
  con.setConnectTimeout(5000); // 5 seconds
  con.setReadTimeout(5000);

  ```

## Sources:

- (1) [The HTTP Request Lifecycle](https://dev.to/dangolant/things-i-brushed-up-on-this-week-the-http-request-lifecycle-)

- (2) [Do a Simple HTTP Request in Java](https://www.baeldung.com/java-http-request)

[Back to home page](../README.md)
