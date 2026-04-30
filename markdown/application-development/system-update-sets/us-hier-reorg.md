---
title: Reorganize a batch of update sets
description: You can remove an individual update set from the batch or change its parent.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Reorganize a batch of update sets

You can remove an individual update set from the batch or change its parent.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

2.  Select the record for an update set that you want to move or remove as a child in the batch.

3.  On the update set record, navigate to the **Parent** field and select the new update set to act as the parent.

4.  To remove the update set from the batch, delete any text from the **Parent** field and leave it blank.

5.  Click **Update**.

    The system returns to the list of update sets. If the **Batch Base** column is visible, it shows the parent for the newly-created child.


## What to do next

If the system property **glide.update\_set.auto\_preview** is set to **true**, the system automatically starts the preview process after the record is updated with a new parent. If this property is **false**, you must start the process manually. For more information on the preview process, see [Preview a batch of update sets](us-hier-preview.md) .

**Parent Topic:**[Working with batched update sets](../concept/us-hier-overview.md)

