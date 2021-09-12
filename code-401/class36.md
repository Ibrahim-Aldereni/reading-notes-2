# **Amplify and Cognito:**

- The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool.(1)

- Steps:

  - Configure Auth Category:
    1- amplify add auth
    2- fill info.
    3- amplify push.

  - Install Amplify Libraries:

    ```
    dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
    }
    ```

  - Initialize Amplify Auth:
    ```
    // Add this line, to include the Auth plugin.
    Amplify.addPlugin(new AWSCognitoAuthPlugin());
    Amplify.configure(getApplicationContext());
    ```
  - Check the current auth session:
    ```
    Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString()));
    ```

## Sources:

- (1) [Amplify and Cognito](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)

[Back to home page](../README.md)
