---
title: Set up an instance hierarchy
description: Set up an instance hierarchy that best supports your development life cycle.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Team Development, Planning your application, Building applications]
---

# Set up an instance hierarchy

Set up an instance hierarchy that best supports your development life cycle.

## Before you begin

Role required: none

## About this task

This example demonstrates how to set up an instance hierarchy where several peer sub-development instances have the same parent development instance, but a more complex configuration may be required to handle multiple project teams or other customer requirements.

Do not use Team Development with production or test instances.

-   Do not use a test or production instance as the parent instance in Team Development.
-   Do not make any instance the parent of a production instance.
-   Production instances should never have a parent.

When you back out a change on a Team Development instance, it backs out the change all the way back down the chain, including undoing the work on the source instance. This behavior can cause major problems on test and production instances.

## Procedure

1.  Provision a parent development instance on the same software version, such as Dublin, as the target instance, such as production.

2.  Clone the production instance to the parent development instance.

    This step is a recommended best practice.

3.  Provision sub-development instances on the same software version as the parent development instance.

4.  Log in to the parent development instance and clone it to the sub-development instances.

5.  On each sub-development instance:

    1.  Define [remote instance connections](t_DefineARemoteInstance.md) to other instances in the hierarchy that this instance needs to push and pull with.
    2.  Select [the parent instance](t_SelectTheParentInstance.md).
    3.  Pull all changes from the parent instance.
    4.  [Grant access rights](../reference/r_GrantingAccessRightsToDevelopers.md) to appropriate developers.
    ![Team development process](../image/TeamDevProcess.png)


