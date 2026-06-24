---
title: Purchase Order Exception
description: Purchase order exceptions arise when a supplier can't fulfill the agreed terms of a purchase order. Common causes include changes to delivery quantity or date, or a complete inability to fulfill the order. Operational buyers use the Purchase Order Management application to manage and resolve these exceptions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/purchase-order-exception-table.html
release: zurich
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Exception

Purchase order exceptions arise when a supplier can't fulfill the agreed terms of a purchase order. Common causes include changes to delivery quantity or date, or a complete inability to fulfill the order. Operational buyers use the Purchase Order Management application to manage and resolve these exceptions.

## sn\_poem\_exception table

The Purchase order exception \[sn\_poem\_exception\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Exception sub-type|String|Type of purchase order exception. Options are: **Revised single delivery**, **Phased delivery**, and **Rejection**.|
|Delivery date gap|Integer|Difference between delivery date in the purchase order and the proposed delivery date in the exception.|
|Delivery quantity gap|String|Difference between quantity in the purchase order and the purchase order exception.|
|Rejection reason|Integer|Reason why a supplier can't fulfill an order.|
|Days till deadline|Integer|Number of days remaining before the requested delivery date.|
|Proposed delivery date|Date|Revised delivery date proposed by the supplier.|
|Related PO line|Reference|Purchase order line number on which the exception is created.|
|Proposed delivery quantity|Decimal|Revised delivery quantity proposed by the supplier.|
|Exception type|String|The broad category of the purchase order exception. The exception type supported is delivery plan change.|
|Supplier|Reference|Supplier who fulfills this order|
|Requested by|Reference|The user that submitted the exception.|
|Primary contact|Reference|The main point of contact for resolving this exception on the buyer side.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/master-data-tables-for-pom.md)

