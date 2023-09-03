# Class 11

### Spring App Basics

1. What role do the @Controller classes play in a Spring MVC application?<br>
 In a Spring MVC application, the @Controller classes are responsible for:

* Handling HTTP requests: They use annotations such as @RequestMapping to map incoming HTTP requests to specific methods within the class.

* Containing business logic: @Controller classes handle user requests by executing the appropriate business logic and returning a response to the user.

* Returning views: They return views (HTML pages, JSON data, etc.) to the user for rendering by the browser or other clients.

* Coordinating with other components: They work closely with other Spring MVC components, such as the model and view, to provide seamless handling of user requests.

In summary, @Controller classes play a crucial role in a Spring MVC application as they are responsible for processing user requests, executing business logic, and returning the appropriate response to the user.
  
2. Explain to a non-technical friend what a GET request is<br>
   
  Think of a GET request as a way you ask for something from a website. You know when you go to a restaurant and the waiter comes over to ask you what you would like to order? A GET request is a bit like that, but instead of food, you are asking for information from a website.

3. What annotation should be placed on your Spring Boot application class?<br>
   
The `@SpringBootApplication` annotation should be placed on the main class of a Spring Boot application. 
Here's how you use @SpringBootApplication:

```java
@SpringBootApplication
public class MySpringBootApplication {

    public static void main(String[] args) {
        SpringApplication.run(MySpringBootApplication.class, args);
    }
}
```

### Spring MVC and Thymeleaf.

1. What method allows for a variable defined in Java (in your Spring Controller) to be dispalyed in HTML with the help of Thymeleaf?<br>
   The method that allows a variable defined in Java (in your Spring Controller) to be displayed in HTML with the help of Thymeleaf is the addAttribute method. This method is provided by the Model class which is injected into the controller method as a parameter. When you add an attribute to the Model object, it becomes available to the view for rendering.
      ```java
        @GetMapping("/hello")
        public String hello(Model model) {
            String message = "Hello, world!";
            model.addAttribute("message", message);
            return "hello";
        }
   ```
2. Explain the role of a @Controller class in a Spring MVC application.<br>
   A @Controller class in a Spring MVC application is responsible for handling HTTP requests and returning an HTTP response. It acts as an intermediate layer between the user interface and the application logic, processing requests and invoking the necessary business logic to fulfill them, and then assembling and returning the appropriate response.

    The @Controller annotation is used to mark a class as a controller, and the methods in the class are mapped to specific HTTP requests using annotations such as @RequestMapping, @GetMapping, @PostMapping, etc. 

    Here is an example of a simple controller class in Spring MVC:

    ```java
    @Controller
    public class MyController {

        @GetMapping("/hello")
        public String hello(Model model) {
            String message = "Hello, world!";
            model.addAttribute("message", message);
            return "hello";
        }
    }
    ```
3. What is a model attribute refered to in Thymeleaf?<br>
     In Thymeleaf, a model attribute refers to a variable or object that is made available to the view for rendering. In the Spring MVC context, these attributes are typically added to the Model object by the controller methods using the addAttribute() method.

    For example, in the following code snippet, a "user" object is added as a model attribute:

    ```java
    @GetMapping("/user/{id}")
    public String getUser(@PathVariable Long id, Model model) {
        User user = userService.getUserById(id);
        model.addAttribute("user", user);
        return "user";
    }
    ```


