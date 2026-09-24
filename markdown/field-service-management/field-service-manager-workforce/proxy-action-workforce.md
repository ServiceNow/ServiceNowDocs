---
title: Complete a proxy action in Workforce
description: Perform a work order task action for a technician who can't act themselves. The action is logged as performed by you on the technician's behalf, and the task stays assigned to the technician.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/field-service-manager-workforce/proxy-action-workforce.html
release: brazil
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Using the team calendar, Managing agents and tasks from Workforce, Managing workforce, Use, Field Service Management]
---

# Complete a proxy action in Workforce

Perform a work order task action for a technician who can't act themselves. The action is logged as performed by you on the technician's behalf, and the task stays assigned to the technician.

## Before you begin

Role required: wm\_basic

## About this task

A proxy policy must already authorize you to act on the technician's work order tasks. If you don't see proxy actions on a task, ask your administrator.

## Procedure

1.  Navigate to Managers, navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **Workforce**.

2.  Select a task.

3.  Select the **More actions** icon.

4.  Select the proxy action you want to take.

    **Note:** A confirmation message names the technician and states that the action will be logged as performed by you on their behalf.

5.  Confirm the pop-up, or complete the form, for the action you selected.

    |Action|What to do|
    |------|----------|
    |**Accept**|Confirm the action. No additional fields are required.|
    |**Reject**|Select a reason for rejecting the task and enter any additional details.|
    |**Start travel / Start work**|Enter the actual time the action occurred. The field displays the technician's time zone so you can enter the correct time even if you're in a different time zone.|
    |**Close complete**|Enter the actual work end time and closure notes.|
    |**Close incomplete**|Enter the actual work end time, select whether to create a follow-on task, and enter a reason for the incomplete closure.|


## Result

The action is recorded, and the activity stream logs it with your name, the action, and the technician's name.

**Related topics**  


[Proxy actions in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/proxy-actions-fsm.md)

[Configure proxy actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/configure-proxy-fsm.md)

