---
title: Create an HR case from Universal Request
description: Restore service to a customer as soon as possible. After creating the HR case, you can investigate potential solutions.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Universal Request for HR Service Delivery, Integrate with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Create an HR case from Universal Request

Restore service to a customer as soon as possible. After creating the HR case, you can investigate potential solutions.

## Before you begin

-   Role required: routing\_agent and sn\_hr\_core.case\_writer

-   Activate the Universal Request \(com.snc.universal\_request\) and Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugins.

## Procedure

1.  Navigate to **Universal Requests** &gt; **All**.

2.  Open the universal request record from which you want to create an HR case.

3.  Click **Create HR case**.

4.  Fill in the fields on the HR case form.

    **Note:** The **Employee Information** field values are automatically copied from the universal request to the HR case.

    |Field|Description|
    |-----|-----------|
    |COE|The Center of Excellence|
    |HR service|The HR service type|
    |Opened for|The person the ticket is opened for|
    |Subject person|The subject person|
    |Work notes|Other notes if any|

5.  Click **Submit**.

    The universal request number from which the HR case is created appears in the**Universal Request** field on the HR case form. The HR case number appears in the **Primary Ticket** field on the universal request form and also under the **Associated Tickets** related list.


**Parent Topic:**[Universal Request for HR Service Delivery](../concept/universal-request-hr.md)

