---
title: Enable automatic action plan creation
description: You can configure the Create Journey Accelerator Action Plan template so that a plan is automatically created from a lifecycle event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/journey-accelerator/enable-template-for-auto-plan-creation.html
release: zurich
product: Journey Accelerator
classification: journey-accelerator
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage audience-specific templates, Configure, Journey Accelerator, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Enable automatic action plan creation

You can configure the Create Journey Accelerator Action Plan template so that a plan is automatically created from a lifecycle event.

## Before you begin

The Create a new action plan for your employee activity must be active. See, [Activate the Create a new action plan for your employee activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/journey-accelerator/activate-create-ja-plan-activity.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Livecycle Events** &gt; **Administration** &gt; **Manage HR Templates**.

2.  Open the **Create Journey Accelerator Plan** template.

3.  Set **Create plan automatically**.

    -   Set **Create plan automatically** to true to automatically create a plan when the lifecycle event activity is created.
    -   Set **Create plan automatically** to false create a to-do for Opened for person \(manager\) in the HR case.
4.  Click **Update** to apply and save your changes.

    When **Create plan automatically** is set to true, an action plan is automatically created for the activity in a lifecycle event.


## What to do next

[Open an HR case to create a Journey Accelerator action plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/hr-service-delivery/create-journey-accelerator-plan.md)

