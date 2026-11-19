---
title: Back out batched update set
description: Back out a batched update set by following the backout procedure for the base update set for the batch. You can also back out any child update set independently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/system-update-sets/us-batch-backout.html
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

To learn more, see [Back out an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/t_BackOutUpdateSet.md) and [Update set batching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/us-hier-overview.md)

## Example of backing out a batched update set

If you back out Update Set 1.1 from the batch shown in [List of batched update sets before backing out an update set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/us-batch-backout.md), the result is the batch shown in [List of batched update sets after backing out Update Set 1.1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/us-batch-backout.md).

\[Omitted image "xmpl-batch-us.png"\] Alt text: Batched update sets

\[Omitted image "xmpl-batch-us-after-backout.png"\] Alt text: Batched update set after backing out a child update set from the batch

[Hierarchical diagram of Update Set batch](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/us-batch-backout.md) shows the hierarchy both before and after the back out. The red boxes show the update sets the system backs out if you back out Update Set 1.1.

\[Omitted image "xmpl-diagram-batched-update-sets.png"\] Alt text: Diagram of batched update set hierarchy with a child selected to back out

**Parent Topic:**[Working with batched update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/us-hier-overview.md)

