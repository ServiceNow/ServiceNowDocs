---
title: Manage HAM advisor scope in CMDB success advisor
description: Manage the scope of your advisor for Hardware Asset Management \(HAM\) by editing model categories in CMDB success advisor to support your targeted HAM outcomes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/cmdb-sa-ham-optimize-dashboard.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [manage HAM advisor scope, edit model categories, HAM advisor scope management]
breadcrumb: [Set up advisor, Use HAM advisor, Asset and CI management, Explore, Hardware Asset Management, IT Asset Management]
---

# Manage HAM advisor scope in CMDB success advisor

Manage the scope of your advisor for Hardware Asset Management \(HAM\) by editing model categories in CMDB success advisor to support your targeted HAM outcomes.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

Control which resource and model categories are included in the HAM advisor dashboard in CMDB success advisor. Add or remove entire resource categories, or include or exclude specific model categories within a resource category. Resource categories can be opted in or out based on hardware asset manager preferences.

## Procedure

1.  On the HAM advisor dashboard, select **Edit dashboard scope**.

2.  In the Edit dashboard scope dialog box, add or remove categories to update the model category selection.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add an opted-in resource category or an available resource category|Select the check box for the resource category to include all its model categories.|Includes all model categories associated with the selected resource category.|
    |Expand model category selection|Select **&gt;** to expand a resource category, then select check boxes for specific model categories.|Includes only the selected model categories associated with a resource category.|
    |Narrow down model category selection|Select **&gt;** to expand a resource category, then clear check boxes for specific model categories.|Excludes only the model categories cleared from a resource category.|
    |Remove an opted-out or available resource category|Clear the check box for the resource category.|Excludes all model categories associated with the removed resource category.|
    |Remove a selected model category|Select the X icon next to the category in the Selected column.|Model category is removed from scope.|

3.  If a confirmation check box appears under **Review and confirm changes**, select the check box.

    The check box appears only when the **com.snc.task.principal\_class\_filter** system property is set and your selection has an unsaved change.

    The check box label states how many model categories you're adding and removing. It also notes that added categories mark their CI classes as principal, which can affect CI filtering for incident, problem, and change \(IPC\) tasks.

    **Done** stays disabled until you select the check box. Changing your selection again clears the check box and disables **Done** until you select it again.

    Selecting the check box enables **Done**.

4.  Select **Done** to apply the changes.


## Result

The HAM dashboard in CMDB success advisor is updated to reflect the data based on the model category selection. Dashboard metrics refresh once daily when the **CMDB Advisor - HAM Daily Data Collection** scheduled job runs. The scheduled job invokes the **CMDB success advisor data collection for HAM** Performance Analytics job to recalculate the pre-aggregated indicators used throughout the dashboard. For more information about Performance Analytics jobs, see [Collecting indicator scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/now-intelligence/c_ClctData.md). Changes to your model category selection appear in the dashboard metrics after this job's next run, not immediately. For the full list of CMDB success advisor scheduled jobs, see [Components installed with CMDB success advisor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/cmdb-sa-components-installed.md).

