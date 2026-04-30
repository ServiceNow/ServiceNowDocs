---
title: Outbound Receipt staging table
description: The Outbound Receipt \[sn\_spend\_intg\_outbound\_receipt\] staging table stores important data about the receipts created so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Sourcing and Procurement Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound Receipt staging table

The Outbound Receipt \[sn\_spend\_intg\_outbound\_receipt\] staging table stores important data about the receipts created so that an ERP integrator can export this data to a third-party ERP system.

The following table lists the key fields for the Outbound Receipt \[sn\_spend\_intg\_outbound\_receipt\] staging table.

**Note:** There are no mandatory fields for this table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP number

</td><td>

String

</td><td>

Unique number generated within the ERP system for the receipt.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which the receipt is imported. The ERP source is determined through the legal entity associated with these records.

</td></tr><tr><td>

Integration status

</td><td>

String

</td><td>

Current status of the receipt integration.

</td></tr><tr><td>

Milestone

</td><td>

String

</td><td>

Milestone associated with the receipt.

</td></tr><tr><td>

Percentage received

</td><td>

String

</td><td>

Percentage of the service received.This field is visible only for a service receipt.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status of the receipt.

</td></tr><tr><td>

Purchase order line number

</td><td>

String

</td><td>

Purchase order line number against which the receipt of the product is acknowledged.

</td></tr><tr><td>

Purchase order line sys ID

</td><td>

String

</td><td>

Purchase order line **Sys\_id** of the receipt.

</td></tr><tr><td>

Quantity received

</td><td>

String

</td><td>

Quantity of product received as part of the receipt.

</td></tr><tr><td>

Receipt number

</td><td>

String

</td><td>

Unique number for the receipt.

</td></tr><tr><td>

Receipt status

</td><td>

String

</td><td>

Current status of the receipt.The status field is visible only when the ERP integration plugin is installed.

</td></tr><tr><td>

Receipt type

</td><td>

String

</td><td>

Type of the receipt based on the product type. For example, Goods Receipt or Services Receipt.

</td></tr><tr><td>

Supplier product

</td><td>

String

</td><td>

Supplier product for which the receipt is generated.

</td></tr></tbody>
</table>