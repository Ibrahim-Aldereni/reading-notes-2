# **Spring RequestMapping]:**

- **@RequestMapping** this annotation is used to map web requests to Spring Controller methods.

- Get request example:(1)

  ```java
  @RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
  @ResponseBody
  public String getFoosBySimplePath() {
      return "Get some Foos";
  }
  ```

- Get request with multiple headers example:(1)

  ```java
  @RequestMapping(
  value = "/ex/foos",
  headers = { "key1=val1", "key2=val2" }, method = GET)
  @ResponseBody
  public String getFoosWithHeaders() {
      return "Get some Foos with Header";
  }
  ```

- Accept header vs produces:(1)

  ```java
  // OLD
  @RequestMapping(
  value = "/ex/foos",
  method = GET,
  headers = "Accept=application/json")
  @ResponseBody
  public String getFoosAsJsonFromBrowser() {
      return "Get some Foos with Header Old";
  }

  //NEW
  @RequestMapping(
  value = "/ex/foos",
  method = RequestMethod.GET,
  produces = "application/json"
  )
  @ResponseBody
  public String getFoosAsJsonFromREST() {
      return "Get some Foos with Header New";
  }
  ```

- Single and multipl @PathVariable:(1)

  ```java
  // single
  @RequestMapping(value = "/ex/foos/{id}", method = GET)
  @ResponseBody
  public String getFoosBySimplePathWithPathVariable(@PathVariable String id) {
      return "Get a specific Foo with id=" + id;
  }

  //multiple
  @RequestMapping(value = "/ex/foos/{fooid}/bar/{barid}", method = GET)
  @ResponseBody
  public String getFoosBySimplePathWithPathVariables
    (@PathVariable long fooid, @PathVariable long barid) {
      return "Get a specific Bar with id=" + barid +
        " from a Foo with id=" + fooid;
  }
  ```

- RequestMapping With Request Parameters example:(1)

  ```java
  // http://localhost:8080/spring-rest/ex/bars?id=100

  @RequestMapping(value = "/ex/bars", method = GET)
  @ResponseBody
  public String getBarBySimplePathWithRequestParam(@RequestParam("id") long id) {
      return "Get a specific Bar with id=" + id;
  }
  ```

- New HTTP mapping annotations, all based on @RequestMapping:(1)

  ```java
  @GetMapping("/{id}")
  public ResponseEntity<?> getBazz(@PathVariable String id){
      return new ResponseEntity<>(new Bazz(id, "Bazz"+id), HttpStatus.OK);
  }

  @PostMapping
  public ResponseEntity<?> newBazz(@RequestParam("name") String name){
      return new ResponseEntity<>(new Bazz("5", name), HttpStatus.OK);
  }

  @PutMapping("/{id}")
  public ResponseEntity<?> updateBazz(
    @PathVariable String id,
    @RequestParam("name") String name) {
      return new ResponseEntity<>(new Bazz(id, name), HttpStatus.OK);
  }

  @DeleteMapping("/{id}")
  public ResponseEntity<?> deleteBazz(@PathVariable String id){
      return new ResponseEntity<>(new Bazz(id), HttpStatus.OK);
  }
  ```

# **Accessing Data with JPA:**

- JPA (Java Persistence API) used to store and retrieve data in a relational database.

- Entity example:(2)

  ```java
  package com.example.accessingdatajpa;

  import javax.persistence.Entity;
  import javax.persistence.GeneratedValue;
  import javax.persistence.GenerationType;
  import javax.persistence.Id;

  //class is annotated with @Entity indicating that it is a JPA entity Because no @Table annotation exists, it is assumed that this entity is mapped to a table.
  @Entity
  public class Customer {

    //The Customer object’s id property is annotated with @Id so that JPA recognizes it as the object’s ID. The id property is also annotated with @GeneratedValue to indicate that the ID should be generated automatically.
    @Id
    @GeneratedValue(strategy=GenerationType.AUTO)
    private Long id;
    private String firstName;
    private String lastName;

    protected Customer() {} //he default constructor exists only for the sake of JPA. You do not use it directly, so it is designated as protected

    //This constructor is the one you use to create instances of Customer to be saved to the database
    public Customer(String firstName, String lastName) {
      this.firstName = firstName;
      this.lastName = lastName;
    }

    @Override
    public String toString() {
      return String.format(
          "Customer[id=%d, firstName='%s', lastName='%s']",
          id, firstName, lastName);
    }

    public Long getId() {
      return id;
    }

    public String getFirstName() {
      return firstName;
    }

    public String getLastName() {
      return lastName;
    }
  }
  ```

# **Comparing repositories:**

- JpaRepository example:(3)

  ```java
  @Entity
  public class Product {

      @Id
      private long id;
      private String name;

      // getters and setters
  }

  //find a Product based on its name
  @Repository
  public interface ProductRepository extends JpaRepository<Product, Long> {
      Product findByName(String productName);
  }
  ```

## Sources:

- (1) [Spring RequestMapping](https://www.baeldung.com/spring-requestmapping)

- (2) [Accessing Data with JPA](https://spring.io/guides/gs/accessing-data-jpa/)

- (3) [Comparing repositories](https://www.baeldung.com/spring-data-repositories)

[Back to home page](../README.md)
