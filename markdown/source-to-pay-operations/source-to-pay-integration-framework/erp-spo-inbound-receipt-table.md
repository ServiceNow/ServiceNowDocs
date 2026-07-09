---
title: Receipt inbound staging table
description: The Receipt inbound \[sn\_fcms\_intg\_imp\_receipt\] staging table temporarily stores important data about receipts before this data is sent to the primary table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/source-to-pay-integration-framework/erp-spo-inbound-receipt-table.html
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-07-01"
reading_time_minutes: 1
breadcrumb: [ERP Integration Framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Receipt inbound staging table

The Receipt inbound \[sn\_fcms\_intg\_imp\_receipt\] staging table temporarily stores important data about receipts before this data is sent to the primary table.

The following table lists the fields for the Receipt inbound \[sn\_fcms\_intg\_imp\_receipt\] staging table.

<table id="table_erp_spo_inbound_receipt_table"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP PO line number

</td><td>

String

</td><td>

Purchase order line number from the ERP system.

</td></tr><tr><td>

ERP PO number

</td><td>

String

</td><td>

Purchase order number from the ERP system.

</td></tr><tr><td>

ERP receipt number

</td><td>

String

</td><td>

Unique number generated within the ERP system for the receipt.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.

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

PO line number

</td><td>

String

</td><td>

Purchase order line number against which the receipt of the product is acknowledged.

</td></tr><tr><td>

Quantity received

</td><td>

String

</td><td>

Quantity of product received as part of the receipt.

</td></tr><tr><td>

State

</td><td>

String

</td><td>

Current state of the receipt.

</td></tr><tr><td>

Supplier product

</td><td>

String

</td><td>

Supplier product for which the receipt is generated.

</td></tr><tr><td>

Type

</td><td>

String

</td><td>

Type of the receipt based on the product type. For example, Goods Receipt or Services Receipt.

</td></tr></tbody>
</table>