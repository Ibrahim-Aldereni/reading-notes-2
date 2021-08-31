# **Overview: Saving data with Room:**

- The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite.(1)

- Room benefits:(1)

  - Compile-time verification of SQL queries.
  - Convenience annotations that minimize repetitive and error-prone boilerplate code.
  - Streamlined database migration paths.

- Room components:(1)

  - The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
  - Data entities that represent tables in your app's database.
  - Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.v

# **Defining entities in Room:**

- When use Room persistence library, we define entities to represent the objects that you want to store. Each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.(2)

- We define each Room entity as a class that is annotated with @Entity. A Room entity includes fields for each column in the corresponding table in the database, including one or more columns that comprise the primary key.(2)

# **Related entities in Room:**

- A **one-to-one** relationship between two entities is a relationship where each instance of the parent entity corresponds to exactly one instance of the child entity, and vice-versa.example:(3)

  ```java
  @Entity
  public class User {
      @PrimaryKey public long userId;
      public String name;
      public int age;
  }

  @Entity
  public class Library {
      @PrimaryKey public long libraryId;
      public long userOwnerId;
  }

  public class UserAndLibrary {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userOwnerId"
    )
    public Library library;

  }

  @Transaction
  @Query("SELECT * FROM User")
  public List<UserAndLibrary> getUsersAndLibraries();
  ```

- A **one-to-many** relationship between two entities is a relationship where each instance of the parent entity corresponds to zero or more instances of the child entity, but each instance of the child entity can only correspond to exactly one instance of the parent entity.example:(3)

  ```java
  @Entity
  public class User {
      @PrimaryKey public long userId;
      public String name;
      public int age;
  }

  @Entity
  public class Playlist {
      @PrimaryKey public long playlistId;
      public long userCreatorId;
      public String playlistName;
  }

  public class UserWithPlaylists {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userCreatorId"
    )
    public List<Playlist> playlists;
  }

  @Transaction
  @Query("SELECT * FROM User")
  public List<UserWithPlaylists> getUsersWithPlaylists();
  ```

# **Accessing data with Room:**

- **defining data access objects, or DAOs**. Each DAO includes methods that offer abstract access to your app's database. At compile time, Room automatically generates implementations of the DAOs that you define.(4)

- You can define each DAO as either an interface or an abstract class. For basic use cases, you should usually use an interface. In either case, you must always annotate your DAOs with @Dao. DAOs don't have properties, but they do define one or more methods for interacting with the data in your app's database, example (4)

  ```java
  @Dao
  public interface UserDao {
      @Insert
      void insertAll(User... users);

      @Delete
      void delete(User user);

      @Query("SELECT * FROM user")
      List<User> getAll();
  }
  ```

## Sources:

- (1) [Overview: Saving data with Room](https://developer.android.com/training/data-storage/room)

- (2) [Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data)

- (3) [Related entities in Room](https://developer.android.com/training/data-storage/room/relationships)

- (4) [Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java)

[Back to home page](../README.md)
