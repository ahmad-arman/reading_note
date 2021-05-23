## Write the following steps in the correct order

Register your application to get a client_id and client_secret <br>

Ask the client if they want to sign in via a third party <br>
Redirect to a third party authentication endpoint <br>
Make a request to the third-party API endpoint <br>
Receive authorization code <br>
Make a request to the access token endpoint <br>
Receive access token <br>

##  What can you do with an authorization code ? 

to make a request to get an access token .

##  What can you do with an access token? 

 it is access tokens are used in token-based authentication to allow an application to access an API.

## What’s a benefit of using OAuth instead of your own basic authentication?

It allows limited access to the user's data and allows accessing when authorization tokens expire. It has ability to share data for users without having to release personal information. It is easier to implement and provides stronger authentication.

### Tram

* A Client ID : is an identifier associated with an application that assists with client / server OAuth 2.0 authentication for ArcGIS client APIs . Developers create a client ID by defining an application on their developer dashboard.

* Client Secret : is a secret known only to your application and the authorization server. It protects your resources by only granting tokens to authorized requestors. Protect your client secrets and never include them in mobile or browser-based apps.

* Authentication Endpoint : is an HTTP endpoint that micropub and IndieAuth clients can use to identify a user or obtain an authorization code (which is then later exchanged for an access token) to be able to post to their website.

* The token endpoint is where apps make a request to get an access token for a user. This section describes how to verify token requests and how to return the appropriate response and errors. Authorization Code. Password Grant. Client Credentials.

* API endpoint is the point of entry in a communication channel when two systems are interacting. It refers to touchpoints of the communication between an API and a server. ... An API endpoint is basically a fancy word for a URL of a server or service.

* The authorization code is a temporary code that the client will exchange for an access token. The code    itself is obtained from the authorization server where the user gets a chance to see what the information the client is requesting, and approve or deny the request.
 
* An access token is an object encapsulating the security identity of a process or thread. A token is used to make security decisions and to store tamper-proof information about some system entity.



## What is JSON Web Token?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA. 

## When should you use JSON Web Tokens?
Here are some scenarios where JSON Web Tokens are useful:

 * Authorization: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

 * Information Exchange: JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.


[JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

[Intro to JWT](https://jwt.io/introduction/)

[Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)

[npm jsonwebtoken docs](https://www.npmjs.com/package/jsonwebtoken)