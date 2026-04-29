---
title: Code reviews
description: Team Development administrators can require that pushes undergo code review before accepting pushes.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Team Development, Planning your application, Building applications]
---

# Code reviews

Team Development administrators can require that pushes undergo code review before accepting pushes.

When code review is enabled, pushing a change to the parent instance triggers the code review workflow. By default, users with the teamdev\_code\_reviewer role receive notifications to review changes and can approve or reject changes. The Team Development Code Reviewers has the teamdev\_code\_reviewer role.

For each change, reviewers can see the following information.

-   Which [remote instance](../task/t_DefineARemoteInstance.md) the pushed change comes from.
-   Who pushed the change to the parent.
-   What the change is called.
-   When the change was created.
-   Which versions the change includes.

Reviewers must approve or reject a push from the Team Development application.

While changes are being reviewed on the parent instance, a child instance cannot do the following activities involving the parent instance:

-   Push changes to the parent instance.
-   Pull changes from the parent instance.
-   Reconcile changes with the parent instance.
-   Change the parent instance to another instance.
-   Delete the remote instance record for the parent instance.

