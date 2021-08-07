# **Spring App Basics:**

- If you use Gradle, visit the [Spring Initializr](https://start.spring.io/) to generate a new project with the required dependencies (Spring Web, Thymeleaf, and Spring Boot DevTools).(1)

- Example of a controller:(1)

  ```java
  package com.example.servingwebcontent;

  import org.springframework.stereotype.Controller;
  import org.springframework.ui.Model;
  import org.springframework.web.bind.annotation.GetMapping;
  import org.springframework.web.bind.annotation.RequestParam;

  @Controller
  public class GreetingController {

    @GetMapping("/greeting")
    public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
      model.addAttribute("name", name);
      return "greeting";
    }

  }
  ```

- Spring Boot Devtools:

  - Enables hot swapping.

  - Switches template engines to disable caching.

  - Enables LiveReload to automatically refresh the browser.

  - Other reasonable defaults based on development instead of production.

- > Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments.(1)

# **Spring MVC and Thymeleaf:**

- Check this site for more infi >>> [Spring MVC and Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

## Sources:

- (1) [Spring App Basics](https://spring.io/guides/gs/serving-web-content/)

- (2) [Spring MVC and Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

[Back to home page](../README.md)
