---
title: Get insights into your vendors' performance
description: Get insights into process bottlenecks and find potential areas that you could optimize. You can also view variation analysis.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Identifying bottlenecks using Process Mining integration with Vendor Management Workspace, Managing vendors using Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Get insights into your vendors' performance

Get insights into process bottlenecks and find potential areas that you could optimize. You can also view variation analysis.

## Before you begin

Role required: sn\_process\_optimization\_analyst

-   The **Process Mining - VM Remine Projects** job fetches projects that have not been mined based on the settings in the **sn\_itsm\_vendor.po\_mining.run\_frequency** system property. For more information, see [Installed with Vendor Management Workspace](../reference/installed-w-vendor-manager-configurable-workspace.md).
-   You must have mined the project for that KPI group for which you want to analyze process insights. For more information, see [Create a Process Mining project for a KPI group](create-project-po-vmw.md).

## About this task

The data is mined starting with the beginning of the previous month. For example, if the current date is June 26, 2023 then the data is mined starting at May 1, 2023.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Manager Workspace**.

2.  Select the List icon.

3.  Go to **Vendors** &gt; **All Vendors**.

4.  Select the vendor for which you want to analyze process insights.

5.  Drill down into a KPI, for example, Total incidents created.

6.  Select the **Process analysis** tab and perform process insights and variation analysis.

    **Note:**

    -   Select the **Vendor Breakdown** tab to view the details of the relationship of vendors to a table.
    -   Process mining can only be performed on KPIs based on the incident table.
    You can analyze the process insights for the last 30 days, excluding the current day, for which you’ve mined the data. For more information on business insights, see [View business insights](https://www.servicenow.com/docs/access?context=view-business-findings&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).


**Parent Topic:**[Identifying bottlenecks using Process Mining integration with Vendor Management Workspace](use-process-optimization-vmw.md)

**Related topics**  


[Analyze and get process insights](https://www.servicenow.com/docs/access?context=analyze-get-process-insights&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

