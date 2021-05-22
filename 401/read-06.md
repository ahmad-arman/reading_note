

## what a “Singleton” is (in Computer Science terms) :

In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.

## how the Singleton pattern can be used with Node modules, specifically with classes?

* A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance
* static method would have access to the private constructor.
* the static method would create an instance of the class if not exists (getInstance()) or call the instance in created before.

## If I was tasked with building a middleware system like Express uses, the approach I might take to construct/operate it: 
* Allow the middleware to have access to both layers
* req ,res ,next

## Vocabulary Terms 
* Router Middleware : it is a piece of code that comes in the middle of request and response. It kind of hijacks your request so that you can do anything that you want with your request or response eg: Modify the data or call the next middleware.

*  Dynamic Module Loading : is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. It is one of the 3 mechanisms by which a computer program can use some other software; the other two are static linking and dynamic linking. 

* The Singleton Pattern : Singleton Pattern is  limits the number of instances of a particular object to just one. This single instance is called the singleton. Singletons are useful in situations where system-wide actions need to be coordinated from a single central place. An example is a database connection pool.

 * CRUD -> REST Method Matches :
 1- create –> POST <br>
 2- read –> GET  <br>
 3- update –> PUT/PATCH  <br>
 4- delete –> DELETE  <br>

 * Mock Testing :Mock functions allow you to test the links between code by erasing the actual implementation of a function, capturing calls to the function (and the parameters passed in those calls), capturing instances of constructor functions when instantiated with new, and allowing test-time configuration of return values.


## Preparation Materials

###  Securing Passwords



1- Passwords: minimum length of 8 characters, common maximum length is 64 characters

2-Transmit passwords only over TLS (transport layer protection) or other strong transport

3-Require re-authentication for sensitive features

4-Account lockout: prevent any more login attempts after a series of failed logins

### Basic Auth 

basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :.

* Server side : 
When the server wants the user agent to authenticate itself towards the server, the server must respond appropriately to unauthenticated requests.

To unauthenticated requests, the server should return a response which contains a HTTP 401 Unauthorized status line[5] and a WWW-Authenticate header field.

* Client side : 

When the user agent wants to send authentication credentials to the server, it may use the Authorization header field.

### Authentication Cheat Sheet 

1- Authentication is the process of verifying that an individual, entity or website is whom it claims to be. Authentication in the context of web applications is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

### node.bcrypt.js :
A library to help you hash passwords.

You can read about bcrypt in Wikipedia as well as in the following article: How To Safely Store A Password

[Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)

[Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)

[OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

[bcrypt docs](https://www.npmjs.com/package/bcrypt)