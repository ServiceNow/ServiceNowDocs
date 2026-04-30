---
title: Configure a task
description: Configure a service activity that is a task.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure service activity, Configure an HR service, HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure a task

Configure a service activity that is a task.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  On the Service Activity form, set the **Activity type** field to `Task`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_n5h_tml_mfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity type

</td><td>

Set the value to **Task**.

</td></tr><tr><td>

Child task template

</td><td>

Name of the child task template that the service activity is associated with.**Note:** The HR task template automatically populates fields on the HR task form when the task is generated. See [Configure an HR task template](configure-hr-task-template.md) for more information.

</td></tr><tr><td>

Name

</td><td>

Name of the service activity.

</td></tr><tr><td>

Parent HR service

</td><td>

This field is automatically set to the parent HR service.

</td></tr><tr><td>

Order

</td><td>

Order number for when the service activity is made available. Lower numbered service activities are made available before higher numbered service activities.**Note:**

-   The current service activity must be closed, completed, accepted, or rejected before the next service activity is made available.
-   Service activities with the same order number will be grouped and when there is an approval activity in the group, approval will execute first, followed by others.


</td></tr></tbody>
</table>3.  Click **Submit** or **Update** on the Service Activity form.

4.  Click **Update** on the HR Service form.


**Parent Topic:**[Configure a service activity for an HR service](configure-service-activity-for-hr-service.md)

