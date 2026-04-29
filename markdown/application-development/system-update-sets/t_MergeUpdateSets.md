---
title: Merge update sets
description: Merge multiple update sets into a single update set.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Merge update sets

Merge multiple update sets into a single update set.

## Before you begin

The batch update sets feature accomplishes the same outcome with a more predictable and robust solution. See [Update set batching](../hier-update-sets/concept/us-hier-overview.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Merge Update Sets or Merge Completed Sets**.

2.  Filter the list to show only the update set that you want to merge.

    You can only merge update sets that belong to the same application.

    ![Merge update sets.](../image/merge-update-sets.png)

3.  Enter a **Name** for the new update set.

4.  Enter a **Description** for the update set.

5.  Select **Merge**.

6.  In the confirmation dialog box, select **OK**.

    The most recent change for each object is moved from the original sets to the new set. Only changes that aren’t merged into the new set remain in the original sets. A message indicates how many updates were moved and how many were skipped.

    **Note:** The system determines which record is the most recent by comparing the **Updated** field for the records, NOT the **sys\_updated\_on** value in the payload.

7.  Open the old update set records in the Merged Update Sets related list and verify that the correct changes were moved.

8.  Delete or empty the original update sets to avoid committing an older change by mistake.


**Parent Topic:**[Configuring System Update Sets](../concept/configure-system-update-sets.md)

