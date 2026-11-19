---
title: ERP Canvas custom field example
description: ERP Canvas helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by ERP Canvas.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/ecm-example-case.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring ERP Canvas, ERP Canvas, Building low-code applications, Developing your application, Building applications]
---

# ERP Canvas custom field example

ERP Canvas helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by ERP Canvas.

## Example of ERP custom data replatforming

In this example, a farmer grows grain to sell. The farmer has entries in a table for standard values, such as weight and sales price.

However, the sale price of grain depends on the moisture content of the grain. If it rains the day before grain is harvested, the farmer must adjust the sale price to reflect the moisture content. Thus, in addition to standard fields like **Date** and **Weight**, the legacy table that tracks the grain harvest on the ERP system must have a custom **Moisture %** field.

The farmer can use ERP Canvas to connect to the legacy system of record and identify the table that contains the custom field. Then they can create an ERP model in ERP Canvas with a remote table or an extraction table that contains the **Moisture %** field.

After they have the ERP model with custom data, they can use App Engine Studio or other ServiceNow products to quickly build an app that tracks their grain sales. The data that the grain sale app consumes still lives on the legacy system of record.

**Parent Topic:**[Exploring ERP Canvas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/exploring-erp-integration.md)

