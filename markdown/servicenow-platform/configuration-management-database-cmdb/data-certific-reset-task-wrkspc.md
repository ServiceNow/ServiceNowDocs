---
title: Reset a certification task
description: Reset a certification task to restart the certification process for the task. Reset sets all certification results for the task to 'Review not completed', removes any added comments, and adds the task to the list of tasks that need review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/data-certific-reset-task-wrkspc.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-07-19"
reading_time_minutes: 1
breadcrumb: [Data Certification experience in a workspace, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Reset a certification task

Reset a certification task to restart the certification process for the task. Reset sets all certification results for the task to 'Review not completed', removes any added comments, and adds the task to the list of tasks that need review.

## About this task

Resetting a data certification task doesn't affect any field values that were updated during certification.

## Before you begin

The task that you want to reset must have at least one attribute that is already reviewed \(certified or failed\).

Role required: data\_manager\_user or a user that has access to the task. For information about configuring user assignments for policy tasks, see [Create a CMDB Data Manager policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/data-manager-create-policy-wrkspc.md).

## Procedure

1.  Locate the task that you want to reset.

    Use either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace**, then select **My Work** in the CMDB Workspace menu bar.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel select the Tasks icon. In the Tasks navigation panel select **Certification** and on the Data Certification page, select the Certification tasks tab and then select a certification task.
2.  Select **Reset** on the task page.

3.  In the Confirm certification task reset dialog box select **Confirm**.


