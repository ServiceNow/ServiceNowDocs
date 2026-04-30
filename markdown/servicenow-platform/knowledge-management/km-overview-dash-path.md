---
title: Update the navigation path for the Knowledge Management Overview dashboard
description: Update the navigation path to access the Knowledge Management Overview dashboard.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Overview dashboard, Knowledge Management Platform Analytics Solutions, Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Update the navigation path for the Knowledge Management Overview dashboard

Update the navigation path to access the Knowledge Management Overview dashboard.

## Before you begin

-   Activate the knowledge overview \(com.sn\_knowledge\_overview\) plugin.
-   If you are upgrading from a previous release, you must update the knowledge overview entry in the Modules \(sys\_app\_module\) table.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Modules**.

2.  On the Modules page, in the **Title** field, enter `overview`.

3.  In the **Application menu** field, enter `knowledge`.

4.  Open the **Overview** module.

5.  In the Module Overview page, click **Link Type**.

6.  In the **Link type** field, select **URL \(from Arguments\)** from the list.

7.  In the **Arguments** field, enter `now/platform-analytics-workspace/dashboards/params/edit/false/sys-id/5d5e18458731fd51a2522b5a4309cacc`.

8.  Select **Update**.


## Result

The navigation path for the Knowledge Management dashboard is updated to **All** &gt; **Knowledge** &gt; **Administration** &gt; **Overview**.

