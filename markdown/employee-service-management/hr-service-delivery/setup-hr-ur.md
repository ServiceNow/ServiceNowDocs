---
title: Custom configurations in Universal Request
description: Transferring and state mappings are preconfigured for all the base system HR states. Do these configurations only when you have a custom state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/setup-hr-ur.html
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Universal Request for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Custom configurations in Universal Request

Transferring and state mappings are preconfigured for all the base system HR states. Do these configurations only when you have a custom state.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

If you have created COEs \(Center of Excellence\), then create service configurations, state mappings, and transfer configurations as well. In case you have activated the Predictive Intelligence plugin, configure the service assignment groups by referring to [Train the classification solution to predict the assignment group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/universal-request-for-hr-service-delivery/train-ur-classification-soln.md).

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Administration**.

2.  Create your service set and services for Universal Request.

3.  Assign the assignment groups for service sets and services.

4.  Assign roles to UR users.

5.  Map a custom state to that of a universal request.

    The following image is an example of a default state mapping. The **Suspended**, **Work in Progress**, and **Awaiting Approval** states of an HR case are mapped to **In Progress** state of a Universal Request.

    \[Omitted image "ur-hr-mapping.png"\] Alt text: State mapping

6.  Set the transfer configuration for any custom state of an HR case.

    This transfer configuration allows you to determine what happens to the departmental ticket when the request is transferred to another department or back to UR.

    If an HR case is being transferred with resolution, the state of the HR case automatically changes to **Awaiting Acceptance**. If an HR case is being transferred without a resolution, the state of the HR case automatically changes to **Closed Incomplete**.

7.  Create record producers specific to an HR service.

    A record producer is a specific type of catalog item that allows end users to create task-based records from the service catalog. On the record producer, if you select the **Create Universal Request** check box, an HR case created from that record producer automatically creates a universal request record.

    Following is an example of a record producer for General Inquiry HR service. When a user selects the catalog item as General Inquiry and creates a ticket, automatically a universal request is created and associated to that HR case.

    \[Omitted image "setup-hr-ur7.png"\] Alt text: Create record producers specific to HR.


**Parent Topic:**[Universal Request for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/universal-request-hr.md)

