### Why is the Context API useful?

The React Context API is a way for a React app to effectively produce global variables that can be passed around. This is the alternative to "prop drilling" or moving props from grandparent to child to parent, and so on. Context is also touted as an easier, lighter approach to state management using Redux


### Can a component outside of a provider get its context?

No need for Context. Provider . This is multiple contexts being used in one component, requiring just two calls to useContext versus wrapping your entire application in two nested contexts, which is what is what you have to do with current Context.



### What are some common use cases for using the Context API?

 Context is primarily used when some data needs to be accessible by many components at different nesting levels. Apply it sparingly because it makes component reuse more difficult. If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

### Describe “Context Hell” 

 Like the callback hell, usual when jQuery was used for everything, the React Context hell is the nasty code you get taking advantage of the React Context API


## Term 

* global state :a global state is a set of local states which are all concurrent with each other. ... A global state in the time domain is also a global state in the causal domain; if two states occur simultaneously, then they cannot have any cause-effect relationship 

* global context : This global context is not just about studying the time and place of an event. It also means looking at how the event has made an impact on personal as well as global history.

* provider :
The `<Provider>` component makes the Redux store available to any nested components that need to access the Redux store. Since any React component in a React Redux app can be connected to the store, most applications will render a` <Provider>` at the top level, with the entire app's component tree inside of it.

* consumer : A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component. Requires a function as a child. The function receives the current context value and returns a React node.



## what is role based access control? 

Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

## EXAMPLES OF ROLE-BASED ACCESS CONTROL

Through RBAC, you can control what end-users can do at both broad and granular levels. You can designate whether the user is an administrator, a specialist user, or an end-user, and align roles and access permissions with your employees’ positions in the organization. Permissions are allocated only with enough access as needed for employees to do their jobs.

#### Some of the designations in an RBAC tool can include:

* Management role scope – it limits what objects the role group is allowed to manage.
* Management role group – you can add and remove members.
* Management role – these are the types of tasks that can be performed by a specific role group.
* Management role assignment – this links a role to a role group.

#### BENEFITS OF RBAC 

1- Reducing administrative work and IT support. 

2-Maximizing operational efficiency.

3-Improving compliance.


#### BEST PRACTICES FOR IMPLEMENTING RBAC
* Current Status 
* Continually Adapt
* Make Changes
* Write a Policy
*  Current Roles



### REFERENCE 

* [what is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)

* [react-cookies component](https://www.npmjs.com/package/react-cookies)

* [react-cookie library](https://www.npmjs.com/package/react-cookie)


