---
title: Manage HAM advisor scope in CMDB success advisor
description: Manage the scope of your advisor for Hardware Asset Management \(HAM\) by editing model categories in CMDB success advisor to support your targeted HAM outcomes.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up advisor, Use HAM advisor, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage HAM advisor scope in CMDB success advisor

Manage the scope of your advisor for Hardware Asset Management \(HAM\) by editing model categories in CMDB success advisor to support your targeted HAM outcomes.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

Control which resource and model categories are included in your HAM advisor dashboard in CMDB success advisor. You can add or remove entire resource categories or fine-tune the selection by including or excluding specific model categories within a resource category. Resource categories may be opted in or out based on your hardware asset manager's preferences. This flexibility enables you to customize the dashboard to display only the most relevant HAM data.

## Procedure

1.  On the CMDB success advisor landing page, select **Edit model categories** within the HAM card.

    See [Viewing the CMDB success advisor landing page](../concept/cmdb-sa-landing-page.md).

2.  In the Edit model categories dialog box, add or remove categories to update your model category selection.

    |Purpose|Action|Data coverage|
    |-------|------|-------------|
    |Add an opted-in resource category or an available resource category|Select the check box for the resource category to include all its model categories.|Includes all model categories associated with the selected resource category.|
    |Expand model category selection|Select **&gt;** to expand a resource category, then select check boxes for specific model categories.|Includes only the selected model categories associated with a resource category.|
    |Narrow down model category selection|Select **&gt;** to expand a resource category, then clear check boxes for specific model categories.|Excludes only the model categories cleared from a resource category.|
    |Remove an opted-out or available resource category|Clear the check box for the resource category.|Excludes all model categories associated with the removed resource category.|
    |Remove a selected model category|Select the X icon next to the category in the **Selected** column.|Model category is removed from scope.|

3.  To remove a model category, select the X icon next to the category in the **Selected** column.

4.  Select **Save** to apply the changes.


## Result

The HAM dashboard in CMDB success advisor is updated to reflect the data based on the model category selection.

