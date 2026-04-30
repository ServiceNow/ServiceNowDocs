---
title: Merge update sets
description: You can merge multiple update sets into a single update set. This capability is supported for backward compatibility with earlier releases of the ServiceNow platform. The newer batch update sets feature accomplishes the same outcome with a more predictable and robust solution.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Merge update sets

You can merge multiple update sets into a single update set. This capability is supported for backward compatibility with earlier releases of the ServiceNow® platform. The newer batch update sets feature accomplishes the same outcome with a more predictable and robust solution.

## Before you begin

**Note:** You cannot "unmerge" update sets once they have been merged. To learn more, see [Update set batching](../hier-update-sets/concept/us-hier-overview.md).

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Merge Update Sets**.

    By default, the list is filtered to only show update sets that are In progress.

    Alternatively, navigate to **System Update Sets** &gt; **Merge Completed Sets**. By default, the list is filtered to only show update sets that are in the Complete state. For example, you may want to use this filter after pushing changes or transferring update set from a development to a test instance.

2.  Filter the list to show only the update set that you want to merge.

    You can only merge update sets that belong to the same application.

    ![Merge update sets](../image/MergeUpdateSets.png "Merge update sets")

3.  Enter a **Name** for the new update set.

    Updates are moved to this new update set during the merge process.

4.  Enter a **Description** for the update set.

5.  Click **Merge**.

6.  In the confirmation dialog box, click **OK**.

    -   The new update set is created.
    -   The most recent change for each object is moved from the original sets to the new set. Only changes that are not merged into the new set remain in the original sets. A message indicates how many updates were moved and how many were skipped. For example, if both update sets modify the Incident form, only the most recent change is moved to the new update set. The other modification remains in its original update set to provide a record of the changes that were not moved.

        **Note:** The system determines which record is the most recent by comparing the **Updated** field for the records, NOT the **sys\_updated\_on** value in the payload.

7.  Verify that the correct changes were moved to the new set by scrolling down to the Merged Update Sets related list and opening the old update set records.

8.  Delete or empty the original update sets to avoid committing an older change by mistake.

    The system does not remove updates that were not merged into the new set. Do not move updates "left behind" in old sets into the new set.


