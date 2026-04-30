---
title: Get started with CMDB success advisor setup for HAM
description: Set up your Hardware Asset Management \(HAM\) specific advisor dashboard by selecting model categories to define the HAM advisor scope.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-02-27"
reading_time_minutes: 2
breadcrumb: [Set up advisor, Use HAM advisor, CMDB success advisor, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Get started with CMDB success advisor setup for HAM

Set up your Hardware Asset Management \(HAM\) specific advisor dashboard by selecting model categories to define the HAM advisor scope.

## Before you begin

-   Install Hardware Asset Management \(sn\_hamp\) on your instance.
-   Obtain entitlement for Hardware Asset Management \(ham\_hamp\_license\).
-   Opt in HAM resource categories. See [Managing opt-in and opt-out resource categories for HAM in CMDB success advisor](../concept/cmdb-sa-ham-opt-categories.md)

Role required: sn\_cmdb\_admin

**Note:** In addition to the sn\_cmdb\_admin role, the pa\_data\_collector role is required to view the last updated data timestamp on the dashboard and pa\_viewer is required to filter data by model categories.

## About this task

Selecting model categories defines which hardware asset types CMDB success advisor monitors for HAM data quality. The selected categories determine the scope of the HAM advisor dashboard, including the KPIs, data integrations, and settings that are tracked.

**Important:** To determine which model categories to select, review the count of operational assets under each category in the Hardware Asset Workspace, or consult with your IT Asset Management \(ITAM\) or HAM administrator for guidance. See [Hardware Asset Workspace](https://www.servicenow.com/docs/access?context=using-ham-workspace&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

## Procedure

1.  On the CMDB success advisor landing page, select **Select model categories** within the HAM card.

    See [Viewing the CMDB success advisor landing page](../concept/cmdb-sa-landing-page.md).

2.  On the Select model categories dialog box, select a resource category to choose all its model categories or expand a resource category to select individual categories, then move them from the **Available resource and model categories** column to the **Selected** column.

    **Note:** If the Select model categories dialog box shows **No model categories available**, select **Opt in categories** to opt in at least one HAM license resource category, then return to this step.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add an available resource category|Select the check box for the resource category to include all its model categories.|Includes all model categories associated with the selected resource category.|
    |Expand model category selection|Select **&gt;** to expand a resource category, then select check boxes for specific model categories.|Includes only the selected model categories associated with a resource category.|
    |Narrow down model category selection|Select **&gt;** to expand a resource category, then clear check boxes for specific model categories.|Excludes only the model categories cleared from a resource category.|
    |Remove an opted-out or available resource category|Clear the check box for the resource category.|Excludes all model categories associated with the removed resource category.|
    |Remove a selected model category|Select the X icon next to the category in the **Selected** column or clear the check box for the category|Model category is removed from scope.|

    **Tip:** You can use the **Search** field to find specific categories. You can select up to 50 model categories.

3.  Select **Done** to build the CMDB success advisor for HAM dashboard.


## Result

The HAM data collection begins. The HAM advisor dashboard is populated after data collection completes.

