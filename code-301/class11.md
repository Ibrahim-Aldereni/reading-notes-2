# **What is OAuth:**

- **What is OAuth?**

  OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential.(1)

- **Give an example of what using OAuth would look like.**

  Is when you go to log onto a website and then click on the button linked to the other website, the other website authenticates you.(1)

- **How does OAuth work? What are the steps that it takes to authenticate the user?**

  1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
  2. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
  3. The first site gives this token and secret to the initiating user’s client software.
  4. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
  5. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
  6. The user approves (or their software silently approves) a particular transaction type at the first website.
  7. The user is given an approved access token (notice it’s no longer a request token).
  8. The user gives the approved access token to the first website.
  9. The first website gives the access token to the second website as proof of authentication on behalf of the user.
  10. The second website lets the first website access their site on behalf of the user.
  11. The user sees a successfully completed transaction occurring.(1)

- **What is OpenID?**

  OpenID would serve as a single sign-in, vouching for the identities of users rather than having multiple logins for multiple websites.

# **Authorization and Authentication flows:**

- **What is the difference between authorization and authentication?**

  _authentication_ is the process of verifying who a user is, while _authorization_ is the process of verifying what they have access to.(2)

- **What is Authorization Code Flow?**

  exchanges an Authorization Code for a token

- **What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**

  The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier.(2)

- **What is Implicit Flow with Form Post?**

  It does offer a streamlined workflow if the application needs only an ID token to perform user authentication.(2)

- **What is Client Credentials Flow?**

  the system authenticates and authorizes the app rather than a user.(2)

- **What is Device Authorization Flow?**

  rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device.(2)

- **What is Resource Owner Password Flow?**

  requests that users provide credentials (username and password), typically using an interactive form.(2)

---

## Things I want to know more about:

## Sources:

- (1) [What is OAuth?](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)

- (2) [Authentication and Authorization Flows](https://auth0.com/docs/flows)

[Back to home page](../README.md)
