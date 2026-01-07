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

I began to notice a pattern among the number of projects we've worked on. We were constantly rewriting the same utility functions, creating a fair amount of code duplication.

A large chunk of our work revolves around facility degredation simulation, which itself revolves around one particular statistical model: [the Weibull Curve](<https://doi.org/10.1061/40799(213)4>)
