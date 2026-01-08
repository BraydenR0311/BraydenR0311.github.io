---
title: "Food for Thought"
excerpt: "Expanding my programming skills through PyGame."
coverImage: "/assets/blog/pysms/cover.jpg"
date: "2025-01-08"
author:
  name: Brayden Riesberg
  picture: "/assets/blog/authors/brayden.jpg"
ogImage:
  url: "/assets/blog/pysms/cover.jpg"
---

## The Idea

Sometime during the fall of 2024, I was biking home from work, and I came up with an idea for a project to work on. It would be a game called "Food for Thought". I wanted to use PyGame, which is a Python library used to make games.

I'm a data scientist at CERL for the _U.S. Army Corps of Engineers_, and a lot of my work is done in Python. Python was pretty much the first programming language I decided to take a deep dive into, and I had been familiar with third-party libraries like Pandas, PyTorch, Matplotlib, etc.

One day, I happened upon a library called PyGame. It's essentially an SDL2 wrapper which exposes convenient functions for drawing things onto windows, moving things around, and handling user input. I became obsessed with this library and dove into its documentation.

Admitedly, I didn't understand much of what was going on. See, I was still in my undergrad when I discovered PyGame and was still learning the ropes of Python and object-oriented programming in general. For a game design class, I used PyGame to create a game called _Mr.Bear's Tavern_. It was really cute, and I was proud of what I'd built. I'd even created a little card game about goblins which was the central aspect of the game. But the code was pure spaghetti and it became really hard to extend. I wasn't making use of PyGame's central Sprite class and everything was purely functional and highly coupled. Very poorly organized. But, it was a great learning experience!

Since graduating, I haven't stopped trying to upskill and learn new programming languages and concepts. At the time of writing, I quite literally study programming and CS/DS concepts every day, at work and at home. When I'm not burned out from work, I try working on projects that I hope demonstrate my passion and dedication to building things and reverse engineering complex systems.

## Learning

When I started this new project, I created a game design document and outline some important aspects of this game. First, that it would be called _Food for Thought_ because it would be a typing game where the user types out philosophers' quotes to cook food.

I cooked up some simple assets using Inkscape and then got to work on the code. I picked up a book from O'Reilly called _Object-Oriented Python_ and read through it. I'd been exposed to OO concepts like inheritance, encapsulation, and polymorphism before, but I was having a lot of trouble. Let me tell you, this book helped, especially since it uses PyGame as a way of explaning OO.

When reading PyTorch code at work, I'd seen classes inheriting from `nn.module` and didn't fully understand what was going on. Much like PyTorch with its `nn.module`, PyGame gives the user a `pg.sprite.Sprite` class to inherit from. It took a while, but I eventually filled those gaps in my understanding.

## The Process

I make it a top-down tile-based game kind of like how the game _Overcooked_ looks. I also drew a lot of inspiration from a Youtuber called Goodgis and from a [video](https://www.youtube.com/watch?v=H09PmP5tsy8) he made. Studying his game's repo helped me understand how to organize and structure my game's components.

Most of the time I was making this game, I didn't have a plan. I was just doing it as I went. I mean, it was just I side project I did for fun. I built entire facets of the game that I would eventually end up throwing out. Like an inventory system I made where the user would pull from a limited amount of ingredients and use those to cook.

This went on and on for a really long time. I was also busy with other stuff at the time, like some additional math classes I decided to take after graduating (only cause work paid for it), and trying to enjoy life when I wasn't grinding. But, after trying things out, tinkering, and messing around, I eventually grew bored and made a point to get this game to a "playable" state. The source can be checked out [here](https://github.com/BraydenR0311/foodForThought) on my github!
