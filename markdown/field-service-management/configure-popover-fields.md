---
title: Configure popover fields
description: Configure the fields that appear in task popovers across Dispatcher Workspace, including the task panel, calendar, and map markers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/configure-popover-fields.html
release: australia
product: Field Service Management
classification: field-service-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure popover fields

Configure the fields that appear in task popovers across Dispatcher Workspace, including the task panel, calendar, and map markers.

## Before you begin

Role required: admin

The system property sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.task\_panel\_card\_hover\_popover must be enabled to see popovers on the task card. The system property sn\_fsm\_disp\_wrkspc.dispatcher\_workspace.calendar\_event\_hover\_popover must be enabled to see popovers on events in the calendar. These fields are enabled by default. For more information, see [Properties installed with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatcher Workspace Configuration** &gt; **Task Popover Fields**.

    The fields you configure here drive the popover displayed on the task panel, calendar, and map markers in Dispatcher Workspace. The following six fields are included by default:

    |Name|Description|
    |----|-----------|
    |short\_description|A summary of the work order task.|
    |number|The unique identifier assigned to the work order task.|
    |expected\_start|The date and time the work order task is scheduled to begin.|
    |assignment\_group|The assignment group responsible for completing the work order task.|
    |location|The location where the work order task is to be performed.|
    |location.time\_zone|The time zone of the location where the work order task is to be performed.|

2.  Choose from the following.

<table id="choicetable_cn3_bdn_fjc"><thead><tr><th align="left" id="d40855e186">

Selection

</th><th align="left" id="d40855e189">

Action

</th></tr></thead><tbody><tr><td id="d40855e195">

**Select __New__**

</td><td>

1.  On the form, fill in the fields.
2.  Select **Submit**.


</td></tr><tr><td id="d40855e218">

**Select an existing field**

</td><td>

1.  Edit the field accordingly.
2.  Select **Update**.


</td></tr></tbody>
</table>    **Note:** Only the first 25 fields are displayed in the popover. If the configured fields exceed the maximum popover height of 800 pixels, a scroll bar appears so that dispatchers can scroll through the contents.

3.  Select a field and update the **Order** value to change the order in which fields appear in the popover.

    **Note:** Fields are displayed in ascending order based on this value. For example, a field with an order value of 10 appears before a field with an order value of 20.


