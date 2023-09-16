# Class 16

### Spring Security overview

1. What does it mean to authenticate a user?<br>
    is the process of verifying the identity of a user by checking whether the provided credentials match those in the system. This involves validating the user's identity through mechanisms such as passwords, security tokens, or biometric measurements, and ensuring that only authorized users can access the system.
   The main strategy interface for authentication is AuthenticationManager, which has only one method:
```
   public interface AuthenticationManager {

    Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
   }
```
2. What does it mean to authorize a user?<br>
   Authorization is the process of granting or denying access to specific resources or functionalities based on the verified identity of the user. This involves checking the user's access rights and permissions to determine whether they are authorized to carry out the requested action.
3. What are the three possible outcomes of the AuthenticationManager’s authenticate() method?<br>
   The three possible outcomes of the AuthenticationManager's authenticate() method are:

      1. Return an Authentication object with authenticated=true if the authentication is successful and the input represents a valid principal.

      2. Throw an AuthenticationException if the authentication fails and the input represents an invalid principal.

      3. Return null if the AuthenticationManager cannot decide, typically because the input type is not recognized.



---------------------------------------
