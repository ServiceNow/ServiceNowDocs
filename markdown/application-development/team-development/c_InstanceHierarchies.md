---
title: Instance hierarchies
description: Team Development allows you to set up a distributed version control system between multiple ServiceNow instances where each instance acts as a source repository, or branch.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Team Development, Planning your application, Building applications]
---

# Instance hierarchies

Team Development allows you to set up a distributed version control system between multiple ServiceNow instances where each instance acts as a source repository, or branch.

Developers use separate instances to work on different features, applications, or product releases at the same time. With Team Development, developers can share code between these instances and resolve collisions throughout the development process.

Team Development allows you to [establish hierarchical relationships between instances](../task/t_SetUpAnInstanceHierarchy.md) and provides a mechanism for transferring changes between instances that integrates with the Update Set process where necessary. In a Team Development instance hierarchy, each non-production instance has a parent instance. Instances that have the same parent instance are peer instances. The shared parent instance becomes the central hub, or repository, and all peer instances synchronize to it.

**Parent Topic:**[Team Development](c_TeamDevelopment.md)

