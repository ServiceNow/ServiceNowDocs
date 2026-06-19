---
title: Purchase order
description: Field descriptions for the purchase order record in the \[sn\_shop\_purchase\_order\] table used for reviewing or completing purchase order details for invoice processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/accounts-payable-operations/purchase-order-table.html
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [APO, Accounts Payable Operations, supplier, purchase order, PO]
breadcrumb: [Data required for invoice processing, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Purchase order

Field descriptions for the purchase order record in the \[sn\_shop\_purchase\_order\] table used for reviewing or completing purchase order details for invoice processing.

## sn\_shop\_purchase\_order table

An Account Payable Specialist fills the key fields in the purchase order for invoice processing.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP number|String|A unique identifier generated within an ERP system for the purchase order.|
|Business owner|Reference|The user who placed the order.|

|Field|Data type|Description|
|-----|---------|-----------|
|Supplier|Reference|Supplier who provides the product of this order.|
|Order type|String|Indicates if the purchase order is of the type Standard or Blanket.|
|Order placed|date\_time|Date and time of the order placed in YYYY-MM-DD HH: MM: SS format.|
|Total amount|currency|The total cost of purchase order calculated as the sum from all related lines. Example:USD 100.|

|Field|Data type|Description|
|-----|---------|-----------|
|Cost center|Reference|The cost center incurring the expense of this order.|
|Legal entity|Reference|Internal legal entity making this purchase|
|Payment term|Reference|The agreed time and conditions of payment to the supplier.|

**Parent Topic:**[Data required for invoice processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/accounts-payable-operations/master-data-table-apo.md)

