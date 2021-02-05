---
title: "Architecture Principles Introduction"
description: ""
lead: "Architecture principles are declarative statements, made with the intention of guiding architectural design decisions and maintain one or more qualities of our system."
date: 2021-02-04T12:10:00+01:00
lastmod: 2021-02-04T12:10:00+01:00
draft: false
images: []
menu:
  docs:
    parent: "principles"
weight: 201
---
Degreed is moving from a single application, to a system of systems. We want every system – aka service – to thrive in our eco-system. The “Architecture Principles” are guidelines to help you achieve that goal.

The principles are not written in stone, they change and adapt along with the needs of the business. Every principle consists of the following:

* A **declarative statement**, for example: "smart nodes, dumb pipes: systems should be decoupled as much as possible and not centrally choreographed”.

* A **rationale** that describes the qualities of the system we want to achieve, for example: _"To allow systems to evolve over time and keep up with the business rate of change, having them own their own communication allows them to change quickly rather than negotiating a change”_.

* **Implications** which give us concrete examples what this would mean within our own eco-sytem.

Try to understand all of the principles and what they mean. They will help you to understand the rationale behind our architecture and make it easy to operate within it.