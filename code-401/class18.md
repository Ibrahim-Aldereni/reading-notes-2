# **Hibernate Many to Many:**

- For example if we have **employee** table and **project** table, here the emplyee can have multiple projects and the project can have multiple employees, so the relation is many to many. We have an employee table with employee_id as its primary key and a project table with project_id as its primary key. A join table employee_project is required here to connect both sides.(1)

- In the example above the model classes (entites) look like this:

  ```java
  @Entity
  @Table(name = "Employee")
  public class Employee {
      // ...

      @ManyToMany(cascade = { CascadeType.ALL })
      @JoinTable(
          name = "Employee_Project",
          joinColumns = { @JoinColumn(name = "employee_id") },
          inverseJoinColumns = { @JoinColumn(name = "project_id") }
      )
     Set<Project> projects = new HashSet<>();

      // standard constructor/getters/setters
  }

  @Entity
  @Table(name = "Project")
  public class Project {
      // ...

      @ManyToMany(mappedBy = "projects")
      private Set<Employee> employees = new HashSet<>();

      // standard constructors/getters/setters
  }
  ```

- > This association has two sides i.e. the owning side and the inverse side. In our example, the owning side is Employee so the join table is specified on the owning side by using the @JoinTable annotation in Employee class(1)

## Sources:

- (1) [Hibernate Many to Many](https://www.baeldung.com/hibernate-many-to-many)

- (2) [Security: a humorous overview](https://scholar.harvard.edu/files/mickens/files/thisworldofours.pdf)

[Back to home page](../README.md)
