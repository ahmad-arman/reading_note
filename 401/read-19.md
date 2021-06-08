#### Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server

both uses RESTful api and uses HTTP for res/req ,Key Authentication ,HTTPS,CORS,oAuth2 ,both uses function to handle those requests and create proper response.

#### List the AWS Database offerings and talk about the pros and cons of each
1- Amazon RDS :  Managed Relational Database Service for MySQL, PostgreSQL, MariaDB, Oracle BYOL, or SQL Server and can’t be integrated with lambda function in aws.
2-Amazon DynamoDB :Fast and flexible NoSQL database with seamless scalability and can be integrated with lambda function in aws. .
3-Amazon ElastiCache
4-Amazon Timestream
#### What’s the difference between a FIFO and a standard queue?
Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue. 
FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue
#### How can the server be assured a message was properly received?

by listening to a received event triggered when the message received , 

## Terms 

* Serverless API :API gateway that handles request and response without integrating it in the server .

* triggers: Triggers are stored programs, which are automatically executed or fired when some events occur. Triggers are, in fact, written to be executed in response to any of the following events − A database manipulation (DML) statement (DELETE, INSERT, or UPDATE) A database definition (DDL) statement (CREATE, ALTER, or DROP).

* Dynamo vs Mongo: DynamoDB is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas. … DynamoDB uses tables, items and attributes, MongoDB uses JSON-like documents. DynamoDB supports limited data types and smaller item sizes; MongoDB supports more data types and has fewer size restrictions.

* Dynamoose vs Mongoose: Dynamoose is a modeling tool for Amazon’s DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familiar.

## AWS — Difference between SQS and SNS

SQS: Simple Queue Service.
SNS: Simple Notification Service.

SQS and SNS are important components for scalable, large scale, distributed, cloud-based applications: SNS is a distributed publish-subscribe service. SQS is distributed queuing service.

## SNS Javascript SDK

Amazon Simple Notification Service (Amazon SNS) is a web service that enables you to build distributed web-enabled applications. Applications can use Amazon SNS to easily push real-time notification messages to interested subscribers over multiple delivery protocols. For more information about this product see the Amazon SNS product page. For detailed information about Amazon SNS features and their associated API calls, see the Amazon SNS Developer Guide.

## REFERENCE 

[SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)<br>
[AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)<br>
[SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)<br>
[SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)<br>