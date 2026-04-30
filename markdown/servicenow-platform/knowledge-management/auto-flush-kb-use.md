---
title: Modify the data retention policy for View logs
description: Remove unwanted and older data from the Knowledge Use \[kb\_use\] table through the data retention policy.
locale: en-US
release: yokohama
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View knowledge logs, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modify the data retention policy for View logs

Remove unwanted and older data from the Knowledge Use \[kb\_use\] table through the data retention policy.

## Before you begin

Role required: admin

## About this task

The View log displays data from the Knowledge Use \[kb\_use\] table. By default, all the records in the Knowledge Use \[kb\_use\] table are retained. Activating the data retention policy for the kb\_use table deletes records that you no longer need. The deleted data is not visible on the reports used in dashboards such as Self-Service Analytics for customer service and Knowledge Management dashboards.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Table Cleanup**.

2.  In the **Tablename** column, search for `kb_use` and click the **kb\_use** link.

3.  On the Auto Flush form, activate the kb\_user table cleanup job by selecting the **Active** check box.

4.  Adjust the amount of time the system waits before deleting the records by modifying the value in the **Age in seconds** field.

    By default, the **Age in seconds** field value is set to 31,536,000 seconds \(equivalent to 365 days\). For more information, see [Autoflush form](https://www.servicenow.com/docs/access?context=atf-auto-flush&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

    If the **glide.knowman.view\_age.days** property, which sets the number of days used when summing article views, is active, the **Age in seconds** field value must be larger than that property's value. For more information, see [Knowledge Management properties](../reference/r_KnowledgeProperties.md#)

    .

5.  Click **Update**.


**Parent Topic:**[View knowledge logs](view-knowledge-logs.md)

