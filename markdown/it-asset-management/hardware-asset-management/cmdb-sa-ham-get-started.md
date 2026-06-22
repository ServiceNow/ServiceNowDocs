---
title: Get started with CMDB success advisor setup for HAM
description: Set up your Hardware Asset Management \(HAM\) specific advisor dashboard by selecting model categories to define the HAM advisor scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/cmdb-sa-ham-get-started.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Set up advisor, Use HAM advisor, Asset and CI management, Explore, Hardware Asset Management, IT Asset Management]
---

# Get started with CMDB success advisor setup for HAM

Set up your Hardware Asset Management \(HAM\) specific advisor dashboard by selecting model categories to define the HAM advisor scope.

## Before you begin

-   Install Hardware Asset Management \(sn\_hamp\) on your instance.
-   Obtain entitlement for Hardware Asset Management \(ham\_hamp\_license\).
-   Opt in HAM resource categories. See [Managing opt-in and opt-out resource categories for HAM in CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/cmdb-sa-ham-opt-categories.md)

Role required: sn\_cmdb\_admin

## About this task

Selecting model categories defines which hardware asset types CMDB success advisor monitors for HAM data quality. The selected categories determine the scope of the HAM advisor dashboard, including the KPIs, data integrations, and settings that are tracked.

**Important:** To determine which model categories to select, review the count of operational assets under each category in the Hardware Asset Workspace, or consult with your IT Asset Management \(ITAM\) or HAM administrator for guidance. See [Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-workspace.md).

## Procedure

1.  On the CMDB success advisor landing page, select **Select model categories** within the HAM card.

    See [Viewing the CMDB success advisor landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-landing-page.md).

2.  On the Select model categories dialog box, select a resource category to choose all its model categories or expand a resource category to select individual categories, then move them from the **Available resource and model categories** column to the **Selected** column.

    **Note:** If the Select model categories dialog box shows **No model categories available**, select **Opt in categories** to opt in at least one HAM license resource category, then return to this step.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add an available resource category|Select the check box for the resource category to include all its model categories.|Includes all model categories associated with the selected resource category.|
    |Expand model category selection|Select **&gt;** to expand a resource category, then select check boxes for specific model categories.|Includes only the selected model categories associated with a resource category.|
    |Narrow down model category selection|Select **&gt;** to expand a resource category, then clear check boxes for specific model categories.|Excludes only the model categories cleared from a resource category.|
    |Remove an opted-out or available resource category|Clear the check box for the resource category.|Excludes all model categories associated with the removed resource category.|
    |Remove a selected model category|Select the X icon next to the category in the **Selected** column or clear the check box for the category|Model category is removed from scope.|

    **Tip:** You can use the **Search** field to find specific categories. You can select up to 200 model categories.

3.  Select **Done** to build the CMDB success advisor for HAM dashboard.


## Result

The HAM data collection begins. The HAM advisor dashboard is populated after data collection completes. Initial data collection runs monthly. The frequency increases to daily after the first time you interact with the dashboard.

To update the scope after initial setup, select **Edit model categories** on the HAM advisor dashboard.

