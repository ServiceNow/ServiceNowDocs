---
title: Team Development process
description: The basic Team Development process sets up the instance hierarchy, grants developer access rights, manages the movement of development changes from development instances to test instances, and promotes applications to the production instance.
locale: en-US
release: yokohama
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Team Development, Team Development, Planning your application, Building applications]
---

# Team Development process

The basic Team Development process sets up the instance hierarchy, grants developer access rights, manages the movement of development changes from development instances to test instances, and promotes applications to the production instance.

## Procedure

1.  Set up the development instance hierarchy as described in [Set up an instance hierarchy](t_SetUpAnInstanceHierarchy.md).

    1.  Provision development instances on the same software version as the target instance. For example, use the software version that is running on your production instance.
    2.  \[Recommended\] Clone the target to the development instances.
    3.  For each instance, define the parent instance.
    4.  \[Optional\] For each instance, define the peer instances.
    5.  For each instance, pull all changes from the parent instance.
2.  For sub-development instances, grant access rights to appropriate developers.

3.  Develop customizations on sub-development instances.

    Use the team dashboard to track development activities.

    -   Pull versions from the parent instance, such as versions that were pushed from other sub-development instances. Reconcile any conflicts with the current local version, as necessary.
    -   Track local changes. Queue changes that are ready to push to the parent development instance.
    -   Compare versions on peer instances. Reconcile any conflicts.
4.  When a feature is ready to promote to the parent development instance, push the current version of the customized records.

5.  Have code reviewers approve or reject the pushed version.

6.  Test and promote the feature into production according to your testing and release management process.


**Related topics**  


[Team Development](../concept/c_TeamDevelopment.md)

[Access rights for developers](../reference/r_GrantingAccessRightsToDevelopers.md)

[Push a version](t_PushAVersion.md)

