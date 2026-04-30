---
title: Enable transfer of a legal request
description: As a admin, configure business rule to enable transfer of general legal request to contract practice area.
locale: en-US
release: xanadu
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a legal contract intake workflow, Configure Contract Management Pro for Legal Service Delivery, Contract Management Pro for Legal Service Delivery, Integration of Legal Service Delivery with ServiceNow applications, Legal Service Delivery, Employee Service Management]
---

# Enable transfer of a legal request

As a admin, configure business rule to enable transfer of general legal request to contract practice area.

## Before you begin

Role required: admin

## About this task

The business rule should be configured only if you have custom record producer that will be used to generate a contract request. For information on how to create a custom record producer, see [Create or modify a record producer for legal services through Classic environment](../../legal-request-management/task/create-record-producer-legal-request.md) and [Create or modify a record producer for legal services through Catalog Builder](../../legal-request-management/task/create-record-producer-catalog-builder-legal.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Open the **Initializing Legal Contract** business rule.

3.  In the **When to run** tab, add a new OR condition for the custom record producer.

    1.  Set the following filter condition: **\[Category\]\[is\]\[&lt;record-producer&gt;\]**.

    2.  Select **AND**.

    3.  Set the following filter condition: **\[Questions\]\[&lt;record-producer&gt;\]\[&lt;mandatory-question&gt;\]\[is not empty\]**.

4.  Select **Update** to save the business rule.


