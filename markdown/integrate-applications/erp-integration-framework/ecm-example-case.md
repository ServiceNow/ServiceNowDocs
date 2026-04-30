---
title: Zero Copy Connector for ERP custom field example
description: Zero Copy Connector for ERP helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record \(such as SAP\) to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by Zero Copy Connector for ERP.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP custom field example

Zero Copy Connector for ERP helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record \(such as SAP\) to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by Zero Copy Connector for ERP.

## Example of ERP custom data replatforming

In this example, a farmer grows grain to sell. The farmer has entries in a table for standard values, such as weight and sales price.

However, the sale price of grain depends on the moisture content of the grain. If it rains the day before grain is harvested, the farmer must adjust the sale price to reflect the moisture content. Thus, in addition to standard fields like **Date** and **Weight**, the legacy table that tracks the grain harvest on the ERP system must have a custom **Moisture %** field.

The farmer can use Zero Copy Connector for ERP to connect to the legacy system of record and identify the table that contains the custom field. Then they can create a model in Zero Copy Connector for ERP with a remote table or an extraction table that contains the **Moisture %** field.

After they have the model with custom data, they can use ServiceNow Studio or other ServiceNow products to build an app that tracks their grain sales. The data that the grain sale app consumes still lives on the legacy system of record.

**Parent Topic:**[Exploring Zero Copy Connector for ERP](exploring-erp-integration.md)

