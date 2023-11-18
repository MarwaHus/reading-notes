# Class 36

#### Where in your application should you check the current auth session?

The check for the current authentication session is typically done in parts of your application where user authentication matters. This often includes sensitive operations, access to user-specific data, or pages that require authentication. For example, you might check the authentication session in a route guard for a web application or at the beginning of a function that requires an authenticated user in a server-side application.

#### what is the command that is used to push your changes to the cloud?

If you are using a cloud service like AWS Amplify for your application deployment, the command might be `amplify push`.

#### What does Amplify Auth do for your application?

Amplify Auth is a service provided by AWS Amplify that simplifies the process of adding user authentication and authorization to your application. It provides a set of pre-built components, libraries, and backend services that handle user management, authentication flows (sign-up, sign-in), and secure access to resources. Amplify Auth helps you implement secure user authentication without having to build complex authentication systems from scratch.
