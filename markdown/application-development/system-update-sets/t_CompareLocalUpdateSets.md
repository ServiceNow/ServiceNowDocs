---
title: Compare local update sets
description: Administrators can preview local and remote \(retrieved\) update sets and compare the sets with one another to resolve conflicting changes.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Compare local update sets

Administrators can preview local and remote \(retrieved\) update sets and compare the sets with one another to resolve conflicting changes.

## Before you begin

Role required: admin

## About this task

Compare local update sets to identify collisions and confirm that the proper changes are being committed. Resolve all conflicts before moving an update set between instances.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the check boxes beside the update sets to compare.

3.  In the **Actions on selected rows...** dropdown, select **Compare Update Sets**.

    The progress screen displays as ServiceNow generates the collision report.

    ![Generating a collision report](../image/update-sets-collision-report.png "Collision report")

4.  Select **Go to the Collision Report** when the report is complete.

5.  Inspect the list for collisions by locating duplicate collision numbers that show the same change in separate update sets.

6.  Resolve the collision by deleting the unwanted update record from one of the update sets.

    **Note:** To delete a record, open the update record directly. You can't delete it using the **Delete** action from the Update Set Collisions list. Deleting the update record only removes the record of the customization, it doesn't undo the customization.

    1.  Select the link in the sys update column for the unwanted update.
    2.  Select **Delete**.
7.  Run the comparison again to make sure that all collisions have been resolved.


-   **[Update set collision resolution](../reference/update-set-collisions.md)**  
A collision is an update that has a newer local update.

**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)

