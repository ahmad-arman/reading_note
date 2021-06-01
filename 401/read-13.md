## What does it mean that web sockets are bidirectional?

  It means that the data flows in both ways (full-duplex), a web socket can both send and receive which is useful because it allows data to be sent and received on the same channel. 
 ## Why is this useful?
## Does socket.io use HTTP? Why? 
Yes, it use HTTP. Socket.io will try to establish a WebSocket if possible but if it cannot it will fall back on HTTP.
## What happens when a client emits an event?
Whenever server is emitting an event it will be send to all client’s socket connected and listen to it.
## What happens when a server emits an event?

The socket that miss an event won’t recognize it later and it will be ignored.
## What happens if a client “misses” an event?
## How can we mitigate this?

To avoid missing an event by caching the events on the server and when the client recive the event it will emit an event to the server, so that the server will awknowladge the client got the message and the server will remove the event from the chach. And every time the client start a connection with the server he will emit an event to get the events that he missed.

# Terms 

 * Socket :  is one endpoint of a two-way communication link between two programs running on the network. A socket is bound to a port number so that the TCP layer can identify the application that data is destined to be sent to. An endpoint is a combination of an IP address and a port number.
 * Web Socket : specification defines an API establishing “socket” connections between a web browser and a server. In plain words: there is a persistent connection between the client and the server and both parties can start sending data at any time
 * Socket.io :  Communication protocol that provides a full-duplex and low-latency channel between the server and the browser.
 * Client :  It is a library that enables real-time, bidirectional, and event-based communication between the browser and the server, consists of a Node.js server and a javascript client library for the browser.
 * Server
 * OSI Model : The Open Systems Interconnection model is a conceptual model that characterizes and standardizes the communication functions of a telecommunication or computing system without regard to its underlying internal structure and technology.
 * TCP Model :Transmission control protocol, essentially a concise version of the OSI model .
 * TCP :  The Transmission Control Protocol (TCP) is a transport protocol that is used on top of IP to ensure reliable transmission of packets


 * UDP :User Datagram Protocol: is a communications protocol that is primarily used for establishing low-latency and loss-tolerating connections between applications on the internet. It speeds up transmissions by enabling the transfer of data before an agreement is provided by the receiving party.

[REFERENCE-One](path)

[REFERENCE-One](path)

[REFERENCE-One](path)

[REFERENCE-One](path)