---
title: Detecting duplicate CIs
description: When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Detecting duplicate CIs

When IRE identification process detects duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.

During Identification and Reconciliation Engine \(IRE\) processes, handling of duplicate CIs is determined by the properties **glide.identification\_engine.skip\_duplicates** \(set to true by default\) and **glide.identification\_engine.skip\_duplicates.threshold** \(set to 5 by default\), and on the number of duplicate CIs that are detected. You can configure these properties so duplicate CIs are automatically reconciled, skipping duplication.

-   If **glide.identification\_engine.skip\_duplicates** is true, and the number of duplicate CIs is less than the threshold specified by **glide.identification\_engine.skip\_duplicates.threshold**, then the oldest of the duplicate CIs is picked as a match and gets updated. That oldest duplicate CI also becomes the main CI for that set of duplicate CIs. The rest of the duplicate CIs are tagged as duplicates by setting their **duplicate\_of** attribute to the appropriate main CI. During matching, IRE filters out any CI that is tagged as duplicate of any CI.
-   If **glide.identification\_engine.skip\_duplicates** is false, then matching of duplicate CIs fails with an error, and none of the duplicate CIs are updated.

Also, the **glide.duplicate\_ci\_remediator.max.cis** property determines de-duplication processing for a large number of duplicate CIs. For more information, see the 'Large number of duplicate CIs' section in the [Duplicate CIs remediation](de-duplication-tasks.md) topic.

In either case, de-duplication tasks are always created.

**Note:** For a duplicate CI, if any of the CI's attributes, other than **duplicate\_of**, is updated by IRE processing, then the CI is no longer considered a duplicate CI. In that situation, the value of **duplicate\_of** is cleared in the CI.

For more information about these properties, see [Properties](../reference/properties-id-reconciliation.md).

## Remediating de-duplication tasks

For information about reviewing and remediating de-duplicate tasks, and how the main CI is used, see [Duplicate CIs remediation](de-duplication-tasks.md).

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md)

