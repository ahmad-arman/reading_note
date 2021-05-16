##  What’s the difference between PUT and PATCH?
 Put : <br>
 PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PUT is similar to POST in that it can create resources, but it does so when there is a defined URI. PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn’t exist.

 patch: <br>
 applies a partial update to the resource.
 This means that you are only required to send the data that you want to update, and it won’t affect or change anything else.

 [click for more information](https://rapidapi.com/blog/put-vs-patch/?utm_source=google&utm_medium=cpc&utm_campaign=DSA&gclid=CjwKCAjwhYOFBhBkEiwASF3KGS0SosAiBv84NKqmvFwWfjSHU4-wS0IEhx5bAo52VK7jvsob-wW21RoCKGYQAvD_BwE)

## Provide links to 3 services or tools that allow you to “mock” an API for development like json-server 
 1 – Nock <br>
 2 – MockServer <br>
 3 – Postman Mock Server <br>

[click for more information](https://nordicapis.com/10-tools-to-mock-http-requests/)

##  Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?

 This module allows you to serve auto-generated swagger-ui generated API docs from express, based on a swagger.json file. The result is living documentation for your API hosted from your API server via a route.

 Swagger version is pulled from npm module swagger-ui-dist. Please use a lock file or specify the version of swagger-ui-dist you want to ensure it is consistent across environments.

 [click for more information](https://www.npmjs.com/package/swagger-ui-express)

## Compare and contrast SOAP and ReST

 SOAP (Simple Object Access Protocol) is a standards-based web services access protocol that has been around for a long time. Originally developed by Microsoft, SOAP isn’t as simple as the acronym would suggest.

 REST (Representational State Transfer) is another standard, made in response to SOAP’s shortcomings. It seeks to fix the problems with SOAP and provide a simpler method of accessing web services. 

 [click for more information](https://smartbear.com/blog/soap-vs-rest-whats-the-difference/)


## Term 

 Web Server : A web server is a computer that runs websites. It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users. This intercommunication is done using Hypertext Transfer Protocol (HTTP). 

 [click for more information](https://economictimes.indiatimes.com/definition/web-server)

 Express:   is a minimal and flexible Node.js web application framework that provides a robust set of features to develop web and mobile applications. It facilitates the rapid development of Node based Web applications

 [click for more information](https://www.tutorialspoint.com/nodejs/nodejs_express_framework.htm)


 Routing : Routing defines the way in which the client requests are handled by the application endpoints.

 [click for more information](https://www.geeksforgeeks.org/routing-in-node-js/)


 WRRC: The request/response cycle traces how a user’s request flows through the app


# What is TDD 

 Test-driven development” refers to a style of programming in which three activities are tightly interwoven: coding, testing (in the form of writing unit tests) and design (in the form of refactoring).

### Expected Benefits :
 1-many teams report significant reductions in defect rates, at the cost of a moderate increase in initial development effort

 2-the same teams tend to report that these overheads are more than offset by a reduction in effort in projects’ final phases

 [click for more information](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))



# What is CI /CD

 CI :Continuous Integration (CI) is the process of automating the build and testing of code every time a team member commits changes to version control.

 CD : Continuous Deployment (CD) can be thought of as an extension of continuous integration, and is the process of automatically deploying an application after CI is successful

## Continuous Integration Benefits:
1-Fewer bugs
2-Less context switching as developers are alerted as soon as they break the build
3-Testing costs are reduced
4-Your QA team spend less time testing

## Continuous Deployment Benefits:
 1-Releases are less risky
 2-Easy release
 3-Customers see a continuous stream of improvements
 4-Expedite development as there’s no need to pause development for releases


 [click for more information](https://medium.com/@tamizharasank/a-way-to-setup-the-ci-cd-pipeline-for-a-node-app-server-93268a40d7fa#:~:text=Continuous%20Integration%20(CI)%20is%20the,application%20after%20CI%20is%20successful.)





# REFERENCE 


[An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)<br>
[What is NPM?](https://docs.npmjs.com/about-npm) <br>
[What is TDD?](https://www.agilealliance.org/glossary/tdd/) <br>
[CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)<br>


[nodeJS docs](https://nodejs.org/en/docs/)<br>
[npm docs](https://docs.npmjs.com/)<br>
[express docs](https://expressjs.com/en/4x/api.html)<br>
[http status codes](https://www.restapitutorial.com/httpstatuscodes.html)<br>
[supertest](https://github.com/visionmedia/supertest)<br>

