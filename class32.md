# Class 32

### What makes an API RESTful?
There are six key constraints that make an API RESTful:
- Client-server separation: the client and server should be independent and able to evolve separately.
- Stateless: each request from the client should contain all the necessary information for the server to understand it. The server should not maintain any client context between requests.
- Cacheable: responses should be explicitly or implicitly cacheable to improve performance.
- Uniform interface: the communication between the client and server should be standardized to simplify the architecture and improve scalability.
- Layered system: a client should not be able to tell if it is communicating directly with the server or through an intermediary layer.
- Code-on-demand (optional): clients can retrieve executable code on demand from the server.

### What is the benefit of using GraphQL? Any downsides?
GraphQL is a query language and runtime for APIs that allows the client to specify exactly what data it needs and get back only that data. This can be beneficial in reducing over-fetching or under-fetching of data and making the API more efficient. Some benefits of using GraphQL include:
- Less network roundtrips: the client can get all the data it needs in a single request.
- Improved developer experience: the client can specify its data requirements, reducing the likelihood of miscommunication between the frontend and backend teams.
- Strongly-typed schema: the schema can be used to validate queries and get better error messages.

Some downsides of using GraphQL include:
- Steep learning curve: GraphQL has a learning curve and requires a considerable amount of upfront work to set it up and use it effectively.
- Caching: caching with GraphQL can be more challenging than with REST APIs due to the dynamic nature of the queries and the lack of a standard caching mechanism.
- More complex server: implementing a GraphQL server requires more work, as it must be able to parse and execute arbitrary queries.

### Describe “serverless” to a new 301 Code Fellows student.
Serverless is a software architecture model where the developers can build and run their applications without worrying about managing or maintaining servers. In this model, the developers can write codes on their local machines and deploy them to a cloud provider who will take care of running the application on their end. Serverless is suitable for developing small and medium applications, backend functions, microservices, and APIs. It is cost-effective, scalable, fast to deploy, and does not require any infrastructure maintenance.
