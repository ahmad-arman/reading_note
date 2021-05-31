
## What is the benefit of transforming data into packets? 

It allows data to be transferred fast and efficiently over the network and to minimizes the transmission latency 

## UDP is often refereed to as a connectionless protocol. Why is this?

Because it’s helps to make the connection between to parts before the data transmission

## Can a socket server application have multiple socket connections? 
 yes

## Can a socket connection application be connected to multiple socket servers? 
No, a single client-side server should only connect to one socket server.

## Can an application be both a socket server and a socket connection?

Yes an application can be both a socket server and a socket connection

## Terms 

* Observer Pattern :  The observer pattern is a software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. The observer pattern defines a one-to-many relationship.
<br>

* Listener : It is a function that listens for an event to occur. <br>
* Event Handler : Is a function that runs when a specific event fires. <br>
* Event-Driven Programming :  is a programming paradigm in which the flow of program execution is determined by events - for example a user action such as a mouse click, key press, or a message from the operating system or another program. ... Virtually all object-oriented and visual languages support event-driven programming. <br>

* The event loop  : is continuously checks the call stack to see if there's any function that needs to run. While doing so, it adds any function call it finds to the call stack and executes each one in order.
<br>

* Event Queue :  A queue where events from an application are held prior to being processed by a receiving program or system .

* Call Stack: A Stack for an interpreter to store and track of its place in a script that calls multiple functions - what function is currently being run and what functions are called from within that function. <br>

* Emit/Raise/Trigger: In event-driven programming, emit sends a message to trigger a response and raise an event <br>

* Subscribe: Listening to an event to take place. 

* Database: is a data structure that stores organized information. 

## Websocket 
communication Protocol that provides bidirectional communication between the Client and the Server over a TCP connection; WebSocket remains open all the time, so they allow real-time data transfer. 

## Socket.IO : 
  * It is the library to work with WebSocket
 * Provides the event-based communication between  browser and server.
 * A connection can be established in the presence of    
   proxies and load balancers.

# REFERENCE

[OSI Model Explained](https://www.youtube.com/watch?v=vv4y_uOneC0) <br>

[TCP Handshakes Explained](https://www.youtube.com/watch?v=xMtP5ZB3wSk)<br>



[Web Sockets](https://en.wikipedia.org/wiki/WebSocket)
[Socket.io Tutorial](https://www.tutorialspoint.com/socket.io/)<br>
[Socket.io vs Web Sockets](https://www.educba.com/websocket-vs-socket-io/)<br>

[Socket.io Documentation](https://socket.io/docs/v4/index.html)<br>
[Socket.io Server API](https://socket.io/docs/v3/server-api/index.html)<br>
[Socket.io Client API](https://socket.io/docs/v3/client-api/index.html)<br>
[Socket Testing Tool](https://amritb.github.io/socketio-client-tool/)<br>

