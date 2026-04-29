---
title: Exploring System Update Sets
description: An update set is a group of configuration changes that can be moved from one instance to another. Update sets enable developers to create functionality on a non-production instance, and promote the changes to another instance for testing or deployment.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Exploring System Update Sets

An update set is a group of configuration changes that can be moved from one instance to another. Update sets enable developers to create functionality on a non-production instance, and promote the changes to another instance for testing or deployment.

## System update sets overview

An update set is an XML file that contains:

-   A set of record details that uniquely identify the update set.
-   A list of configuration changes.
-   A state that determines whether another instance can retrieve and apply configuration changes.

## Users

<table id="table_lqr_lpq_jfc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

Creates, compares, and merges update sets while also managing how update sets store, retrieve, preview, and apply configuration changes between instances.

</td></tr><tr><td>

Developer

</td><td>

Creates update sets for specific versions of an application and specifies which application tables to track.

</td></tr></tbody>
</table>## Workflows

A common process for developing customizations with update sets involves moving changes from development to test and production instances.

![Three-step import process for update set workflow.](../image/update-sets-workflow.png "Three-step import process")

1.  Create an update set on the development instance.
2.  Make customizations and changes on the development instance.
3.  Mark the update set as complete.
4.  Log in to the test instance and retrieve the completed update set from the development instance.
5.  Commit the update set on the test instance, and test customizations thoroughly.
6.  If the update set has problems in the test instance, repeat steps 1–5 to develop the fix on the development instance with another update set.
7.  Identify a common path for update sets to move from instance to instance and maintain that model. Never migrate the same update set from multiple sources. Move update sets from dev to test and then from test to production.
8.  Commit the update set on production. If the update set required a fix, commit both update sets in the order they were made.

If your development environment consists of only two instances, you can combine your development and testing instances into a single staging instance.

![Two-step import process for update set workflow.](../image/update-sets-workflow-2.png "Two-step import process")

1.  Create an update set on the staging instance.
2.  Make customizations and changes on the staging instance.
3.  Mark the update set as complete.
4.  Test customizations thoroughly on the staging instance.
5.  If the update set has problems, repeat steps 1–4 to develop the fix on the staging instance with another update set.
6.  Log in to the production instance and retrieve the completed update set from the staging instance. If the update set required a fix, retrieve both update sets.
7.  Commit the update set on production. If the update set required a fix, commit both update sets in the order they were made.

## Benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create an update set to store local changes.|[Create and select an update set as the current set](../task/create-select-update-set.md)|Developer|
|Select the current update set to store local changes.|[Select the current update set in Unified Navigation](../task/select-update-set-system-settings.md)|Admin|
|Commit an update set to prepare it for distribution.|[Commit an update set](../task/t_CommitAnUpdateSet.md)|Admin|
|Compare update sets to determine what differences they contain.|[Compare local update sets](../task/t_CompareLocalUpdateSets.md)|Admin|
|Create an external file from an update set.|[Save an update set as a local XML file](../task/t_SaveAnUpdateSetAsAnXMLFile.md#)|Admin|
|Retrieve update sets from remote instances.|[Retrieve an update set](../task/t_RetrieveAnUpdateSet.md)|Admin|
|Back out changes applied from an update set.|[Back out an update set](../task/t_BackOutUpdateSet.md)|Admin|
|Set system properties related to update sets.|[Update sets properties](../reference/update-sets-properties.md)|Admin|
|Track customizations to application tables, fields, and records.|[Customizations tracked by update sets](../reference/customizations-tracked-update-sets.md)|Admin|
|Batch update sets together so you can preview and commit them in bulk.|[Working with batched update sets](../hier-update-sets/concept/us-hier-overview.md)|Admin|

## Use cases

Choose update sets or the application repository depending on the result that you want to achieve. Don’t use both Update Sets and the Application Repository for scoped app development. Combining the usage of both results in skipped changes and commit errors. After installing an app from the Application Repository, continue its usage for development and publishing. Update sets can only transfer limited application files. For larger transfers, export and import data using import sets or web services.

-   **Update sets**
    -   Storing changes to a base system or installed application.
    -   Storing and applying a particular version of an application.
    -   Producing a file for export.
-   **Application repository**
    -   Installing and updating applications on all company instances.
    -   Managing application update sets.
    -   Restricting access to applications from the same company.
    -   Deploying completed applications to end users.

**Warning:** Update sets track changes to applications and system platform features. Update sets from older releases can be loaded onto newer instances without problems. Moving update sets from newer to older releases, or between different ServiceNow Store app versions, should be avoided due to potential compatibility issues and risks of data loss.

## What to explore next

To learn more about configuring, using, and managing system update sets see:

-   [Configuring System Update Sets](configure-system-update-sets.md)
-   [Working with update sets](using-system-update-sets.md)
-   [Working with batched update sets](../hier-update-sets/concept/us-hier-overview.md)
-   [Update set transfers](../reference/update-set-transfers.md)

