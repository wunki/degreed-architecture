---
title: "Smart Nodes Dumb Pipes"
description: ""
lead: "Systems aim to be as decoupled and cohesive as possible, and not centrally choreographed in middleware."
date: 2021-02-04T12:15:09+01:00
lastmod: 2021-02-04T12:15:09+01:00
draft: false
images: []
menu:
  docs:
    parent: "principles"
weight: 205
toc: true
---
Composing larger systems around simpler and smaller systems also means needing to own their communication with other systems as well. To allow systems to evolve over time and keep up with the business’s desired pace of change, having them own their communication allows them to change quickly rather than negotiating a change to the pipes that connect them.

## Implications

* Prefer open protocols, such as HTTP.

* Services act like unix-filters, accepting requests, applying logic and returning a response.

* Implement integration adapters to isolate the technicalities of integration, and anti-corruption layers to isolate the translation of business data, between bounded contexts.

* When data needs to be exposed or exported outside the service boundary, wrap this communication in a service layer rather than allowing consumers to access the data directly. This helps prevent business logic leaking out of the system.