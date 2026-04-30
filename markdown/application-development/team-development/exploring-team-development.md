---
title: Exploring Team Development
description: Team Development supports parallel development on multiple, non-production ServiceNow instances.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Team Development, Planning your application, Building applications]
---

# Exploring Team Development

Team Development supports parallel development on multiple, non-production ServiceNow instances.

## Team Development overview

Team Development enables developers to work on separate development instances while sharing code and resolving collisions throughout the development process.

After setting up the instance hierarchy, you can develop changes on your local development instance. Use the team dashboard to manage Team Development activities, such as:

-   Tracking local changes and determining which changes to promote to the parent development instance.
-   Pulling changes from the parent instance and resolving any collisions with local changes.
-   Comparing your instance with other development instances and resolving any collisions with other development projects.
-   Pushing changes when a feature is tested and ready to promote to the parent development instance.
-   Branching operations, including pushing and pulling record versions between instances.
-   A central dashboard for all Team Development activities.

Developers with admin access to their development instance and the parent instance can use Team Development. For alternative access settings, see [Granting access rights for the developers](../reference/r_GrantingAccessRightsToDevelopers.md).

## Team Development users

|User|Description|
|----|-----------|
|System Administrator|Configures instance hierarchies, defines remote instances, and administers parent instances in Team Development.|
|Developer|Pull and push versions of customized records to the parent instance in Team Development.|

## Team Development workflow

This workflow displays the Team Development admin workflow.

![team development admin workflow.](../image/team-development-workflow.png "Team Development admin workflow")

1.  Set up the development instance hierarchy as described in [Set up an instance hierarchy](../task/t_SetUpAnInstanceHierarchy.md).
    1.  Provision development instances on the same software version as the target instance. For example, use the software version that is running on your production instance.
    2.  \[Recommended\] Clone the target to the development instances.
    3.  For each instance, define the parent instance.
    4.  \[Optional\] For each instance, define the peer instances.
    5.  For each instance, pull all changes from the parent instance.
2.  For subdevelopment instances, grant access rights to appropriate developers.
3.  Develop customizations on subdevelopment instances.
    -   Pull versions from the parent instance, such as versions that were pushed from other subdevelopment instances. Reconcile any conflicts with the current local version, as necessary.
    -   Track local changes. Queue changes that are ready to push to the parent development instance.
    -   Compare versions on peer instances. Reconcile any conflicts.
4.  When a feature is ready to promote to the parent development instance, push the current version of the customized records.
5.  \(optional\) Have code reviewers approve or reject the pushed version. See [Approve or reject a push](../task/t_ApproveOrRejectAPush.md).
6.  Test and promote the feature into production according to your testing and release management process.

## When to use Team Development

<table id="r_WhenToUseTeamDevelopment_table_jbx_trm_5y"><thead><tr><th id="r_WhenToUseTeamDevelopment_table_jbx_trm_5y_entry_1">

Deployment option

</th><th id="r_WhenToUseTeamDevelopment_table_jbx_trm_5y_entry_2">

Good for

</th><th id="r_WhenToUseTeamDevelopment_table_jbx_trm_5y_entry_3">

Future considerations

</th></tr></thead><tbody><tr><td>

Update Sets

</td><td>

Storing changes to a base system or installed application.Storing and applying a particular version of an application.

Producing a file for export.

</td><td>

You can manually create update sets to store a particular application version.Use update sets to deploy patches or changes to installed applications.

 **Note:** Don’t use update sets to install applications. Instead, use the application repository or the ServiceNow Store to install applications.

</td></tr><tr><td>

Application Repository

</td><td>

Installing and updating applications on all company instances.Automatically managing application update sets.

Restricting access to applications to the same company.

Deploying completed applications to end users.

</td><td>

Consider uploading an application to the ServiceNow Store to share it with other users.

 Enables installation of and update to the latest application version only.

 Use update sets to store prior application versions.

 **Note:** If used with team development, publish applications only from a parent instance.

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Team Development, see:

-   [Configuring Team Development](../task/configuring-team-development.md)
-   [Resolving collisions](resolving-collisions.md)
-   [Local changes](c_LocalChanges.md)
-   [Working with version records](c_Versions.md)
-   [Team Development Reference](../reference/team-development-reference.md)

