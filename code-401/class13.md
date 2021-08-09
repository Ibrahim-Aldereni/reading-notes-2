# **Working with Relationships in Spring Data REST:**

- One-to-One Relationship and One-to-Many Relationship example example:(1)

  ```java
  // table 1
  @Entity
  public class Library {

      @Id
      @GeneratedValue
      private long id;

      @Column
      private String name;

      @OneToOne
      @JoinColumn(name = "address_id")
      @RestResource(path = "libraryAddress", rel="address")
      private Address address;

      // standard constructor, getters, setters
  }

  // table 2
  @Entity
  public class Address {

      @Id
      @GeneratedValue
      private long id;

      @Column(nullable = false)
      private String location;

      @OneToOne(mappedBy = "address")
      private Library library;

      // standard constructor, getters, setters
  }

  // table 3
  @Entity
  public class Book {

      @Id
      @GeneratedValue
      private long id;

      @Column(nullable=false)
      private String title;

      @ManyToOne
      @JoinColumn(name="library_id")
      private Library library;

      // standard constructor, getter, setter
  }

  // One-to-Many Relationship example
  // add this to above table 1
  public class Library {
    //...

    @OneToMany(mappedBy = "library")
    private List<Book> books;

    //...
  }
  //In order to expose these entities as resources, let's create two repository interfaces for each of them, by extending the CrudRepository interface:

  public interface LibraryRepository extends CrudRepository<Library, Long> {}
  public interface AddressRepository extends CrudRepository<Address, Long> {}
  ```

# **Integration Testing in Spring:**

- > Integration testing plays an important role in the application development cycle by verifying the end-to-end behavior of a system.(2)

- For more info check this site >>> [Integration Testing in Spring](https://www.baeldung.com/integration-testing-in-spring)

## Sources:

- (1) [Working with Relationships in Spring Data REST](https://www.baeldung.com/spring-data-rest-relationships)

- (2) [Integration Testing in Spring](https://www.baeldung.com/integration-testing-in-spring)

[Back to home page](../README.md)
