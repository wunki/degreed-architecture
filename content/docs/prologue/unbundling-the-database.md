---
title: "Unbundling the Database"
description: ""
lead: "Our data layer is the foundation of our application. It needs to scale and adapt to change. All of this without introducing any breaking changes. Unbundling our database with the help of Data APIs is how we achieve these goals."
date: 2021-02-04T11:48:56+01:00
lastmod: 2021-02-04T11:48:56+01:00
draft: false
menu:
  docs:
    parent: "prologue"
images: []
weight: 102
---

## Scalability

We will continue to experience tremendous growth as a business and our data store needs to accommodate this. Growing your data store means that you are breaking it into smaller, horizontal pieces. Pieces which you are then able to grow vertically.

We have chosen to divide our data layer around the areas of our business. In Domain Driven Design it's often referred to as a "Bounded Context". This will not only give us more scaling options, but also enable us to optimize our data store, specific to the needs of that context.

## Stability

I think we agree that our data is at the foundation of our application. This is where the *Stable Dependencies Principle* comes into play:

> Design your software in such a way that any given component depends on other components that are more stable than it is.

How are you able to address changing requirements in your most stable part of your dependency chain?

As always in software engineering, the answer is abstractions. You abstract away the data layer by supplying an interface, a contract. As a user you don't have to deal with implementation details or changing internals, you can depend on a stable contract.

We will introduce an uniform contract for getting data in and out of the system. Ours is a REST API, where we communicate in JSON's, something we are all familiar with. This is what we call [Data APIs]({{< ref "/docs/data/introduction" >}}) and we will dive deeper into the details later on.