### What are serverless functions?

s a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier

#### If you were to create a system that emulated Lambda functions, how would you do it? 

1-Open the Functions page on the Lambda console.

2-Choose Create function.

3-Under Basic information, do the following:

   a-For Function name, enter my-function.

   b-For Runtime, confirm that Node.js 14.x is selected. Note that Lambda provides runtimes for .NET (PowerShell,C#) Go, Java, Node.js, Python, and Ruby.

4-Choose Create function.

### Describe how a CDN works ?

To minimize the distance between the visitors and your website's server, a CDN stores a cached version of its content in multiple geographical locations (a.k.a., points of presence, or PoPs). ... In essence, CDN puts your content in many places at once, providing superior coverage to your users.

## Term 
* Serverless Functions : s a programmatic function written by a software developer for a single purpose. It's then hosted and maintained on infrastructure by cloud computing companies. These companies take care of code maintenance and execution so that developers can deploy new code faster and easier
* Cloud Storage : allows you to save data and files in an off-site location that you access either through the public internet or a dedicated private network connection. Data that you transfer off-site for storage becomes the responsibility of a third-party cloud provider.
* CDN :allows for the quick transfer of assets needed for loading Internet content including HTML pages, javascript files, stylesheets, images, and videos.


## AWS API Gateway Overview 

#### What is Amazon API Gateway? 

 is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.
#### How does API Gateway work? 

API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

#### How does API Gateway integrate with other AWS services?

Many AWS services support integration with Amazon API Gateway, including:

 * AWS Lambda: run Lambda functions to generate HTTP API responses.
 * AWS SNS: publish SNS notifications when an HTTP API endpoint is accessed.
 * Amazon Cognito: provide authentication and authorization for your HTTP APIs.

## What is DynamoDB?

is a hosted NoSQL database offered by Amazon Web Services (AWS).

 * DynamoDB is a particularly good fit for the following use cases:

 1-Applications with large amounts of data and strict latency requirements. 

 2-Serverless applications using AWS Lambda. 

 3-Data sets with simple, known access patterns.

### Amazon DynamoDB
Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-active, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB can handle more than 10 trillion requests per day and can support peaks of more than 20 million requests per second.


### REFERENCE 
* [AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway) 

* [AWS API Gateway](https://aws.amazon.com/api-gateway/)

* [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/) 
 
* [AWS DynamoDB](https://aws.amazon.com/dynamodb/) 

* [Dynamoose](https://dynamoosejs.com/getting_started/Introduction/)