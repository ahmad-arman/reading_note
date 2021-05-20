
## What is a Linked List
 A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

 There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.

## Terminology
 Head - The Head is a reference of type Node to the first node in a linked list.<br>
 Linked List - A data structure that contains nodes that links/points to the next node in the list.<br>
 Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.<br>
 Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.<br>
  Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.<br>
 Next - Each node contains a property called Next. This property contains the reference to the next node.<br>


 
## Memory management
 The biggest differentiator between arrays and linked lists is the way that they use memory in our machines. Those of us who work with dynamically typed languages like Ruby, JavaScript, or Python don’t have to think about how much memory an array uses when we write our code on a day to day basis because there are several layers of abstraction that end up with us not having to worry about memory allocation at all.

 But that doesn’t mean that memory allocation isn’t happening! Abstraction isn’t magic, it’s just the simplicity of hiding away things that you don’t need to see or deal with all of the time. Even if we don’t have to think about memory allocation when we write code, if we want to truly understand what’s going on in a linked list and what makes it powerful, we have to get down to the rudimentary level.

## Hey, so, what even is Big O?
 Most of us have probably heard the term “Big O Notation”, even if we had no idea what it meant the first time that we heard someone use it. My personal experience with it has always been in the context of designing algorithms (or being asked to evaluate the efficiency of an algorithm). But Big O is really all over and omnipresent within computer science.

 The reason for this is that computer science — and effectively, anything that we code — is all about efficiency and tradeoffs. Whether you’re building software as a service, choosing a front end framework, or just trying to make your code DRY and more elegant, that’s what all of us are striving towards: being efficient with our software, and choosing things that are important to what we’re building, all while being aware of the tradeoffs that we’ll ultimately have to make.


## Traversal
When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. 

[REFERENCE-One](path)

[REFERENCE-One](path)

[REFERENCE-One](path)

[REFERENCE-One](path)