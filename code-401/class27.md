# **Android Tasks and the Back Stack:**

- A task is a collection of activities that users interact with when performing a certain job.(1)

- When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. The previous activity remains in the stack, but is stopped. When an activity stops, the system retains the current state of its user interface. When the user presses the Back button, the current activity is popped from the top of the stack (the activity is destroyed) and the previous activity resumes (the previous state of its UI is restored).(1)

  ![pic1](./img/diagram_backstack.png)

- The way Android manages tasks and the back stack, as described above—by placing all activities started in succession in the same task and in a "last in, first out" stack—works great for most apps and you shouldn't have to worry about how your activities are associated with tasks or how they exist in the back stack.(1)

- Launch modes allow you to define how a new instance of an activity is associated with the current task. You can define different launch modes in two ways:
- Using the manifest file
- Using Intent flags

# **Android SharedPreferences:**

- If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs. A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.(2)

- You can create a new shared preference file or access an existing one by calling one of these methods:
  - getSharedPreferences()
  - getPreferences()

## Sources:

- (1) [Android Tasks and the Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack)

- (2) [Android SharedPreferences](https://developer.android.com/training/data-storage/shared-preferences)

[Back to home page](../README.md)
