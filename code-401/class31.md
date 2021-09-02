# **Espresso Testing:**

- Example of Espresso test :

  ```java
  @Test
  public void greeterSaysHello() {
      onView(withId(R.id.name_field)).perform(typeText("Steve"));
      onView(withId(R.id.greet_button)).perform(click());
      onView(withText("Hello Steve!")).check(matches(isDisplayed()));
  }
  ```

- Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:(1)

  - The message queue is empty.
  - There are no instances of AsyncTask currently executing a task.
  - All developer-defined idling resources are idle.

> By performing these checks, Espresso substantially increases the likelihood that only one UI action or assertion can occur at any given time. This capability gives you more reliable and dependable test results.

- The main components of Espresso include the following:
  - Espresso
  - ViewMatchers
  - ViewActions
  - ViewAssertions

# **The Espresso Test Recorder:**

- The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app. Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.(2)

- Espresso tests consist of two primary components:
  - UI interactions include tap and type actions that a person may use to interact with your app.
  - Assertions verify the existence or contents of visual elements on the screen.

## Sources:

- (1) [Espresso Testing](https://developer.android.com/training/testing/espresso)

- (2) [the Espresso Test Recorder](https://developer.android.com/studio/test/espresso-test-recorder)

[Back to home page](../README.md)
