---
title: Create a business rule to automatically create universal request
description: Create a before insert business rule on the service table to automatically create a universal request when a ticket is raised from any of the available channels.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create a business rule to automatically create universal request

Create a before insert business rule on the service table to automatically create a universal request when a ticket is raised from any of the available channels.

## Before you begin

Role required: admin

## About this task

When a new request is submitted from the employee portal, this business rule validates if UR already exists. If there is no UR attached to the request, then the business rule automatically creates the UR and the department specific request is attached as the primary ticket.

UR is auto-created from any of the following channels:

-   ServiceNow AI Platform
-   Workspace
-   Virtual Agent
-   Email
-   Interaction
-   Self-service

You can automatically create a universal request in the following scenarios.

-   To provide a consistent user experience while viewing the UR ticket.
-   Transfer the department ticket seamlessly, as UR is already associated with the ticket.
-   Use cross-departmental SLA or OLA reporting for UR, department ticket, and any other tasks associated with the parent UR.

**Note:** By default, this business rule is shipped with HR Service Delivery and IT Service Management. Activate it to use it. For other departments, to use this capability, create or customize the given business rule for your specific department table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Click **New**.

3.  In the **Name** field, enter your business rule name.

4.  Select your service table from the **Table** list.

5.  Select **Advanced**.

6.  On the **When to run** tab, in the **When** condition select `before` and select the **insert** check box.

    This action specifies that the business rules should run before the insert.

7.  Enter the highest **Order** for the table.

    The order value is department specific.

8.  Add your condition.

    For example, add the below condition in the **Condition** field.

    `current.universal_request.nil()`

9.  Enter the script in the **Script** field that you want to run when the defined condition is true.

    For example, add the below script to attach the service ticket as a primary ticket for UR.

    `(function executeRule(current, previous /*null when async*/) { /* call UR API to create or attach Universal Request with inserted department record */ new sn_uni_req.UniversalRequestFieldsMappingUtils().attachUniversalRequest(current); })(current, previous);`

10. Click **Submit**.

    For more information on other fields of this form, see [Create a business rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/business-rules-classic/c_BusinessRules.md).


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)

