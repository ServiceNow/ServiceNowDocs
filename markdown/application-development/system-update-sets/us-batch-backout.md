---
title: Back out batched update set
description: Back out a batched update set by following the backout procedure for the base update set for the batch. You can also back out any child update set independently.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with batched update sets, System update sets, Deploying applications, Building applications]
---

# Back out batched update set

Back out a batched update set by following the backout procedure for the base update set for the batch. You can also back out any child update set independently.

The following rules apply when backing out an update set that belongs to a batch:

-   If the update set has a parent value, the system clears the parent value and treats the update set as an independent update set, or as a new batch base if it has any children.
-   The system backs out the selected update set, plus any children of the backed-out update set.

To learn more, see [Back out an update set](../task/t_BackOutUpdateSet.md) and [Update set batching](../hier-update-sets/concept/us-hier-overview.md)

## Example of backing out a batched update set

If you back out Update Set 1.1 from the batch shown in [List of batched update sets before backing out an update set](us-batch-backout.md#fig_g3f_syx_41b), the result is the batch shown in [List of batched update sets after backing out Update Set 1.1](us-batch-backout.md#fig_px1_xyx_41b).

![Batched update sets](../image/xmpl-batch-us.png "List of batched update sets before backing out an update set")

![Batched update set after backing out a child update set from the batch](../image/xmpl-batch-us-after-backout.png "List of batched update sets after backing out Update Set 1.1")

[Hierarchical diagram of Update Set batch](us-batch-backout.md#fig_xcs_fyd_p1b) shows the hierarchy both before and after the back out. The red boxes show the update sets the system backs out if you back out Update Set 1.1.

![Diagram of batched update set hierarchy with a child selected to back out](../image/xmpl-diagram-batched-update-sets.png "Hierarchical diagram of Update Set batch")

**Parent Topic:**[Working with batched update sets](../hier-update-sets/concept/us-hier-overview.md)

