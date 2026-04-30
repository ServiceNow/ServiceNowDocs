---
title: Preview a batch of update sets
description: You can preview at once all the update sets belonging to a batch.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Preview a batch of update sets

You can preview at once all the update sets belonging to a batch.

## Before you begin

Role required: admin

You must have retrieved the update sets from the source instance.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**

2.  From the list of retrieved update sets, select the batch base for the batch you want to preview.

    You cannot separately preview an update set that is a child in a batch. You must preview the entire batch by previewing the batch base. If necessary, you can [remove the child update set](us-hier-reorg.md) from the batch by editing its record's **parent** field.

3.  Click **Preview Update Set Batch**.

4.  If the system found problems, preview the problems.

    1.  Click the **Preview Problems for Batch** and [resolve the problems](../../task/t_PreviewARemoteUpdateSet.md#) as you normally would for any update set.

    2.  When you have resolved all the problems, click **Run Preview Again for Batch**.


