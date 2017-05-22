---
layout: post
title: They want EFX!
---

Check out how we learned to deploy a simple website on Heroku using event-based javascript to run a
MadLibs game.  [https://madlibs-learn-teach-code.herokuapp.com/](https://madlibs-learn-teach-code.herokuapp.com/)
Another exciting chapter in the blogosphere of the [Learn Teach Code](http://learnteachcode.org/) UnBootcamp experiment!

## Today I learned (#TIL):

- Whaaaaaat I was excited to deploy the MadLibs website using a little php/json hack found here: [Deploy a static website to Heroku](https://gist.github.com/wh1tney/2ad13aa5fbdd83f6a489)
- Also don't forget to use the Heroku CLI to create the PHP buildpack with this command:
{% highlight javascript %}
heroku create --buildpack https://github.com/heroku/heroku-buildpack-php.git
{% endhighlight %}
- How to call javascript files and libraries in the HTML document - in our MadLibs site, it was index.html
- Point to an external javascript file (just insert script includes at the bottom of the DOM examples below - https://www.w3schools.com/js/js_htmldom.asp):
{% highlight javascript %}
<!-- bring in local javascript file below -->
<script src="madlibs.js"></script>
<!-- bring in the socket.io library in the next line //think about bootstrap/angular/react/{next.agile.library} -->
<script type="text/javascript" src="socket.io.js"></script>
<!-- bring in jQuery library below...props to the LearnTeachCode crew for all the help! -->
<script src="jquery-x.x.x.min.js"></script>
{% endhighlight %}

- I uploaded this MadLibs website to my GitHub account here: [https://techguy95.github.io/madlibs](https://techguy95.github.io/madlibs)
- The code we mob programmed in class was on my laptop so I made a new GitHub repo for this lesson using this guide:
[Creating a Repository on GitHub](https://help.github.com/articles/create-a-repo/)
- Later when I started working on the desktop "rig" at the crib I pulled down the code that I uploaded to the GitHub repo from my laptop using this guide:
[Cloning a Repository on GitHub](https://help.github.com/articles/cloning-a-repository/)
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
- the key elements where we grab and render the HTML in our javascript:
{% highlight javascript %}
document.getElementById('object/variable').value;
//used for inputs e.g. forms - remember value is used for inputs - interesting background story why "value" is used
document.getElementById("object/variable").textContent;
//grab n change the text content - generate the HTML here
{% endhighlight %}

## Questions:

- How can I permanently store user or session data from a signup form on a website using javascript (node.js? hmm)?
- Curious about FireBase...  I keep hearing about FireBase and i'm fired up!  Let me read up more about it here [https://firebase.google.com](https://firebase.google.com)
- need to hyperlink stuff in Jekyll

## Bugs discovered / what I got stuck on:

- the missing link: calling javascript & libraries through html (#TIL)
- trying to comprehend and visualize when you would need to use literal or constructor notation for objects

## Useful links to save for later:

- [https://medium.freecodecamp.com/stanford-just-abandoned-java-in-favor-of-javascript-for-its-intro-cs-course](https://medium.freecodecamp.com/stanford-just-abandoned-java-in-favor-of-javascript-for-its-intro-cs-course)
- [https://code.tutsplus.com/tutorials/event-based-programming-what-async-has-over-sync--net-30027](https://code.tutsplus.com/tutorials/event-based-programming-what-async-has-over-sync--net-30027)
- [https://medium.freecodecamp.com/getting-your-first-developer-job-whats-the-best-way-1737d0bcba7a](https://medium.freecodecamp.com/getting-your-first-developer-job-whats-the-best-way-1737d0bcba7a)

## My next goals:

- 15 minutes of blogging and coding per day...
- Finish the Codecademy tutorial
- Tactfully manage distraction barriers
- Take advantage of opportunities for networking, meditation and brainstorming
- Start reading the free book [Eloquent JavaScript](http://eloquentjavascript.net/).
- [Chapter 1](http://eloquentjavascript.net/01_values.html): and if you like it, go on to
- [Chapter 2](http://eloquentjavascript.net/02_program_structure.html): and do the practice problems at the end of that chapter!
- Pick ONE of the following built-in JavaScript string functions look it up online and read about it, and then write one of your blog posts explaining what it does and why it’s useful.
- Write at least 3 short code examples of your own that show how to use it, and include the same code on your blog.
- (Bonus: format your code examples with syntax highlighting, following [GitHub’s Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet):
- Built-in JavaScript string functions to choose from (just choose ONE of these): indexOf(), slice(), substring(), charAt(), replace(), toUpperCase(), split()
- [Extra practice problems - Codewars Kata Tricky Doubles!](https://www.codewars.com/kata/tricky-doubles)
- Watch [“The Poetry of Programming”](https://www.youtube.com/watch?v=-jRREn6ifEQ) talk by Linda Liukas

## Thoughts to share:
- Regarding coding...consistency is the key.  Never surrender! (This is a theme of season veterans of Learn Teach Code - shout out to Allen and Vincent for this one)
- Coding projects require planning, collaboration and ownership of deliverables - The approach of our coding group!  Learn Teach Code...
