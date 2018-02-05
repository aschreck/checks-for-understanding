## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's one difference between ES5 and ES6?
  ES6 introduces a number of syntactic features. It introduced, const and let as opposed to var, fat arrow syntax over traditional function definitions, and created class constructors.
2. What's the difference between asynchronous and synchronous JavaScript?
  Synchronous JavaScript functions in an absolutely single-threaded manner, meaning that each code process accumulates on the stack in a linear order and must be resolved sequentially, even if a function makes requests that are blocking and require the program to wait. In the browser, JavaScript uses a browser engine to replicate multi-threaded behavior by placing functions that make an external request to an API onto the stack through an additional channel. This allows JavaScript to execute other things while fetch requests etc are made.
3. What are the four pillars of Object Oriented programming?
  Abstraction: We abstract methods into small pieces of functionality that can be easily tested to verify their functionality. We then use these abstracted pieces within other functions to abstract way the complexity of various pieces of our code.
  Encapsulation: encapsulation refers to the coupling of functionality and data storage within single objects. We store data within methods and also dictate behavior for that data.
  Polymorphism: Creating methods that appear to do the same thing to different pieces of data, but actually do very different things on the good. For example, .length on strings and .length on arrays.
  Inheritance: We can create hierarchies of inheritance that allow us to build only the exact functionality that we want in each object while not repeating ourselves.
4. What are some tools available in JavaScript to help you write object oriented code?
  We can use constructors and prototypes to write this code. Constructors allow us to create objects with various properties, and prototypes allow us to pass along functionality without the data bloat of storing behavior on individual objects.
5. What are some key concepts to be aware of when refactoring your JavaScript?
  Method length, duplicate code, complex conditional logic, long parameters, obscuring comments.
6. What's a callback function and what are some reasons when we use/need callback functions?
  Callback functions are functions that are passed into other functions as arguments. This is possible because functions are first-class objects in JavaScript.
7. What are the different scopes of variables in Javascript? When would you want to define global variables?
  var is a variable that is available in the scope it is defined. Originally, javascript did not support block scoping, so a var defined in a block would be available outside of that block. Let is a variables that is block scoped. Const is a var that cannot be changed.
8. What's the difference between `==` and `===` in JavaScript?
  they are loose and strict equality, respectively. JavaScript will attempt to coerce datatypes into something common to compare things, such as if we were to compare 2 and "2". Strict equality does not allow for that coercion.
9. Why do front end frameworks exist?
  These exist to provide us with ways to organize our files.
10. Why do people say "HTTP is stateless"?
  HTTP requests are made and exist without any reference to any other HTTP requests. Once a connection is broken between two computers, unless any changes have persisted to their databases as a result of the request, it is as though nothing happened—on its own, HTTP does not allow computers to remember that they have talked to each other before. This problem is solved by cookies and sessions.
#### Review

11. Describe a RESTful API.
  a Restful API has endpoints that are based upon the CRUD (Create Read Update Destroy) model. It has 7 fundamental routes that are reached through the verbs Get, Post, Patch, Put, Delete. The purpose of Rest is to create a standardized architecture for the construction of APIs
12. What are some main characteristics of a team following an agile workflow?
  Agile teams focus on short sprints followed by a retrospective reassessment. The purpose of this model is to make a team more responsive to changes in the set of available information about their problem, or changes in the customers' desires. The alternative is the Waterfall method, where the project moves in singlular monolithic stages.
13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
  Advantages: OAuth providers generally have better security. It is easier than dealing with your own.
  Disadvantages: Your users must have the account of your Oauth provider. You lose control over the process. Your app is now tied to that service's existence.
