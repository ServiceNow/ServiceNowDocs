---
title: Activate the Business application candidate agent
description: Activate the Business application candidate agent to begin automatic discovery and matching business applications with application services. Both the Data Synchronization and Processing jobs must be activated together to function properly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/now-assist-for-configuration-management-database-cmdb/na-cmdb-agent-biz-app-candidate-act.html
release: australia
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 1
keywords: [activation, scheduled jobs, Business application candidate agent, configuration, ServiceNow Otto for CMDB]
breadcrumb: [Configure, ServiceNow Otto for Configuration Management Database \(CMDB\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Activate the Business application candidate agent

Activate the Business application candidate agent to begin automatic discovery and matching business applications with application services. Both the Data Synchronization and Processing jobs must be activated together to function properly.

## Before you begin

Do your best to update application service and business application records.

Role required: `admin`

## About this task

The Data Synchronization and App Service Processing jobs aren't active by default. You must manually activate them to start the agent. The two jobs are automatically kept in sync — activating one also activates the other.

When you activate the jobs, the Data Synchronization job runs first to copy and index your app services and business applications. Once indexing is complete, the Processing job begins generating recommendations. On a large instance with hundreds of thousands of app services, the first full cycle may take several days.

## Procedure

1.  Navigate to **Scheduled Jobs**.

2.  In the list, find **App Service Data Synchronization** and open it.

    If you have many scheduled jobs, search for "App Service" to filter the list.

3.  Set the **Active** field to **true**.

4.  Select **Save**.

5.  Verify that the **App Service Processing** job also shows **Active** as true.

    The two jobs are kept in sync automatically. Both jobs are now running. The Data Synchronization job executes first to index your data. The Processing job begins once indexing is complete.


## Result

The Business application candidate agent is now active. The Data Synchronization job runs first to copy and index your app services and business applications. Once complete, the Processing job begins generating business app recommendations.

On a large instance, the first full synchronization and processing cycle may take several hours or even days. You can monitor progress by checking the work queue tables.

**Parent Topic:**[Configuring ServiceNow Otto for CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/now-assist-for-configuration-management-database-cmdb/now-assist-cmdb-configuring.md)

