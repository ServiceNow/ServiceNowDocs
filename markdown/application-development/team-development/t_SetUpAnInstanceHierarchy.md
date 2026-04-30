---
title: Set up an instance hierarchy
description: Set up an instance hierarchy that best supports your development life cycle.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Building an instance hierarchy, Configure, Team Development, Planning your application, Building applications]
---

# Set up an instance hierarchy

Set up an instance hierarchy that best supports your development life cycle.

## Before you begin

Role required: admin

## About this task

This example demonstrates how to set up an instance hierarchy where several peer subdevelopment instances have the same parent development instance but a more complex configuration is required.

Don’t use Team Development with production or test instances. When you back out a change on a Team Development instance, it backs out the change, including undoing the work on the source instance. This behavior can cause major problems on test and production instances.

## Procedure

1.  Provision a parent development instance on the same software version, such as Yokohama, as the target instance.

2.  Clone the production instance to the parent development instance.

3.  Provision subdevelopment instances on the same software version as the parent development instance.

4.  Log in to the parent development instance and duplicate it with the subdevelopment instances.

5.  On each subdevelopment instance:

    1.  Define [remote instance connections](t_DefineARemoteInstance.md) to other instances in the hierarchy that this instance must push and pull with.
    2.  Select [the parent instance](t_SelectTheParentInstance.md).
    3.  Pull all changes from the parent instance.
    4.  [Grant access rights](../reference/r_GrantingAccessRightsToDevelopers.md) to appropriate developers.

**Parent Topic:**[Building an instance hierarchy](../concept/c_InstanceHierarchies.md)

