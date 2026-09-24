---
title: Limit conflict detection to a change model state
description: Use the Allow Conflict Detection attribute to limit conflict detection to a specific change model state. Conflict detection then runs only when a change request reaches that state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/limit-conflict-detection-state.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Allow Conflict Detection, change model, model state attribute, conflict detection]
breadcrumb: [Change lockdown conflict detection, Change lockdown, Configure, Change Management, IT Service Management]
---

# Limit conflict detection to a change model state

Use the Allow Conflict Detection attribute to limit conflict detection to a specific change model state. Conflict detection then runs only when a change request reaches that state.

## Before you begin

You must have a change model configured with at least one state.

Role required: admin.

## About this task

Without the **Allow Conflict Detection** attribute, conflict detection runs whenever the state, the configuration item, or the planned start or end date of a change request changes, in any state. Adding the attribute to a single state narrows conflict detection to that state, so it does not run in earlier or later states.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Change Models**.

2.  Open the change model to configure.

    For example, open the Emergency change model.

3.  On the **Model States** tab, open the state on which conflict detection is to run.

    The related list shows each state with its **State label**, whether it is the **Initial state**, and its **Sequence**.

4.  On the **Attributes** tab, select **New**.

5.  In the **Attribute** field, select **Allow Conflict Detection**.

6.  Select the **Active** check box.

7.  Select **Submit**.


**Parent Topic:**[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/lockdown-conflict-detection.md)

**Related topics**  


[Change lockdown conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/lockdown-conflict-detection.md)

