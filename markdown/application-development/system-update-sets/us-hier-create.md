---
title: Create a batch update set
description: You include an update set in a batch by specifying another update set as its parent.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Create a batch update set

You include an update set in a batch by specifying another update set as its parent.

## Before you begin

Role required: admin

Adding a WIP update set to a completed batch resets the batch base to WIP.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the record for an update set that you want to include as a child in the batch.

3.  On the Update Set record, navigate to the **Parent** field and select the update set to act as the parent.

4.  Click **Update**.

    The system returns to the list of Update Sets. If the **Parent** column is visible, it shows the parent for the newly-created child.


