---
title: Back out an update set
description: You can back out changes to existing records for any committed update set.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Update set transfers, System update sets, Deploying applications, Building applications]
---

# Back out an update set

You can back out changes to existing records for any committed update set.

## Before you begin

Role required: admin

## About this task

Backing out an update set creates delete updates in the current update set. If you commit, back out, and then reapply a remote update set, errors appear in the previewer because the deleted updates are considered more recent changes and cause collisions.

**Warning:** Do not back out the **Default** update set. This action can damage the configuration of the instance.

The back out process reverses both record-level updates and changes to the dictionary. Some changes caused by a back-out can result in data loss. These are the expected results of the back-out process:

|Customer Update|Result of the back out action|
|---------------|-----------------------------|
|A new table|The table is dropped from the database, deleting any data from it.|
|A new field|The field is dropped from the database, deleting any data from it.|
|A deleted field|The field is restored to the database, but the original data is lost.|
|A resized field|The field resize is reversed. If the field has been increased, data is truncated first to avoid errors.|
|A configured form|The form is reverted to its previous state.|
|A record is inserted|The record is deleted. \(See **Note** below\)|
|A record is deleted|The record is restored with its original data.|

**Warning:** Backing out an update set that belongs to an update set batch may affect other update sets in the batch. For more information, see [Back out batched update set](../hier-update-sets/concept/us-hier-overview.md#).

-   If the sys\_package is global, it is deleted.
-   If the sys\_package is not global, and it has a value, a warning displays that there is no deletion. Rather, the sys\_update\_xml is put into the default update set and the record is left in place.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Open the update set record.

    Make sure it is complete and a date is set on the **Release date** field.

    **Note:** The currently selected application affects what options are available for the update set. Make sure you select the application, such as Global, that matches the contents of the update set.

3.  Carefully review the contents of the update set and consider whether there will be problems if it is backed out.

    If backing out an update set is not sufficient or will cause issues, then, instead, create and commit a new update set to reverse the customizations.

4.  Click **Back Out**.

    A Progress page displays actions, progress, and problems. Problems are changes in more recent update sets that affect the update set that is being backed out. The backout preview process generates a warning for each problem.

5.  Resolve each problem before proceeding with the back out.

    -   To keep the latest version, click **Decide to Keep Current**.
    -   To back out to the previous version, click **Decide to Use Previous**.
    All changes are reversed as described in the table. The current update set tracks all of the new changes that occur.

    The update set and all associated update records are deleted. If needed, you can still navigate to the retrieved update set, preview it, and commit it again.

    **Note:** If you commit, back out, and then reapply a remote update set, errors appear in the previewer because backing out an update set creates delete updates in the current update set. The deletes are considered more recent changes and cause collisions.


