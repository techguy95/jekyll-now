---
layout: post
title: Fleshing out a Dungeon Crawler!
---

After figuring out how to get an old school dikuMUD up and running on a Google Cloud Ubuntu 17.04 (Zesty Z)
Continuing the saga of the [Learn Teach Code](http://learnteachcode.org/) UnBootcamp experiment.

## Today I learned (#TIL):

- How to quickly scrum and brainstorm in a collaborative manner to forge a project through "Mob Coding"
- How to wireframe a project by sketching out on paper
- We made the first room of our dungeon and uploaded the project to GitHub here: [https://github.com/r7uaz0n/the-great-escape](https://github.com/r7uaz0n/the-great-escape)
- If you would like to play the game, click [The Great Escape!](https://dungeon-learn-teach-code.herokuapp.com/)
- Feel free to fork this project and make it more interesting!

## Questions:

-
-

## Bugs discovered / what I got stuck on:

- The GitHub project I cloned earlier did not compile correctly because of an antiquated library dependency from an ancient UNIX/VAX C code base
- I discovered that the C program used an sqlite package to store user sessions for their equipment, stats, inventory, experience/level, player description and more
- This means I'll definitely need to learn some database, SQL and json for my text based dungeon crawler pet project


## Useful links to save for later:

-


## My next goals:

- Find a modern linux distro version of dikuMUD code that will compile on a Google cloud Ubuntu 17.04 (Zesty Zapus) instance.
- Once the code runs, examine the structure and guts of the code to help me envision, architect and code a new version of a this dungeon crawler in node.js
