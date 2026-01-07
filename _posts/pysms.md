---
title: "PySMS"
excerpt: "Coming up with a Python library with civil engineering utilities for data scientists and engineers."
coverImage: "/assets/blog/pysms/cover.jpg"
date: "2025-01-06"
author:
  name: Brayden Riesberg
  picture: "/assets/blog/authors/brayden.jpg"
ogImage:
  url: "/assets/blog/pysms/cover.jpg"
---

I'm in Python pretty much all day every day, and since I work with mathematicians, it also happens to be their go-to. Its dynamic, interactive nature lets us rapidly write code that actualizes the research done by our senior engineers. Not to mention, it gets first-class attention from the ML/AI community so all the latest PyTorch models and pretty much all cutting edge research makes its way to Python first.

## Inception

---

I began to notice a pattern among the number of projects we've been working on. We were constantly rewriting the same utility functions, creating a fair amount of code duplication.

A large chunk of our work revolves around facility degredation simulation, which itself revolves around one particular statistical model: [the Weibull Curve](<https://doi.org/10.1061/40799(213)4>) (seen below).

![Weibull Curve](/assets/blog/pysms/curve.png)

Take for example, this set of PyTorch calculation functions authored by one of our mathematicians for a facility optimization project:

![Pytorch functions](/assets/blog/pysms/funcs.png)

Don't worry if its not obvious what these functions do. The bottom line is that these same calculations have been written a number of times, scattered across jupyter notebooks and even written in languages like C# and R (As an aside, the top function actually draws out the above curve when given specific alpha and beta parameters: 2.64 and 1.0, respectively).

At some point late summer 2025, I thought it'd be nice if we had a place to put these common utilities. That way, we had one source of truth so we could create some thorough documentation and unit test the hell out of the code. So, I asked around if anyone thought it was remotely a good idea and not just a waste of time and precious taxpayer dollars. They were all onboard and thus, the PySMS repository was born.

## Design

Throughout the project, I've tried to draw design inspiration from popular Python repos (ie. [Requests](https://docs.python-requests.org/), [Scikit-Learn](https://scikit-learn.org/), [Seaborn](https://seaborn.pydata.org/)). Whether its the API, unit tests, CLI, or even the documentation, I wanted my project to follow some tried and true design patterns.

At a high-level, I've separated the library into two sections: the functional API and the Object-oriented API. The functional API exposes the program similar to those functions from earlier. The Object-oriented approach is a bit more complex and has certainly pushed my software engineering skills.

E-SMS manages DoD real property through a heirarchical categorization system. Organizations (ie. DoD, Army, Air Force) contain Installations (forts and bases) which contain sites which contain facilities (also called "assets") which contain systems (ie. A10, B10 in the Uniformat standard) which contain components (think A/C units, doors, walls). This system lends itself well to being thought of in an "object-oriented" sense.

I went through a couple first drafts before getting fed up with how long this was taking and settled on a decent "good-enough" system which can be easily integrated into other ongoing projects.

The heirarchy is a tree whose leaf nodes are the **Components**. Each level in the heirarchy is _composed_ of instances at the level directly under it. We call these instances "children". I chose to represent the entire collection of all installations

## Challenges

By far, the biggest challenge is finding the best way to parameterize functions and object constructors. For instance, `calculate_component_condition()` is technically a function of component age. Therefore, the function signature can require the user to pass the "component age" _or..._ it can require "year built" along with a "projection_date" which defaults to `datetime.now()`. Adding insult to injury, function overloading is not native to the Python language.

The PhD engineers on our team have a much better intuition for how these _should_ look. It's also one of those things where there isn't a single right answer (but there are wrong ones). That's why this project is an iterative process and is still in active development.

## Conclusion

This project was born out of a need to centralize and deduplicate common engineering and R&D utilities within the E-SMS ecosystem. It provides an avenue for members of our team to experiment and interact with our research findings in a tangible way. It also aims to speed up future development. Following SOLID principles and common design philosophies, PySMS is extensible and modifiable.
