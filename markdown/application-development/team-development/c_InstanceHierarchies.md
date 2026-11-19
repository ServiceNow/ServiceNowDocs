---
title: Building an instance hierarchy
description: Team Development enables you to set up a distributed version control system between multiple ServiceNow instances where each instance acts as a source repository, or branch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/team-development/c\_InstanceHierarchies.html
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Team Development, Planning your application, Building applications]
---

# Building an instance hierarchy

Team Development enables you to set up a distributed version control system between multiple ServiceNow instances where each instance acts as a source repository, or branch.

Developers use separate instances to work on different features, applications, or product releases at the same time. With Team Development, developers can share code between these instances and resolve collisions throughout the development process.

Team Development enables you to [establish hierarchical relationships between instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_SetUpAnInstanceHierarchy.md) and provides a mechanism for transferring changes between instances that integrates with the Update Set process where necessary. In a Team Development instance hierarchy, each non-production instance has a parent instance. Instances that have the same parent instance are peer instances. The shared parent instance becomes the central hub, or repository, and all peer instances synchronize to it.

\[Omitted image "team-development-versions.png"\] Alt text: team development instance hierarchy and workflow

-   **[Set up an instance hierarchy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_SetUpAnInstanceHierarchy.md)**  
Set up an instance hierarchy that best supports your development life cycle.
-   **[Define a remote instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_DefineARemoteInstance.md)**  
For each instance, define other instances in the hierarchy as remote instances.
-   **[Select the parent instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_SelectTheParentInstance.md)**  
An instance can have multiple peer instances but only one parent instance.
-   **[Change the parent instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_ChangeTheParentInstance.md)**  
Change the parent for a development instance to modify the instance hierarchy.

**Parent Topic:**[Configuring Team Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/configuring-team-development.md)

