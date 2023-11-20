# Class 37

#### What is Amazon S3?
Amazon S3 (Simple Storage Service) is a scalable cloud storage service provided by Amazon Web Services (AWS). It is designed to store and retrieve any amount of data from anywhere on the web. S3 offers durability, availability, and security for storing and managing data.
#### List at least 3 features that it offers to its users.
Three features of Amazon S3 are:

1. Scalability and Durability: Amazon S3 is designed for durability, with data automatically distributed across multiple devices and multiple facilities within a region. It provides 99.999999999% (11 nines) durability, meaning that objects stored in S3 are highly resilient and are designed to withstand the loss of data.

2. Data Access Control and Security: S3 allows users to control access to their data through robust access control lists (ACLs) and bucket policies. It also supports server-side encryption for data at rest and transit, using AWS Key Management Service (KMS) or customer-provided encryption keys. Additionally, S3 integrates with AWS Identity and Access Management (IAM) for fine-grained access control.

3. Data Management and Analytics: S3 provides features for managing and analyzing data stored in it. It supports lifecycle policies, which allow users to automatically transition objects between different storage classes based on defined rules. It also integrates with other AWS services like Amazon Athena, Amazon Redshift, and Amazon EMR for data processing and analytics. S3 also supports event notifications, enabling users to trigger workflows or notifications based on object-level operations.
   
#### What is an object key?
In Amazon S3, an object key is the unique identifier assigned to each object (file) stored in an S3 bucket. The object key is used to retrieve and manage objects in S3. It is similar to a full path or file name in a traditional file system. The object key is a string that can include alphanumeric characters, special characters, and slashes ("/").
The object key in S3 is important because it determines the object's unique identifier within a bucket and helps organize and locate objects within the bucket hierarchy. It is important to note that S3 is a key-value store, which means objects are accessed by their keys, and not through a hierarchical file structure.
#### Which dependencies are needed to install Amplify AWS S3 to your ndroid application?
To install Amplify AWS S3 in an Android application, you need to add the following dependencies to your project's build.gradle file:
```
dependencies {
    implementation 'com.amplifyframework:aws-storage-s3:1.24.0'
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```
#### What is needed in order to upload data to your bucket?
To upload data to your bucket using Amplify AWS S3, you need the following:

1. AWS Account: You need an AWS account to create an S3 bucket and access its credentials.

2. Amplify CLI: Amplify CLI is a command-line tool provided by AWS that helps in setting up Amplify resources and generating necessary configuration files. You'll need Amplify CLI installed and configured on your local machine.

3. Configuration Setup: After configuring Amplify CLI, you need to initialize Amplify in your Android application and configure it to enable the Storage category for S3.
#### what method(s) initialize(s) the Amplify Auth and Storage categories?
To initialize the Amplify Auth and Storage categories, you need to call the `Amplify.configure()` method with the necessary configurations. Here is an example:

```
Amplify.configure(getApplicationContext());
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.addPlugin(new AWSS3StoragePlugin());
```

This code initializes Amplify, adds the necessary plugins for Auth and Storage (Cognito and S3), and configures them with default settings.

After initializing the Amplify Auth and Storage categories, you can use Amplify APIs to handle authentication and interact with your S3 bucket for uploading and downloading data.
