---
title: Working with batched update sets
description: Batched update sets enable you to group update sets together so you can preview and commit them in bulk.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [batch, update set]
breadcrumb: [System update sets, Deploying applications, Building applications]
---

# Working with batched update sets

Batched update sets enable you to group update sets together so you can preview and commit them in bulk.

Dealing with multiple update sets can lead to problems, including committing update sets in the wrong order or inadvertently leaving out one or more sets. You can avoid these problems by grouping completed update sets into a batch.

**Note:** To preserve the update set batch hierarchy while cloning, set only the parent update set to Ignore status and leave all other update sets as Complete. This will prevent batch sets from cloning and preserves the batch update set hierarchy.

The system organizes update set batches into a hierarchy. One update set can act as the parent for multiple child update sets. A given set can be both a child and parent, enabling multiple-level hierarchies. One update set at the top level of the hierarchy acts as the base update set.

When you preview or commit the base update set, you preview or commit the entire batch. The system decides which changes to process first and checks for any conflicts by looking at when each change was made and how they are connected in a sequence. This sequence, or ancestry, refers to the specific moments when each change in the update sets occurred.

**Note:** For more details, see [Compare local update sets](../../task/t_CompareLocalUpdateSets.md) and [View customizations and compare with current version](../../task/view-customer-update-records.md).

## Example of batched update sets

The list of update set records reflects the batch hierarchy in the **Parent** and**Batch Base** columns.

![List of batched update sets](../../image/xmpl-batch-us.png "List of batched update sets")

![Diagram of batched update set hierarchy.](../../image/update-sets-batch-1.png "Diagram of batched update set hierarchy")

-   **[Reorganize a batch of update sets](../task/us-hier-reorg.md)**  
You can remove an individual update set from the batch or change its parent.

**Parent Topic:**[System update sets](../../concept/system-update-sets.md)

