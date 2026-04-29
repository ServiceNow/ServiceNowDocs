---
title: Use External Interface to push records into a third-party system
description: Use External Interface to view details of records that are being pushed from ServiceNow into a third-party system.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Enterprise Service Management Integrations Framework, Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Use External Interface to push records into a third-party system

Use External Interface to view details of records that are being pushed from ServiceNow into a third-party system.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Integrations Framework** &gt; **External Interface**.

2.  On the form, view the fields:

    |Field|Description|
    |-----|-----------|
    |Service|OnDemand push service that is invoked to interact with a third-party system.|
    |Source table name|Source table in which the record is stored.|
    |Table Sys ID|Sys ID of the table record that has been modified. A combination of **Source table name** and **Table Sys ID** is used to identify and push the modified record into a third-party system.|
    |Status|Current status of the push, such as completed or pending.|
    |Error message|Error message displayed when the push failed.|
    |Error code|Error code displayed when the push failed.|


## What to do next

The Trigger External Interfaces flow automatically:

-   Identifies records whose Status is Pending, Service is Active, and Service type is OnDemand Push from the External Interface \[sn\_hr\_integr\_fw\_ext\_interface\] table.
-   Pushes the identified records into third-party system.

