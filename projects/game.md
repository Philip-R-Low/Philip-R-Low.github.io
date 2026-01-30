---
layout: project
type: project
image: img/game/Python-logo.png
title: "CSci 121 Final Project"
date: 2022
published: true
labels:
  - Python
summary: "A text adventure game that I developed for CSci 121."
---

My first proper computer science course was at Reed University in the Spring of 2022. The course was an introduction to the basics of programming and taught in Python. The class’s final project, to test our skills at Object Oriented Programming, was to create a game. We were given some starter code that had basic classes for Rooms, Enemies, the Player character, and a main game loop printing actions into the console like old school text based adventures. We were then given a list of possible mechanics to implement with a score value based on how hard they expected implementation to be. However, to encourage creativity and go beyond base expectations, we were also allowed to come up with our own features for points provided we justified why we thought they were hard enough to warrant the score. I admit I don’t remember nor have the ability to find what the final point value was attributed to an A on the project, but I believe it was somewhere between 25 and 40. Working by myself for a month, I finished with a point value of 51.

<img height="200px" src="../img/game/dcss_logo.png">

I did stick to the text based gameplay, but my inspirations drew from elsewhere. My primary influence was a little open source Rouge-like game called [Dungeon Crawl Stone Soup](https://crawl.develz.org/). Admittedly my final game was not nearly as deep, nor played in a similar manner as DCSS, but the game inspired me to change the game world from the four static rooms of the starter code into a series of mazes connected by staircases. Programing the maze generation, despite being worth a measly 3 points for randomizing the world, was one of the features I was most proud of. This is because I had no idea how to generate mazes when I started, but with a day of work and the [wikipedia page on maze generation](https://en.wikipedia.org/wiki/Maze_generation_algorithm), I had a maze… that I had no way to see how to solve. So I spent another few hours figuring out how to create a key word the player could use to look at a map. This task I recall as being a lot harder than anticipated, but in the end I could appreciate my new map.

According to the final write up I did for the assignment, one of the features I was most proud of was making a way for the player to cast magic spells in the game. I had to add a key word for the player to see the list of spells they had access to, and a key word for casting spells as well. The casting keyword I recall being finicky to program because the player then had to input the name of the spell, which could be multiple words, which was inconvenient when the command parser split commands up per word. If I recall correctly, about half of the spells were damage spells that not so secretly were re-flavorings of other damage spells just of a different “element”. I believe my primary inspiration for the spells came from The Elder Scrolls V: Skyrim.
	Currently I cannot provide the source code for my game because the computer I created it on broke, and my relationship with cloud storage is antagonistic. If I can track down this code I will create a github project for it and link to it.
