---
title: Create Core UI dashboards on upgraded instances
description: On upgraded instances, including ones fully migrated to Platform Analytics, you can create Core UI dashboards from the Platform Analytics Dashboards library. You can create shareable dashboards with data visualizations, filters, and other existing elements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-core-ui-db-on-migrated-instance.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Create Core UI dashboards on upgraded instances

On upgraded instances, including ones fully migrated to Platform Analytics, you can create Core UI dashboards from the Platform Analytics Dashboards library. You can create shareable dashboards with data visualizations, filters, and other existing elements.

## Before you begin

A ServiceNow AI Platform administrator should create the **com.snc.par.coreui.dashboard\_create.enabled** property and set it to `true`. Otherwise, only dashboard\_admin users or higher can create Core UI dashboards, and only directly in the Dashboards \[pa\_dashboards\] table.

Role required: If the **com.snc.par.coreui.dashboard\_create.enabled** system property is `true`, any user with an internal role can create Core UI dashboards.

## About this task

**Important:** You cannot create Core UI dashboards on instances that were net new on Xanadu or later. On instances that were net new on older releases, you can continue to create Core UI dashboards, even if the instance was fully migrated to Platform Analytics.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Select **Create dashboard**.

3.  In the New dashboard modal, select **Core UI** and then select **Create dashboard**.

    \[Omitted image "create-core-ui-db-from-library.png"\] Alt text: Create a Core UI dashboard on migrated instance

    The form for a new Core UI dashboard opens.

4.  Follow the instructions in the topic [Create or configure a responsive dashboard in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateADashboard.md) to create your dashboard.


**Parent Topic:**[Common dashboard tasks in the in-line editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/common-dashboard-tasks.md)

**Related topics**  


[Create a dashboard with the in-line editor]()

[Edit Platform Analytics dashboards]()

[Share a Platform Analytics dashboard]()

[Duplicate a Platform Analytics dashboard]()

[Print a Platform Analytics dashboard]()

[Export a Platform Analytics dashboard]()

[Schedule the export of dashboards and data visualizations]()

[Bookmark a Platform Analytics dashboard]()

[Delete a Platform Analytics dashboard]()

