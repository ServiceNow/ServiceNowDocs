---
title: Create associated tickets from an HR case
description: From an HR case that is the primary ticket of a universal request, create tickets for another department and associate them to the same universal request as the HR case. This feature enables agents from various departments to collaborate and work on their tickets in parallel. It also enables organizations to trace back efforts against a single universal request.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-14"
reading_time_minutes: 1
breadcrumb: [Universal Request for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Create associated tickets from an HR case

From an HR case that is the primary ticket of a universal request, create tickets for another department and associate them to the same universal request as the HR case. This feature enables agents from various departments to collaborate and work on their tickets in parallel. It also enables organizations to trace back efforts against a single universal request.

## Before you begin

Role required: sn\_hr\_core.case\_writer

Logged in user is the member of the **Assignment group** or **Assigned to** fields.

## Procedure

1.  Open an HR case.

2.  Click **Create Associated Ticket**.

3.  In the **Create Associated Ticket** dialog box, provide the following details:

    |Field|Description|
    |-----|-----------|
    |Department|Department for which you want to create a ticket.|
    |Short description|Purpose of creating the ticket.|
    |Description|More details pertaining to the ticket.|
    |Work notes|Updates that you want to share with the department for which you are creating the ticket.|

4.  Click **Create**.

    A ticket is created for another department. This ticket is automatically tied to a universal request and appears in the **Associated Tickets** related list in a universal request.


**Parent Topic:**[Universal Request for HR Service Delivery](../concept/universal-request-hr.md)

