---
title: "System of Systems"
description: ""
lead: "Build small and simple systems, which compose into a single system."
date: 2021-02-04T12:14:38+01:00
lastmod: 2021-02-04T12:14:38+01:00
draft: false
images: []
menu: 
  docs:
    parent: "principles"
weight: 202
toc: true
---

Monolithic applications can be successful, but it has become common for organisations to feel frustrations with them as they grow in complexity and scope over time.

Change cycles are tied together – a change made to a small part of the application requires the entire monolith to be rebuilt, retested and deployed. Over time it is often hard to keep a good modular structure, making it challenging to keep changes that ought to affect only one module contained within that module. Scaling requires scaling of the entire application rather than parts of it that require greater resources. Scaling requires uplift of the entire application rather than only the parts that require greater resources.

Building software that is small and simple also makes systems easier to reason about, and easier to test independently. Things that are easier to reason about, with less code, tend to generate fewer bugs and reduce the likelihood of complex issues in Production. 

## Implications

* Aim to decompose your system into a suite of smaller systems, each of which focus on doing a small number of things well.

* Build systems around business capabilities that change independently to others, rather than individual features or technologies.

* Beware the risks of creating a distributed monolith.

* Services are independently deployable and independently testable.

* Reduce the burden of managing several smaller systems through automation.

* In distributed systems, it is important to design for failure.

* Publish interfaces.