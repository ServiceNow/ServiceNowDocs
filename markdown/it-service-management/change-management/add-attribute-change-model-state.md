---
title: Add an attribute to a change model state
description: Assign a change model attribute to a state in a change model so that scripts can check for the attribute when a change request is in that state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/add-attribute-change-model-state.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [change model attributes, model states, change model]
breadcrumb: [Change model attributes, Create a Change model, Configure, Change Management, IT Service Management]
---

# Add an attribute to a change model state

Assign a change model attribute to a state in a change model so that scripts can check for the attribute when a change request is in that state.

## Before you begin

The attribute must exist in the **Change Model Attributes** list.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Models** &gt; **Change Models**.

2.  Open the change model that you want to update, for example, **Normal**.

3.  In the **Model States** related list, expand the state that you want to add the attribute to.

    The expanded state shows the **Attributes**, **State Transitions**, and **State Field Policies** lists. If another list is displayed, select the list context menu icon and select **Attributes**.

4.  In the **Attributes** list, select **Edit**.

5.  Move the attribute to the selected list and save your changes.

    The attribute appears in the **Attributes** list for the state, with **Active** selected.

6.  Open the attribute record and clear the **Active** check box to stop applying the attribute to the state without removing it.


## What to do next

Reload any open change requests that use the model to see the updated behavior.

**Parent Topic:**[Change model attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-model-attributes.md)

