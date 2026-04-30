---
title: Exploring System Update Sets
description: An update set is a group of configuration changes that can be moved from one instance to another. Update sets enable developers to create functionality on a non-production instance, and promote the changes to another instance for testing or deployment.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2025-10-03"
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

Update sets track changes to applications and system platform features. This enables developers to create functionality on a non-production instance and promote the changes to another instance.

**Warning:** Update sets allow moving changes between instances that may be running different family release versions and different features. You can always load an update set created on an older family release on an instance running a newer family release. Loading an update set created on a newer family release on an instance running an older family release requires additional testing to determine compatibility. Updates from newer family releases may not produce the same functionality when moved to older family releases. In extreme cases, newer family release updates may cause outages or data loss on an older family release instance. Where possible, avoid moving updates from newer family releases to older family releases. Similar constraints apply to moving updates between instances running different versions of ServiceNow Store apps.

## System properties

Administrators can exclude system properties from update sets by making them private. Keeping system properties private helps prevent settings in one instance from overwriting values in another instance. For example, you may not want a system property in a production instance to use a particular value from a development instance. See [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Applications

Application developers have additional options with update sets such as:

-   Create an update set for a specific version of an application.
-   Specify which application tables to track in update sets.

## Update set tables

Each update set is stored in the Update Set `[sys_update_set]` table, and the customizations that are associated with the update set, which is entries in the Customer Update `[sys_update_xml]` table, appear as a related list on the update set record.

When a tracked object is customized, a corresponding record is added or updated in the Customer Update `[sys_update_xml]` table and is associated with the user current update set. The [associated application file properties](../../applications/concept/c_ApplicationFiles.md) are tracked and transferred along with the customized object in a single update record. A corresponding record is also added to the Versions `[sys_update_version]` table.

The Customer Update table contains one record per customized object, per update set. The Versions table contains one record per change to a customized object.

-   Administrators can compare two versions and revert to a specific version of an object.
-   Administrators can suppress versions for specific tables.
-   Administrators can specify fields on tracked tables that you can change without skipping updates to the rest of the record \(exclude the field from the update\).

**Note:** Don’t directly modify Customer Updates `[sys_update_xml]` records.

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
</table>## System update sets workflow

A common process for developing customizations with update sets involves moving changes from development to test and production instances.

1.  Create an update set on the development instance.
2.  Make customizations and changes on the development instance.
3.  Mark the update set as complete.
4.  Log in to the test instance and retrieve the completed update set from the development instance.
5.  Commit the update set on the test instance, and test customizations thoroughly.
6.  If the update set has problems in the test instance, repeat steps 1–5 to develop the fix on the development instance with another update set.
7.  Identify a common path for update sets to move from instance to instance and maintain that model. Never migrate the same update set from multiple sources. Move update sets from dev to test and then from test to production.
8.  Commit the update set on production. If the update set required a fix, commit both update sets in the order they were made.

## Benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Create an update set to store local changes.|[Create and select an update set as the current set](../task/create-select-update-set.md)|Developer|
|Select the current update set to store local changes.|[Select the current update set in Unified Navigation](../task/select-update-set-system-settings.md)|Admin|
|Commit an update set to prepare it for distribution.|[Commit an update set](../task/t_CommitAnUpdateSet.md)|Admin|
|Compare update sets to determine what differences they contain.|[Compare local update sets](../task/t_CompareLocalUpdateSets.md#)|Admin|
|Create an external file from an update set.|[Save an update set as a local XML file](../task/t_SaveAnUpdateSetAsAnXMLFile.md#)|Admin|
|Retrieve update sets from remote instances.|[Retrieve an update set](../task/t_RetrieveAnUpdateSet.md)|Admin|
|Back out changes applied from an update set.|[Back out an update set](../task/t_BackOutUpdateSet.md)|Admin|
|Set system properties related to update sets.|[Update sets properties](../reference/update-sets-properties.md)|Admin|
|Track customizations to application tables, fields, and records.|[Customizations tracked by update sets](../reference/customizations-tracked-update-sets.md)|Admin|
|Batch update sets together so you can preview and commit them in bulk.|[Working with batched update sets](../hier-update-sets/concept/us-hier-overview.md)|Admin|

## What to explore next

To learn more about configuring, using, and managing system update sets see:

-   [Configuring System Update Sets](configure-system-update-sets.md)
-   [Administer system update sets](administer-system-update-sets.md)
-   [Working with update sets](using-system-update-sets.md)
-   [Working with batched update sets](../hier-update-sets/concept/us-hier-overview.md)
-   [Update set transfers](../reference/update-set-transfers.md)

