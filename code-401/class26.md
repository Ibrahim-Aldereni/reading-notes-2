# **Application Fundamentals :**

![android](./img/android.png)

- > Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.(1)

- An Android package, which is an archive file with an **.apk** suffix.

- An Android App Bundle, which is an archive file with an **.aab** suffix.

- The Android system implements the principle of least privilege. That is, each app, by default, has access only to the components that it requires to do its work and no more. This creates a very secure environment in which an app cannot access parts of the system for which it is not given permission.

- There are four different types of app components:

  - Activities
  - Services
  - Broadcast receivers
  - Content providers

- **An activity** is the entry point for interacting with the user. It represents a single screen with a user interface.(1)

- **A service** is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.(1)

- **A broadcast receiver** is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.(1)

- **A content provider** manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access.(1)

- > Three of the four component types—activities, services, and broadcast receivers—are activated by an asynchronous message called an intent. Intents bind individual components to each other at runtime(1)

## Sources:

- (1) [Android fundamentals](https://developer.android.com/guide/components/fundamentals)

[Back to home page](../README.md)
