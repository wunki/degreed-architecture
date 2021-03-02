---
title: "Detangling the Monolith"
description: ""
lead: "To reduce cognitive load, we will split our monolithic application into smaller, composable services. This is what we call \"Application Services\"."
date: 2021-02-04T11:50:26+01:00
lastmod: 2021-02-04T11:50:26+01:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 103
---

By implementing application services, we will reduce the cognitive load required to make changes. We also increase autonomy, the ability to aply the optimal solution to your problem, not being hindered by dependencies outside of your domain.

## What do they contain?

Application services are units of business logic which act on changes within the business. That's all they contain, business logic. The application services sit on top of our Domain API's and preferably have a one-to-one relation with them.

We have a whole [Domain APIs]({{< ref "/docs/data/introduction" >}}) chapter dedicated to them, where you can read how they communicate and fit within the whole eco-system.

## Conclusion

In the prologue we wanted to introduce you to the two architecture initiatives: *"Unbundling the database"* and *"Detangling the Monolith"*.

We will accomplish these things with *"Domain APIs"* and *"Application Services"* on top of *"Event-Driven Architecture"*. That's a whole lot of lingo, which I promise you will make sense once we dive into them later on.

Before we go there, let's first dive into the underlying principles which have guided us in building these plans and which will help guide you in your day-to-day decision making.
