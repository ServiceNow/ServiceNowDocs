---
title: Configure a child HR service
description: Configure a service activity that is a child HR service.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-08"
reading_time_minutes: 1
breadcrumb: [Configure a service activity for an HR service, Configure an HR service, HR service configuration, HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure a child HR service

Configure a service activity that is a child HR service.

## Before you begin

Role required: sn\_hr\_core.admin

**Note:** This feature is only available when the Human Resources Scoped App: Lifecycle Events \(com.sn\_hr\_lifecycle\_events\) plugin is activated.

## Procedure

1.  On the Service Activity form, set the **Activity type** field to `Child HR Service`.

2.  Fill in the fields on the form, as appropriate.

<table id="table_s4y_5ml_mfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity type

</td><td>

Set the value to **Child HR Service**.

</td></tr><tr><td>

Child HR service

</td><td>

Name of the child HR service that the service activity is associated with.

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
-   Service activities with identical order numbers are made available at the same time.


</td></tr></tbody>
</table>3.  Click **Submit** or **Update** on the Service Activity form.

4.  Click **Update** on the HR Service form.


**Parent Topic:**[Configure a service activity for an HR service](configure-service-activity-for-hr-service.md)

