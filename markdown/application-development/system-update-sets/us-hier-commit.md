---
title: Commit a batch of update sets
description: You can commit at once all the update sets belonging to a batch.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Commit a batch of update sets

You can commit at once all the update sets belonging to a batch.

## Before you begin

Role required: admin

Before committing, you must have previewed the update sets from the source instance and resolved any collisions.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Retrieved Update Sets**

2.  From the list of retrieved update sets, select the batch base for the batch you want to preview.

    You cannot separately commit an update set that is a child in a batch. You must commit the entire batch by committing the batch base. If necessary, you can remove the child update set from the batch by editing its record's **parent** field.

3.  Click **Commit All Update Sets**.


