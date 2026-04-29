---
title: Create a batch update set
description: You include an update set in a batch by specifying another update set as its parent.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Create a batch update set

You include an update set in a batch by specifying another update set as its parent.

## Before you begin

Role required: admin

When you add an in-progress update to a batch that is marked as complete, the status of the batch changes back to in progress.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the record for an update set that you want to include as a child in the batch.

3.  Navigate to the parent field on the update set record.

4.  Select the update set to act as the parent.

5.  Select **Update**.

    The system navigates back to the Update Sets list. When the parent column is displayed, it identifies the parent associated with the newly created child.


