---
title: Reactivate a deprecated activity
description: Orchestration activities that were converted to activity packs are deprecated for upgraded and new instances but can be reactivated for use in new workflows.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Deprecated Orchestration activities, Activate Orchestration, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Reactivate a deprecated activity

Orchestration activities that were converted to activity packs are deprecated for upgraded and new instances but can be reactivated for use in new workflows.

## Before you begin

Role required: workflow\_admin, admin

**Note:** Reactivation of deprecated activities for use in new workflows is discouraged. Legacy activities cannot use the unique features of the scoped applications, such as reuse of data from the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#) and input variable testing.

## Procedure

1.  Navigate to **All** &gt; **Workflow** &gt; **Administration** &gt; **Activity Definitions**.

2.  In the list of activities, clear the condition **Category !=deprecated** from the filter.

    ![Category filter for deprecated activities](../image/CategoryDeprecationFilter.png)

3.  Open the definition record for the activity you want to reactivate.

4.  Select the **What to Display** tab.

5.  In the **Category** field, replace the value **deprecated** with another category.

    This can be an arbitrary string.

6.  Click **Update**.

    The system creates a new category using the value provided and reactivates the activity, which becomes available in the **Core** tab of the Workflow Editor.


**Parent Topic:**[Deprecated Orchestration activities](../reference/r_OrchestrationBasicActivities.md)

