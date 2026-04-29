---
title: Configure classes for Cloud vs Non-cloud resources in Service Graph Workspace
description: Include or exclude pairs of CI Class/Type in the Cloud vs Non-cloud resources chart that appears in the Insights view in Service Graph Workspace.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure classes for Cloud vs Non-cloud resources in Service Graph Workspace

Include or exclude pairs of **CI Class**/**Type** in the Cloud vs Non-cloud resources chart that appears in the Insights view in Service Graph Workspace.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

The CMDB Insight Query Categories \[sn\_cmdb\_ws\_insight\_query\_category\] table contains the pairs of **CI Class**/**Type** for the Cloud vs Non-cloud resources chart that appears in the Insights view in Service Graph Workspace. The **Active** setting in a record determines if the respective **CI Class**/**Type** pair appears in the chart. By default, all pairs are configured to appear in the chart.

A **CI Class**/**Type** pair appears or doesn't appear according to its **Active** setting and regardless of the status of its associated scheduled job.

## Procedure

1.  Select **All**.

2.  In the Filter navigator, enter `sn_cmdb_ws_insight_query_category.list` to access the CMDB Insight Query Categories table.

3.  Set **Active** to **true** or **false** for a CI Class/Type pair.

    For example, set **Active** to **false** for the **Applications**/**Non-cloud** pair. This setting will exclude from the chart all CIs in the Applications class which are determined to be non-cloud.


