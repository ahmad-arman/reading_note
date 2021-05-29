## Why is access control important?

Access controls limit access to information and information processing systems. When implemented effectively, they mitigate the risk of information being accessed without the appropriate authorisation, unlawfully and the risk of a data breach 
## Describe an application that would need access control.

Access control is a method of guaranteeing that users are who they say they are and that they have the appropriate access to company data.

At a high level, access control is a selective restriction of access to data. It consists of two main components: authentication and authorization, says Daniel Crowley, head of research for IBM’s X-Force Red, which focuses on data security.

## What is a role used for?

use to give the user authorization ,The assignment of access rights in RBAC is very systematic and repeatable, easier to audit user rights (users are in only one of a few categories), and easier to correct any issues that are identified. There is no case by case assignment of roles, users fall into one of already pre-assigned roles/capabilities.
## Why is role based access control more scalable than discretionary or mandatory access control?

The assignment of access rights in RBAC is very systematic and repeatable, easier to audit user rights (users are in only one of a few categories), and easier to correct any issues that are identified. There is no case by case assignment of roles, users fall into one of already pre-assigned roles/capabilities.

## Terms 
1- Authorization:determine access levels or user/client privileges related to system resources including files, services, computer programs, data and application features, Is the process of giving someone the ability to access a resource.<br>
2-Role Based Access Control (RBAC):is a method of restricting network access based on the roles of individual users within an enterprise. RBAC lets employees have access rights only to the information they need to do their jobs and prevents them from accessing information that doesn't pertain to them..<br>
3-Capabilities: The functions that a user has access to. For example: (read,delete)<br>



## Event-Driven Programming in Node.js


### EventEmitter : 
that allows us to get started incorporating Event-Driven Programming in our project right away.

We access the EventEmitter class through the events module. Once imported we’ll need to create a new object from the class to start using it.

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

we’ll write a function that will act as our event listener, then we can use EventEmitters on method to set the listener.

```
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function userJoined(username){
  // Assuming we already have a function to alert all users.
  alertAllUsers('User ' + username + ' has joined the chat.');
}

// Run the userJoined function when a 'userJoined' event is triggered.
chatRoomEvents.on('userJoined', userJoined);
```


he next step would be to make sure that our chat room triggers a userJoined event whenever someone logs in so that our event handler is called. EventEmitter has an emit method that we we use to trigger the event. We would want to trigger this event from within a login function inside of our chatroom module. 

```
function login(username){
  chatRoomEvents.emit('userJoined', username);
}
```
[Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)

[Node docs: events](https://nodejs.org/api/events.html)

