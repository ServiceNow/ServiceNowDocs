---
title: Resume a disabled Cloud vs Non-cloud resources scheduled job
description: Reactivate a scheduled job to resume data collection for the Cloud vs Non-cloud resources chart that appears in the Insights view in Service Graph Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-09"
reading_time_minutes: 1
breadcrumb: [Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Resume a disabled Cloud vs Non-cloud resources scheduled job

Reactivate a scheduled job to resume data collection for the Cloud vs Non-cloud resources chart that appears in the Insights view in Service Graph Workspace.

## Before you begin

Role required: cmdb\_query\_builder \(contained in the sn\_cmdb\_user, sn\_cmdb\_editor, sn\_cmdb\_admin user roles\)

## About this task

The Cloud vs Non-cloud resources chart in Service Graph Workspace uses several scheduled jobs that gather and calculate the data for the charts. Each bar in the CI classes chart represents a pair of a CI class and a storage type \(cloud, non-cloud\) such as Applications/Cloud. Each bar is associated with its own scheduled job. When a scheduled job exceeds its limits of time and amount of collected data, it is automatically stopped. A job that can't complete for 3 \(default\) consecutive days is automatically disabled for future runs.

Use the following procedure to later resume that disabled scheduled job.

## Procedure

1.  Select **All**.

2.  In the Filter navigator, enter `sysauto_query_builder.list` and open the Scheduled Email of Query Builders table.

3.  In the **Scheduled Email of Query Builders** list view, set **Active** to **true** for the scheduled job to resume.


