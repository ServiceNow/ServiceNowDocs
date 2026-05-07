---
title: Outbound Order staging table
description: The Outbound Order \[sn\_spend\_intg\_outbound\_purchase\_order\] staging table stores important data about the purchase orders created so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables Sourcing Procurement, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound Order staging table

The Outbound Order \[sn\_spend\_intg\_outbound\_purchase\_order\] staging table stores important data about the purchase orders created so that an ERP integrator can export this data to a third-party ERP system.

The following table lists the key fields for the Outbound Order \[sn\_spend\_intg\_outbound\_purchase\_order\] staging table.

**Note:** There are no mandatory fields for this table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Blanket order end date

</td><td>

Date

</td><td>

Date on which the blanket order is expected to end.If you're unsure of the delivery date of the product, you can provide an estimated time frame, which then creates a blanket order.

</td></tr><tr><td>

Blanket order start date

</td><td>

Date

</td><td>

Date on which the blanket order is expected to start.If you're unsure of the delivery date of the product, you can provide an estimated time frame, which then creates a blanket order.

</td></tr><tr><td>

Business owner

</td><td>

String

</td><td>

The user who placed the order.

</td></tr><tr><td>

Catalog ID

</td><td>

String

</td><td>

Unique identifier for each catalog of the purchase order.

</td></tr><tr><td>

Customer ID

</td><td>

 

</td><td>

Unique identifier for each customer of the purchase order.

</td></tr><tr><td>

ERP number

</td><td>

String

</td><td>

Unique number generated within the ERP system for the purchase order.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which the purchase order is imported.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Current status of the purchase order integration.

</td></tr><tr><td>

Legal entity

</td><td>

String

</td><td>

Name of the legal entity making this purchase.

</td></tr><tr><td>

Order date

</td><td>

String

</td><td>

Date and time of the order placed in YYYY-MM-DD HH: MM: SS format.

</td></tr><tr><td>

Order type

</td><td>

String

</td><td>

Type of the purchase order, which can be Standard or Blanket.

</td></tr><tr><td>

Payment term

</td><td>

String

</td><td>

The agreed time and conditions of payment for the purchase order.

</td></tr><tr><td>

PO amount

</td><td>

String

</td><td>

Total amount of the purchase order.

</td></tr><tr><td>

PO amount currency

</td><td>

String

</td><td>

Currency of the purchase order.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status of the purchase order.

</td></tr><tr><td>

Purchase order number

</td><td>

String

</td><td>

Unique number for the purchase order.

</td></tr><tr><td>

Purchase order status

</td><td>

String

</td><td>

Current status of the purchase order.

</td></tr><tr><td>

Purchasing group

</td><td>

String

</td><td>

The group of employees making the purchase order.

</td></tr><tr><td>

Purchasing organization

</td><td>

String

</td><td>

The organization making the purchase order.

</td></tr><tr><td>

Supplier company name

</td><td>

String

</td><td>

Supplier company name for which the purchase order is generated.

</td></tr><tr><td>

Supplier ID

</td><td>

String

</td><td>

Supplier ID for which the purchase order is generated.

</td></tr></tbody>
</table>