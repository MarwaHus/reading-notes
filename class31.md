# Class 31

### What are a few alternatives to AWS Amplify? What are the differences? What are the tradeoffs?

1. Firebase: Firebase is a popular mobile and web application development platform that provides a range of services including authentication, hosting, and realtime database. It offers a free tier similar to AWS Amplify and provides a unified API that enables easy integration with mobile and web applications. Firebase is provided by Google rather than AWS, which is the main difference between the two services.
Tradeoffs: While Firebase is an excellent alternative to AWS Amplify, it can become more expensive than Amplify for some use cases due to its pricing model based on data storage, data transfer, and API calls. Firebase also does not provide some features offered by Amplify, e.g. GraphQL API and app delivery service.
2. Parse: Parse is an open-source Platform as a Service (PaaS) for mobile and web applications development. It is similar to AWS Amplify and Firebase in the sense that it offers a range of services including push notifications, user authentication, and data storage. The difference is that Parse is self-hosted rather than a cloud-based service provided by a cloud vendor.
Tradeoffs: Parse requires more maintenance and setup time since it is self-hosted and requires a server to run. It may also not be suitable for more demanding applications with high traffic or require extensive scale, as the server may become a bottleneck.
3. Hasura: Hasura is an open-source backend-as-a-service (BaaS) provider that enables developers to build scalable and fast GraphQL APIs on top of their databases. Hasura provides features such as authentication, authorization, and data queries with the GraphQL API.
Tradeoffs: Hasura is primarily focused on providing a GraphQL API, which may not fit all use cases. It is also more database-focused and less feature-rich compared to AWS Amplify and Firebase, making it less suitable for applications requiring other services like push notifications.

