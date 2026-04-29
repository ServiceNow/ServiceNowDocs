---
title: CMDB Health process status: incomplete score
description: The CMDB Health Dashboard shows the string 'incomplete score' for a metric when it fails to calculate the score for the metric.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tracking and troubleshooting, CMDB Health, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Health process status: incomplete score

The CMDB Health Dashboard shows the string 'incomplete score' for a metric when it fails to calculate the score for the metric.

'Incomplete score' is displayed when:

-   The number of CIs that are failing the tests of one of its sub-metric, reaches the failure threshold set for the metric. In this situation, the processing status for the respective parent metric \(for example, correctness\) is set to 'incomplete' in the CMDB Health Metric Status \[cmdb\_health\_metric\_status\] table. Processing for the failing metric in the current cycle stops, and therefore there are no aggregated health scores for the sub-metric or for the parent metric.

    To remediate, you need to resolve the underlying cause of CIs failing the sub-metric tests. See [CMDB Health process status: failure threshold reached](failure-threshold-reached.md) for more information about resolving the failures of the sub-metric.

-   An error is encountered while processing the sub-metric.

    To remediate, examine the system logs to determine the cause of the error. After fixing the cause of the problem, restart processing by manually executing the respective parent metric dashboard job.


**Parent Topic:**[CMDB Health process tracking and troubleshooting](c_CMDBHealthTroubleshooting.md)

