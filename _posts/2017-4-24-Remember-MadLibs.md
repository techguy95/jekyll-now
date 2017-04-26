---
layout: post
title: They want EFX!
---

Check out how we learned how to throw up a simple website using javascript to run a MadLibs game!
Another exciting chapter in the blogosphere of the [Learn Teach Code](http://learnteachcode.org/) UnBootcamp experiment!

## Today I learned (#TIL):

- How to call javascript files and libraries in the HTML document - in our MadLibs site, it was index.html
- Point to an external javascript file (just insert script includes at the bottom of the DOM https://www.w3schools.com/js/js_htmldom.asp):
{% highlight javascript %}
<!-- bring in local javascript file below -->
<script src="myscripts.js"></script>
<!-- bring in the socket.io library in the next line //think about bootstrap/angular/react/{next.agile.library} -->
<script type="text/javascript" src="socket.io.js"></script>
<!-- bring in jQuery library below...props to the LearnTeachCode crew for all the help! -->
<script src="jquery-x.x.x.min.js"></script>
{% endhighlight %}

- I uploaded the MadLibs site to my GitHub account here: https://techguy95.github.io/madlibs
- The code we mob programmed in class was on my laptop so I made a new GitHub repo for this lesson using this guide https://help.github.com/articles/create-a-repo/
- Later when I started working on the desktop "rig" at the crib I pulled down the code that I uploaded to the GitHub repo from my laptop using this guide https://help.github.com/articles/cloning-a-repository/
- I almost forgot to mention something wonderful I learned in the class was about event based programming, aka "THE event loop".
- You can kick off scripts through interactive user input(s) - also thinking of possibilities of other libraries
- OK! Let's take a look at our javascript running an event-based MadLibs program!
{% highlight javascript %}
function showMadLib()
  {
      // Get the values of HTML input boxes
      // with the IDs "noun", "verb", and "adjective"
      var noun = document.getElementById('noun').value;
      var verb = document.getElementById('verb').value;
      var adjective = document.getElementById('adjective').value;
      // For testing purposes, display the values in the console
      console.log(noun, verb, adjective);

      // Make the madlib and save it to a variable
      var madLib = createMadLib(noun, verb, adjective);
      console.log(madLib);

      // Make a JavaScript object for the HTML element with id "madlib"
      document.getElementById("madlib").textContent = madLib

  }

function createMadLib(noun, verb, adjective)
  {
      return ("Vincent " + verb + " the " + noun + " while running away from the " + adjective + " person!");
  }

var submit = document.getElementById("submit");
submit.addEventListener('click', showMadLib);

  //test createMadLib function
  //createMadLib("dog", "spanked", "weird");
{% endhighlight %}

## Questions:

- How can I permanently store user or session data from a signup form on a website using javascript (node.js? hmm)?
- Curious about FireBase...  I keep hearing about FireBase and i'm fired up!  Let me read up more about it here https://firebase.google.com
- need to hyperlink stuff in Jekyll

## Bugs discovered / what I got stuck on:

- the missing link: calling javascript & libraries through html (#TIL)
- trying to comprehend and visualize when you would need to use literal or constructor notation for objects

## Useful links to save for later:

- https://medium.freecodecamp.com/stanford-just-abandoned-java-in-favor-of-javascript-for-its-intro-cs-course-fe40543e81d8
- https://code.tutsplus.com/tutorials/event-based-programming-what-async-has-over-sync--net-30027
- https://medium.freecodecamp.com/getting-your-first-developer-job-whats-the-best-way-1737d0bcba7a

## My next goals:

- 15 minutes of blogging and coding per day...
- Finish the Codecademy tutorial
- Tactfully manage distraction barriers
- Take advantage of opportunities for networking, meditation and brainstorming
- Start reading the free book Eloquent JavaScript. Chapter 1: http://eloquentjavascript.net/01_values.html and if you like it, go on to Chapter 2: http://eloquentjavascript.net/02_program_structure.html and do the practice problems at the end of that chapter!

## Thoughts to share
- Regarding coding...consistency is the key.
- Coding projects require planning, collaboration and ownership of deliverables - The approach of our coding group!  Learn Teach Code...
