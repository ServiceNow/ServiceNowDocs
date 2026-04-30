---
title: Create a BMC Remedy object in your ServiceNow instance
description: Manage other objects in BMC Remedy from your ServiceNow instance by creating the required object.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [BMC Remedy Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Create a BMC Remedy object in your ServiceNow instance

Manage other objects in BMC Remedy from your ServiceNow instance by creating the required object.

## Before you begin

Role required: admin or Remedy\_Admin

## About this task

By default, the BMC Remedy spoke supports the change request, incident, and problem objects. To manage other objects, such as Product Catalog, create an object in your ServiceNow instance.

## Procedure

1.  Navigate to **All** &gt; **BMC Remedy Spoke** &gt; **Objects**.

2.  Click **New**.

3.  On the form, fill these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the required form. This value is unique to each object. For example, the form value for Product Catalog is `PCT:Product Catalog`.|
    |Label|Label name to identify the record.|
    |Creatable|Option to create records in the object. Select the option to create records and use the object in your flows.|

4.  Click **Submit**.


