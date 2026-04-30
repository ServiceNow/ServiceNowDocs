---
title: Inbound request states
description: An inbound request transitions through a series of states as ServiceNow AI Platform processes the asynchronous order received via an API.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-23"
reading_time_minutes: 1
breadcrumb: [Order Management reference, Reference, Sales Customer Relationship Management]
---

# Inbound request states

An inbound request transitions through a series of states as ServiceNow AI Platform processes the asynchronous order received via an API.

|Field|Description|
|-----|-----------|
|New|The inbound request has been received via API and is waiting to be picked up by the scheduled job.|
|In progress|The scheduled job has picked up the inbound request and is processing the order.|
|Completed|The order was created successfully.|
|Error|An error occurred while creating the order. The inbound request exits the processing cycle.|
|Pending|The inbound request is waiting for a condition to be met before processing can continue.|

**Parent Topic:**[Order Management reference](order-mgt-reference.md)

**Related topics**  


[Asynchronous order processing for large customer and consumer orders](../concept/asynchronous-order-processing.md)

