## Week One - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR.

1. What's the most useful thing you learned from completing the intermission week work?
  I read most of Eloquent Javascript and did part of Wes Bos' JavaScript30 and that was pretty cool
2. What are some tools to help debug JavaScript code?
  We can use debugger, console log various things, use the source tab to see definitions of variables and our code file, and set breakpoints from the dev tools menu.
3. What are some tools you need in order to unit test your JavaScript?
  Mocha and Chai
4. What is the syntax for invoking a function? Give an example.
  var itsAFunction = function(args) { stuff happening(args)}

  itsAFunction()
5. What's `this` in JavaScript?
  Everything in JavaScript is an object, more or less, and This refers to the specific object you're inside.
6. What is Webpack and why is it useful?
  Webpack is like the Asset Pipeline in Rails. It minifies our javascript and CSS and concatenates them into a single file. It also provides us with a server that watches changes to our files.
7. When/why do you want to use event delegation?
  When the element that we want to watch has a variable quantity (checkboxes on a todo list of variable length, etc), it makes more sense to set a single event listener on some container on top
  of that variable number of things we're interested in, and capturethe event through event bubbling, event.target, and event.currentTarget.
8. What's `npm` and what do we use it for?
  Node Packet Manager. Managing Node Packets. Similar to Gemfile. Holds packages we want in our program.

#### Review
9. What's the MVC design pattern? Describe each part of MVC.
  Model: Objects that serve as a bridge between SQL database rows and our program.
  View: The thing that appears on the screen.Receives the data from models by way of our controllers, which package that information specifically for different views.
  Controller: Controllers handle HTTP requests. These requests are routed to different actions on a controller based on defined Routes.
10. What are a few ways to optimize a Rails application?
  Use caching, make sure the application is making an optimal number of queries. Use background workers.
11. What's a background worker? When would we want to use a background worker?
  A background worker is a process that allows our application to perform tasks for specific users without requiring them to remain on the page until the action completes. These jobs go to a queue and are finished as time allows while the user is free to do other things.

