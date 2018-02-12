## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. At a high level, what is Node?
  Node is a runtime for JavaScript that borrows the V8 engine from Chrome to allow JS to function and maintain it's asynchronous, pseudo-multithreaded behavior in a backend context.
2. What is Express? What is Express similar to in the Ruby world?
  Express is a backend framework for web applications. It resembles Rails in that it provides an apparatus for interfacing with a database and receiving HTTP requests.
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

  Having required the router from express and required a uri in the app.js file, you call a method that is synonymous with the desired HTTP verb off of the router, i.e. :

    router.get('/foods', foodsController.index);

    The method called on the router determines the verb. The first argument of the function is the route relative to the URI specified in the app.js file, and the second argument is a handler for that request. Although Express is an unopinionated framework, one possible organizational pattern is to take the MVC approach from (not exclusively) Rails. The router calls a method on a controller module which uses a model module to manipulate the database.


4. What do we use Knex for?
    Knex is a library for building SQL queries. Similar to Active Record, Knex allows developers to make database queries more easily than would typically be the case in raw SQL.
5. How **could** you organize your code to follow the MVC design pattern in your Quantified Self project?
  Like Rails, we could choose to structure our code following an MVC pattern, where a 'model' module contains functions that query the database, and a controller module the functions of which you call as handlers in routers.
6. How do you execute raw SQL in node?
  require a database in a file and then use database.raw("SELECT answers FROM questions")
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
  Advantages: It's kind of like SRP for your code bases. Your backend can focus all of its effort on creating API endpoints and your Frontend can be exclusively devoted to displaying things, making fetch calls, and running JS files. Further, it makes your app more changeable. If (as seems to be the case currently), your frontend ceases to be hot and desirable, you can build a new one and set it ontop of the same backend endpoints rather than having to disentangle the views from the app.

  Disadvantages: You have to keep track of and maintain two different repositories, and two different apps in production. It's sometimes not immediately obvious where a problem is occurring.

#### Review

8. Describe DNS.
  When neither the OS nor the browser have an IP address for a URL, it sends a request to the DNS, which holds a registry of URLs indexed to IP addresses. It looks this up and sends it back to the client.
9. What does writing clean code mean to you?
  In my opinion this means code that is 1) easy to change and 2) easy to understand. For this reason, sometimes I resist extensive refactors because I personally find code easier to understand when it is all in one place. If a method is being used in multiple places, this is of course not the best approach.
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality? Hint: think about what tables you would need in the database, how those records would relate to each other, and good OOP.
  A hotel has_many employees, guests, rooms, reservations.
  A guest has_many reservations.
  A reservation has_one room.
