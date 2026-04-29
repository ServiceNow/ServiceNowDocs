---
title: Create a business rule for your service
description: Create a business rule on the service table to attach the newly created department ticket with a universal request.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create a business rule for your service

Create a business rule on the service table to attach the newly created department ticket with a universal request.

## Before you begin

Role required: admin

## About this task

You can create a business rule for your service for any of the following reasons.

-   Provide a unified and simplified ticketing experience for your requester by configuring UR creation from all channels.
-   Enable agents to transfer the primary ticket to other departments if the original request was initially sent to the wrong department by the requester.
-   Facilitate cross-departmental reporting on the overall SLA if the ticket is transferred between departments.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  In the **Name** field, enter your business rule name.

4.  Select your service table from the **Table** list.

5.  Select **Advanced**.

6.  On the **When to run** tab, in the **When** condition select `after` and select the **insert** check box.

    This action specifies that the business rules should run after the insert or update.

7.  On the **Advanced** tab, add your condition.

    For example, add the below condition in the **Condition** field.

    `!current.universal_request.nil() && current.universal_request.primary_task.nil()`

8.  Enter the script in the **Script** field that you want to run when the defined condition is true.

    For example, add the below script to attach the service ticket as a primary ticket for UR.

    `(function executeRule(current, previous /*null when async*/) { var urUtilsApi = new sn_uni_req.UniversalRequestUtils(); urUtilsApi.attachPrimaryTicket(current.universal_request, current.getUniqueValue(),null,true); })(current, previous);`

9.  Click **Update**.

    For more information on other fields of this form, see [Create a business rule](https://www.servicenow.com/docs/access?context=c_BusinessRules&version=australia&pubname=australia-build-workflows&section=t_CreatingABusinessRule&ft:locale=en-US).


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)

