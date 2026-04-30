---
title: Purchase order
description: A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Master data table for Accounts Payable Operations, Reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Purchase order

A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.

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

**Parent Topic:**[Master data table for Accounts Payable Operations](master-data-table-apo.md)

