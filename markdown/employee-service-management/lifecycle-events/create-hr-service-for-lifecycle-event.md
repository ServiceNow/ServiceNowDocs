---
title: Configure an HR service for a lifecycle event
description: Create a corresponding HR service so that the lifecycle event can be requested for service. For example, the lifecycle event for New Hire Onboarding has a corresponding HR service also named New Hire Onboarding. When an HR case for that HR service is created, the HR case will be fulfilled by the associated lifecycle event.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure an HR service for a lifecycle event

Create a corresponding HR service so that the lifecycle event can be requested for service. For example, the lifecycle event for New Hire Onboarding has a corresponding HR service also named New Hire Onboarding. When an HR case for that HR service is created, the HR case will be fulfilled by the associated lifecycle event.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

HR services are the requests and assistance an HR organization provides its employees, and they are the starting point for HR case creation. You must create an HR service for a lifecycle event so that it can be requested for service. To learn more about HR services, including whether to make an HR service available for internal use only or for employee self-service, see [HR services](../concept/hr-service-administration.md).

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_y3w_hmd_qhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Fulfillment type

</td><td>

Set the value to `Lifecycle Event`.

</td></tr><tr><td>

Lifecycle event type

</td><td>

Select the lifecycle event you want to fulfill the HR service.**Warning:** If the lifecycle event type field of an HR service is the same as the lifecycle event \(LE\) type that’s being used in an LE activity, a loop can be created that causes memory issues.

</td></tr><tr><td>

COE

</td><td>

Select the COE you want the HR service to be categorized under.**Note:** An HR service for a lifecycle event can be associated with any HR Center of Excellence \(COE\).

</td></tr></tbody>
</table>4.  Fill in the other fields on the form, as appropriate.

    For further details on the form fields, see [Configure an HR service](configure-hr-service.md).

5.  Click **Submit** or **Update**.


**Parent Topic:**[Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md)

**Previous topic:**[Configure the rescind process for a lifecycle event](configure-rescind-for-a-lifecycle-event.md)

**Next topic:**[Configure an HR service for a journey](configure-hr-service-for-journey.md)

