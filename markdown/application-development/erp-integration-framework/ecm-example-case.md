---
title: ERP Data Hub custom field example
description: ERP Data Hub helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub custom field example

ERP Data Hub helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by ERP Data Hub.

## Example of ERP custom data replatforming

In this example, a farmer grows grain to sell. The farmer has entries in a table for standard values, such as weight and sales price.

However, the sale price of grain depends on the moisture content of the grain. If it rains the day before grain is harvested, the farmer must adjust the sale price to reflect the moisture content. Thus, in addition to standard fields like **Date** and **Weight**, the legacy table that tracks the grain harvest on the ERP system must have a custom **Moisture %** field.

The farmer can use ERP Data Hub to connect to the legacy system of record and identify the table that contains the custom field. Then they can create an ERP model in ERP Data Hub with a remote table or an extraction table that contains the **Moisture %** field.

After they have the ERP model with custom data, they can use App Engine Studio or other ServiceNow products to quickly build an app that tracks their grain sales. The data that the grain sale app consumes still lives on the legacy system of record.

**Parent Topic:**[Exploring ERP Data Hub](exploring-erp-integration.md)

