---
title: Configure an HR service for a journey
description: Create a corresponding HR service so that the lifecycle event can be requested for service as part of an employee's journey.
locale: en-US
release: yokohama
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Building a lifecycle event, Using Lifecycle Events, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure an HR service for a journey

Create a corresponding HR service so that the lifecycle event can be requested for service as part of an employee's journey.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

HR services are the requests and assistance an HR organization provides its employees, and they are the starting point for HR case creation. You must create an HR service for a lifecycle event so that it can be requested for service. To learn more about HR services, including whether to make an HR service available for internal use only or for employee self-service, see [HR services](../concept/hr-service-administration.md).

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Click **New**.

3.  On the HR Service form, provide the following field values.

<table id="table_y3w_hmd_qhb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Fulfillment type

</td><td>

Set the value to `Journey`.

</td></tr><tr><td>

Lifecycle event type

</td><td>

Select the Lifecycle event you want to fulfill the HR service.

</td></tr><tr><td>

Journey configuration

</td><td>

Select the Journey designer journey you want to associate with the Lifecycle event.

</td></tr><tr><td>

COE

</td><td>

Select the COE you want the HR service to be categorized under.**Note:** An HR service for a Lifecycle event can be associated with any HR Center of Excellence \(COE\).

</td></tr></tbody>
</table>    ![On the HR service form, set the Fulfillment type to Journey](../image/create-hr-service-for-jny.png)

4.  Fill in the other fields on the form, as appropriate.

    For further details on the form fields, see [Configure an HR service](configure-hr-service.md).

5.  Click **Submit** or **Update**.


**Parent Topic:**[Building a lifecycle event](../concept/hr-lifecycle-event-configuration.md)

**Previous topic:**[Configure an HR service for a lifecycle event](create-hr-service-for-lifecycle-event.md)

**Next topic:**[Using the Test Activity Sets tool for a lifecycle event activity set](../concept/hr-lifecycle-event-test-tool.md)

