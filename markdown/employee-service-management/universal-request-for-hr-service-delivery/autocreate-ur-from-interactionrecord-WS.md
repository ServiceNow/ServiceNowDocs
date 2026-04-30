---
title: Create universal request automatically for department tickets via other channels
description: Universal request is not automatically created when a fulfiller or employee creates a department ticket from channels other than the Service Portal or Virtual Agent topics. Create universal request automatically by adding the business rule to the specific service table, such as an Incident or a HR service.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Unified ticket experience setting, Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create universal request automatically for department tickets via other channels

Universal request is not automatically created when a fulfiller or employee creates a department ticket from channels other than the Service Portal or Virtual Agent topics. Create universal request automatically by adding the business rule to the specific service table, such as an Incident or a HR service.

## Before you begin

Role required: admin

## About this task

Create universal request automatically by adding the business rule to the specific service table, such as an Incident or a HR service. The universal request created is then automatically associated to the department ticket, such as an Incident or a HR case created in that table.

You may want to automatically create universal request in the following scenarios.

-   To provide a consistent user experience when viewing the UR ticket.
-   Transfer the department ticket at any time, as UR is already associated with the ticket.
-   Use cross-departmental SLA/OLA reporting for the UR, the department ticket, and any other tasks associated with the parent UR.

You can achieve this by using a business rule and the Universal Request API. For more information, see [UniversalRequestUtilsSNC API](https://www.servicenow.com/docs/access?context=UniversalRequestUtilsSNCScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

Follow the given steps to enable create universal request automatically from an interaction record.

## Procedure

1.  Modify the UI action of the department ticket to pass the URL parameter that is retrieved from the client script.

2.  Create an AJAX script include to set the data in the glide session.

3.  Create an onSubmit\(\) client script to fetch the URL parameter.

    For more information, see [Client scripts](https://www.servicenow.com/docs/access?context=client-scripts&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

4.  Set the URL parameter and the sys\_id to the glide session using the AJAX script include.

5.  Create a before insert business rule on the department ticket and retrieve the data from the glide session.

    ![Business Rule to create UR from interaction](../images/auto-create-business-rule.png)

6.  Create universal request record using the **UniversalRequestUtils** API and attach the universal request to the task.


**Parent Topic:**[Unified ticket experience setting](../concept/unified-ticket-experience.md)

**Related topics**  


[Email notification preferences for your service](../concept/ur-customize-email-notifcations.md)

[Automatically create universal request from an inbound email](../concept/create-ur-from-inbound-email.md)

[Configure a catalog item or record producer to create a universal request](../../service-catalog-management/task/create-ur-recordproducer.md)

