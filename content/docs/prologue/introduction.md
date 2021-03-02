---
title: "Introduction"
description: "Read everything you need to know about the Degreed architecture, from Domain APIs, through Event-Driven Architecture, we got you covered."
lead: "You found it, the recipe book for Degreed's software development. In here you can read everything you need to know about being a succesfull and happy cook in our kitchen."
date: 2021-01-29
lastmod: 2021-01-29
draft: false
images: []
menu:
  docs:
    identifier: prologue-introduction
    parent: "prologue"
weight: 101
---
To continue our growth, we need an eco-system which supports that. We are building that new eco-system and want you to be successful in it.

This site will tell you everything you need to know about our new architecture and the [Architecture Principles]({{< ref "/docs/principles/introduction" >}} "Architecture Principles") which lie at its foundation.

When Degreed started, life was relatively simple. There weren't a lot of features to maintain, clients to please or fellow developers to collaborate with. Meaning our software was simple, the data models well understood and the feedback loop fast.

_You know how to make changes to the system and was confident in what the impact of those changes was._

As we grew, we added more complexity to all layers of our software. Not only did we add a lot of parts, those parts started moving more quickly when we grew to fourteen product teams.

We want to maintain our ability to make changes with confidence, while also growing our team. To do so, we need to have an architecture which enables us to do so. This document is our plan to increase developer productivity, autonomy and our ability to scale.

## Developer Productivity

Our goal is to increase developer productivity by _reducing the complexity_ and _increase the feedback loop_.

We want to reduce your cognitive load when solving a problem. Maybe the better description would be that we are pushing or moving the complexity away from the every-day developer experience.

What that means is that we are looking at ways where we can apply a multiplier. Push the complexity to a part of our system where we can solve it once for all teams beneath it.

A well known example is micro-services where you are not reducing the complexity, you choose to move a lot of complexity to the infrastructure so that developers have a reduced amount of complexity in their day-to-day work.

Reducing complexity is creating a system where the cognitive burden is low because we moved the complexity not inherent to your problem solving to other parts of our system.

## Autonomy

Autonomy is being able to build a solution with the tools optimal to your problem. We gain this independence by unbundling our data layer and detangling our application.

## Scalability

The only way to scale a large software organization is to keep expanding horizontally. Independent product teams who are empowered to optimize for their own goals.

We also need scalability around our software infrastructure. This is where we also apply horizontal scaling again with a service oriented architecture (System of Systems).

## Get involved

What you are reading is a living document. It may not breath, but it does evolve.

We need your help and input. You can always ask questions or start
discussions in our
[#architecture-townhall](https://degreed.slack.com/archives/C01LZ1XNH1Q)
channel on Slack.

You can also help us write this document. There is a "Edit this page on Github" button on every page which enables you to open up pull requests. You can also add issues to the Github repository if something is missing, unclear or wrong.
