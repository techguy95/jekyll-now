---
layout: post
title: May the Force be with you!
---

The Force works in mysterious ways...and so does JavaScript!
Let's take a look at how we setup a realtime chatroom webapp
using Express, Node.js, WebSocket and Socket.io! [https://chat-learn-teach-code.herokuapp.com/](https://chat-learn-teach-code.herokuapp.com/).
Another tale of the [Learn Teach Code](http://learnteachcode.org/) UnBootcamp experiment.

## Today I learned (#TIL):

- As a warmup, we started to build a very simple calculator app. You can see our code in this CodePen here\: [http://codepen.io/LearnTeachCode/pen/xddbxx](http://codepen.io/LearnTeachCode/pen/xddbxx)
- We learned about SocketIO and WebSocket for real-time communication between server and clients, and we made a basic chatroom app!
- All the working code for the chatroom app is here\: [https://github.com/LearnTeachCode/socketio-chat-demo/](https://github.com/LearnTeachCode/socketio-chat-demo/)
- Learned how to integrate the event loop with a callback function and how scope of variables need to follow the trigger and action flow


## Questions:

-
-

## Bugs discovered / what I got stuck on:

- I had help with my first experience debugging a simple javascript game by sprinkling console.log statements on a piece of code
- I had forgotten how the callback function worked, so Allen and Liz gave me some clues on what to focus on
- The clue was that the user input in a number guessing game was not being passed into an if then else evaluation properly
- I then realized that the problem was that the scope of the input variable was global and not local to callback function when a button is clicked
- In this case, the user's input was typing a number into the box, then comparing that number to a random number AFTER clicking "submit"
- To see what I mean check out this codepen that I worked on with Liz and Allen mentoring me\: [https://codepen.io/Argentus/pen/xdrPOj](https://codepen.io/Argentus/pen/xdrPOj)
- I modified the game a bit to display what the random number was and the user's input to verify the game was working correctly
- Black box testing!  Focusing on input, comparing expected/actual output even without understanding the details of how it works
- In QA terminology, we had run unit and acceptance testing and used the results to deduct what part of the code was not working
- Then using what we had learned earlier I was able to recall what Liz had graciously highlighted and taught us in our Saturday class


## Useful links to save for later:

- [https://discuss.codecademy.com/c/javascript](https://discuss.codecademy.com/c/javascript)


## My next goals:

- Daily blog post so that I don't forget small sparks of learning or creative ideas
