---
title: Detecting duplicate CIs
description: When the identification process encounters duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/servicenow-platform/configuration-management-database-cmdb/id-detect-dup-ci.html
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB Identification and Reconciliation \(IRE\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Detecting duplicate CIs

When the identification process encounters duplicate CIs, it groups each set of duplicate CIs into a de-duplication task for review and remediation. A large number of duplicate CIs might be due to weak identification rules. You can configure the identification engine to reconcile duplicate CIs.

During CMDB Identification, processing of duplicate CIs is determined by the properties **glide.identification\_engine.skip\_duplicates** \(set to true by default\) and **glide.identification\_engine.skip\_duplicates.threshold** \(set to 5 by default\), and on the number of duplicate CIs that are detected. You can configure these properties so duplicate CIs are automatically reconciled, skipping duplication.

-   If **glide.identification\_engine.skip\_duplicates** is true, and the number of duplicate CIs is less than the threshold specified by **glide.identification\_engine.skip\_duplicates.threshold**, then the oldest of the duplicate CIs is picked as a match and gets updated. That oldest duplicate CI also becomes the main CI for that set of duplicate CIs. The rest of the duplicate CIs are tagged as duplicates by setting the cmdb\_ci's **duplicate\_of** to the appropriate main CI. During matching, the identification engine filters out any CI that is tagged as duplicate of any CI.
-   If **glide.identification\_engine.skip\_duplicates** is false, then matching of duplicate CIs fails with an error, and none of the duplicate CIs are updated.

Also, the **glide.duplicate\_ci\_remediator.max.cis** property determines de-duplication processing for a large number of duplicate CIs. For more information, see the 'Large number of duplicate CIs' section in the [Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md) topic.

In either case, de-duplication tasks are always created.

**Note:** For a duplicate CI, if any of the CI's attributes, other than **duplicate\_of**, is updated by IRE processing, then the CI is no longer considered a duplicate CI. In that situation, the value of **duplicate\_of** is cleared in the CI.

For more information about these properties, see [Properties for Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/properties-id-reconciliation.md).

## Review de-duplication tasks

For information about reviewing and remediating de-duplicate tasks, and how the main CI is used, see [Duplicate CIs remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/de-duplication-tasks.md).

**Parent Topic:**[CMDB Identification and Reconciliation \(IRE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/servicenow-platform/configuration-management-database-cmdb/c_CMDBIdentifyandReconcile.md)

