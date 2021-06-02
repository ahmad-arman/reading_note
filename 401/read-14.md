

## What’s the difference between a FIFO and a standard queue?
Standard queues guarantee that a message is delivered at least once and duplicates can be introduced into the queue. FIFO queues ensure a message is delivered exactly once and remains available until a consumer processes and deletes it; duplicates are not introduced into the queue.
## How can the server be assured a message was properly received?
by use expecting to receive an event from the client that the massaged received by it
## What classic design pattern is best represented by event driven programming?
Event , Singleton
## How do you test an event driven system?
test event emit and listen it

#  Terms 

* FIFO Queue : first in first out as array the value first input and this value out from queue first 

* Pub/Sub : is an asynchronous messaging service that decouples services that produce events from services that process events.

# Preparation Materials 
* SNS : is a distributed publish-subscribe service.
* SQS : is distributed queuing service.

[AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

