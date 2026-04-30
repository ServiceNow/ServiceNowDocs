---
title: Create a legal request from a universal request
description: Create a legal request from a universal request to get the Legal department's assistance in resolving the request.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Universal Request for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Create a legal request from a universal request

Create a legal request from a universal request to get the Legal department's assistance in resolving the request.

## Before you begin

Ensure you have the Universal Request application installed and [related configuration for legal services](configure-universal-request-legal.md) completed by the administrator.

An employee has [submitted a universal request](../../universal-request/task/ur-create-universal-request-record.md) and the universal ticket is assigned to you.

**Important:** The routing agent with the required roles must also be a member of the Legal Routing Group assignment group.

Role required: sn\_lg\_ops.legal\_user and sn\_uni\_req.universal\_request\_write

## About this task

A routing agent can also create a legal request from a universal request through the Agent mobile app. For creating legal ticket for a complaint, see [Create an ethics legal matter from a universal request](../../legal-investigations/task/create-legal-ticket-universal-request.md).

## Procedure

1.  Navigate to **All** &gt; **Universal Request** &gt; **Assigned to me**.

2.  Open the universal request from which you want to create a legal request.

3.  Click **Create Legal Ticket**.

4.  In the Create Legal Ticket dialog box, fill in the fields.

    1.  From the **Request type** list, select a legal request type.

    2.  In **Additional comments**, enter details about the service and support required from the Legal department.

5.  Click **Create**.


## Result

-   A legal request is created and becomes the primary ticket for the universal request. The legal request number is populated in the **Primary Ticket** field.
-   The state of the universal request changes to In Progress.
-   The **State reason** field displays with the pre-populated value Primary Ticket - In Progress.

## What to do next

In the Legal department, the legal request is assigned a legal fulfiller. The assigned legal fulfiller [works on the legal request](work-on-legal-request.md) and provides the resolution, or transfers the legal request to another department or back to the Universal Request.

To transfer the general legal request back to the Universal Request with external storage enabled, activate the **Name UR Transfer Post Processor** script action to sync the attachments. The script action is available in **All** &gt; **Event** &gt; **Script Actions**.

**Parent Topic:**[Universal Request for Legal Service Delivery](../concept/universal-requests-legal.md)

