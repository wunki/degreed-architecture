---
title: "Database as a Service"
description: ""
lead: "In the past we have relied heavily on Stored Procedures. With the shift to a \"System of Systems\" design, where our goal is to increase autonomy for our teams, we have decided to build domain APIs which don’t use Stored Procedures."
date: 2021-02-04T12:15:09+01:00
lastmod: 2021-02-04T12:15:09+01:00
draft: false
images: []
menu:
  docs:
    parent: "principles"
weight: 204
toc: true
---

This principle only applies to the new development of our Domain APIs, which will use the JSON:API framework. Below you can find our reasoning behind the decision and what the implications are.

## Change Management

Stored Procedures should be treated to the same standards as the rest of our application. It needs to be part of our Continuous Integration pipeline, where automated tests run against it. It has proven difficult to apply versioning and automated tests for them. This makes it hard for us to reach the quality of Continuous deployment and zero downtime that we desire.
Database as a service

We are moving towards a Database as a Service model where each Domain API will access its own persistent storage, completely independent of other Domain APIs.

This means that we can use persistence which is emphatic to the domain. Using Stored Procedures binds us to a specific technology. Using Entity Framework means you could with relative low effort switch between SQL Server, PostgreSQL and Cosmos DB.

## Monolithic Database

Stored Procedures are often applied where different domains and teams want to re-use the same data layer. They allowed us to create an abstraction at the lowest level and making sure that it’s used across the business.

The Domain APIs will be the lowest level access you can get to data, meaning that we can now move that logic into the application layer.

## Tooling

Developer tooling has made leaps and bounds in the past years. From programming language advancements, to tools which help you during development (editors, source control, linters).

One of these tools in our toolbox as Degreed developers is the JSON:API framework, which enables us to easily release a best-in-class REST API for access to our data. 

The JSON:API framework depends heavily on Entity Framework Core (EF Core) to generate dynamic SQL statements. Continuing to make use of Stored Procedures would negate a lot of its capabilities.

## Implications

* Consider the use of Stored Procedures as premature optimization. Only use Stored Procedures for the most critical performance situations and when the application layer has failed to satisfy a particular requirement.

* No more use of Stored Procedures for business logic. Any business logic should be part of the application.

* No more use of Stored Procedures for access management or validation of inputs. This should all reside in the application, before being sent to the persistence layer.

* If you require to use Stored Procedures for reads, always start with views as they are much easier to use and they integrate better with EF Core, a core component of our JSON:API framework.