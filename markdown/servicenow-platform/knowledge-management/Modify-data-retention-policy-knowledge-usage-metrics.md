---
title: Modify the data retention policy for knowledge usage metrics
description: Remove unwanted and older data from the knowledge usage metrics \[kb\_usage\_metrics\] table through the data retention policy.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Collect knowledge usage metrics, User criteria diagnostics for Knowledge Management, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modify the data retention policy for knowledge usage metrics

Remove unwanted and older data from the knowledge usage metrics \[kb\_usage\_metrics\] table through the data retention policy.

## Before you begin

Role required: maint and admin

## About this task

Activating the data retention policy for the kb\_usage\_metrics table deletes records that you no longer need.

## Procedure

1.  Navigate to **All** &gt; **System Maintenance** &gt; **Table Cleanup**.

2.  In the **Tablename** column, search for `kb_usage_metrics` and click the **kb\_usage\_metrics** link.

3.  On the Auto Flush form, activate the kb\_usage\_metrics table cleanup job by selecting the **Active** check box.

4.  Adjust the duration the system waits before deleting the records by modifying the value in the **Age in seconds** field.

    By default, the **Age in seconds** field value is set to 2,592,000 seconds \(equivalent to 30 days\). For more information, see [Autoflush form](https://www.servicenow.com/docs/access?context=atf-auto-flush&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

5.  Click **Update**.


**Parent Topic:**[Collect knowledge usage metrics](Guest-user-diagnostic.md)

