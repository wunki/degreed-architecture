---
title: "Evolutionary Architecture"
description: ""
lead: "The systems and architecture should be designed and built to enable easy, incremental change."
date: 2021-02-04T12:14:48+01:00
lastmod: 2021-02-04T12:14:48+01:00
draft: false
images: []
menu:
  docs:
    parent: "principles"
weight: 203
toc: true
---

At this point in time we know less than we’ll know in six months. Our software should be able to evolve as we learn more about the business domain, the operational environment, and the technology itself. Change is a constant in the world around us, and its impact is increasingly unpredictable. However, by engineering our software for evolvability as a primary concern, we give ourselves the best chance of experimenting, learning and thriving in new conditions.

## Implications

* Whilst we cannot and should not design for every possible eventuality, the evolvability of our systems can be hugely improved, at low cost, if the likely triggers and impacts of change are considered early enough. Uncertainties, “what-if” business & technology changes and failure modes should be made explicit, rehearsed and mitigated where the cost to do so is low relative to the risk. Use Small and Simple and Model the Business Domain to group together functionality in ways that minimise the splash-zone of potential change.

* When making design decisions, give yourself the best chance of adapting to new information by waiting till the last responsible moment, and preferring choices that are easily reversible or that keep your options open.

* Define and regularly measure the architectural qualities that are most important to success, and which must be nurtured as the system evolves.

* Systems and processes will need to be exposed through clearly defined interface contracts so that the underlying implementation can change and evolve without impacting the wider system. _Note: this does not mean that a component or system's internal interfaces need to be approached in the same way._

* Components must be accessible through open, non-proprietary standards (with a preference for HTTP & in particular REST). Embracing the best practices of the web maximises the opportunity for evolution while minimising the risk of technical redundancy.

* Standards that are derived from working software and not just working groups are preferred. Battle-tested standards used by several organisations tend to be more adaptable than over-engineered hot air. Most successful standards tend to be the ones that are adopted by Open Source communities.

* Adopt patterns such as [Tolerant Reader](https://martinfowler.com/bliki/TolerantReader.html) and the [Principle of Robustness](https://en.wikipedia.org/wiki/Robustness_principle) to enable systems to release changes independently without requiring [parallel change](https://www.martinfowler.com/bliki/ParallelChange.html) versioning and migration.

* Sometimes incremental change is insufficient as requirements change, so consider [Sacrificial Architecture](https://martinfowler.com/bliki/SacrificialArchitecture.html) as a pattern. Don't be afraid to throw away and re-write, as this is often faster and will lead to better quality.
