# **Java Imports:**

- Package is a directory where all related classes exist.

- First thing after comments must be package declartion then import declartion then the class definition, example:(1)

  ```java
  package illustration;

  import java.awt.*;

  public class Drawing {
      . . .
  }
  ```

- Import options:(1)

  - ```java
     import javax.swing.*;  // Make all classes visible altho only one is used.
    ```

  - ```java
       import javax.swing.JOptionPane;  // Make a single class visible.
    ```

  - ```java
      class ImportTest {
        public static void main(String[] args) {
            javax.swing.JOptionPane.showMessageDialog(null, "Hi"); // without import
            System.exit(0);
        }
      }
    ```

# **Different types of loops in Java:**

- > Looping is a feature which facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false.(2)

- Types of loops that used in Java: for, foreach, while, do-while.

- For loop used to repeat certain operations by incrementing and evaluating a loop counter, example:(2)

  ```java
  for (int i = 0; i < 5; i++) {
    System.out.println("Simple for loop: i = " + i);
  }
  ```

- For each or enhanced foreach is same as for loop but simplier and it have a drawbacks that you can't access the index and you can't control inc/dec logic, example:(2)

  ```java
  int[] intArr = { 0,1,2,3,4 };
  for (int num : intArr) {
    System.out.println("Enhanced for-each loop: i = " + num);
  }
  ```

- While loop repeats a statement or a block of statements while its controlling Boolean-expression is true, example:(2)

  ```java
  int i = 0;
  while (i < 5) {
    System.out.println("While loop: i = " + i++);
  }
  ```

- Do-while works same as while loop but the differnce is that it execute at least once, example: (2)

  ```java
  int i = 0;
  do {
    System.out.println("Do-While loop: i = " + i++);
  } while (i < 5);
  ```

---

## Sources:

- (1) [Packages and Import](https://perso.ensta-paris.fr/~diam/java/online/notes-java/language/10basics/import.html)

- (2) [A Guide to Java Loops](https://www.baeldung.com/java-loops)

[Back to home page](../README.md)
