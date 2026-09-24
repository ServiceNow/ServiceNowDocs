---
title: Complete proxy actions on Field Service Manager Mobile
description: Perform a work order task action for a technician who can't act themselves. The action is logged as performed by you on the technician's behalf, and the task stays assigned to the technician.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/proxy-action-manager.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [proxy actions, manager mobile, work order task]
breadcrumb: [Field Service Manager Mobile, Completing work on mobile, Use, Field Service Management]
---

# Complete proxy actions on Field Service Manager Mobile

Perform a work order task action for a technician who can't act themselves. The action is logged as performed by you on the technician's behalf, and the task stays assigned to the technician.

## Before you begin

Role required: wm\_manager, sn\_fsm\_tp.fsm\_territory\_resource\_manager

A proxy policy must already authorize you to act on the technician's work order tasks. If you don't see proxy actions on a task, ask your administrator.

## Procedure

1.  Open Field Service Manager Mobile.

2.  Open the work order task you want to take an action on.

3.  Choose the action to take.

    |Action|What to do|
    |------|----------|
    |**Accept**|Confirm the action. No additional fields are required.|
    |**Reject**|Select a reason for rejecting the task and enter any additional details.|
    |**Start travel / Start work**|Enter the actual time the action occurred, converted to the technician's time zone.|
    |**Close complete**|Enter the actual work end time and closure notes.|
    |**Close incomplete**|Enter the actual work end time, select whether to create a follow-on task, and enter a reason for the incomplete closure.|

4.  Confirm who to take the action on behalf of, and fill in the form.

5.  Select **Confirm**.


## Result

The action is taken on behalf of the person you selected.

**Related topics**  


[Proxy actions in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/proxy-actions-fsm.md)

[Configure proxy actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/configure-proxy-fsm.md)

