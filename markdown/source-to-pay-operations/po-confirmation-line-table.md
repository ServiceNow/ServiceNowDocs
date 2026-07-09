---
title: Purchase Order Confirmation Line table
description: A purchase order \(PO\) confirmation line is a supplier's line-level response acknowledging whether a purchase order line can be delivered under the requested terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/po-confirmation-line-table.html
release: australia
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
keywords: [PO confirmation, Confirmation table, purchase order confirmation]
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Confirmation Line table

A purchase order \(PO\) confirmation line is a supplier's line-level response acknowledging whether a purchase order line can be delivered under the requested terms.

## sn\_poem\_po\_confirmation\_line table

The Purchase Order Confirmation Line \[sn\_poem\_po\_confirmation\_line\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP number|String|PO confirmation ID in external enterprise resource planning \(ERP\) systems.|
|Purchase order line|Reference|PO line ID that this confirmation line acknowledges.|
|Additional comments|Journal Input|Free text for the supplier to enter any comments relevant to the entire order confirmation line.|
|Created|Date/Time|Date and time on which this PO confirmation was created.|
|Purchase order confirmation|Reference|ServiceNow ID of this PO confirmation line.|
|Quantity|Decimal|Quantity for which supplier is confirming, which may be a subtotal of the order line quantity.|
|Confirmed supplier part number|String|Supplier part the supplier commits to deliver.|
|Confirmed amount|FX Currency|Confirmed total monetary amount for the confirmation line quantity.|
|Updated|Date/Time|Date and time when this record was last modified.|
|Confirmed unit price|FX Currency|Unit price for which the supplier commits to deliver.|
|Updated by|String|User who last modified this record.|
|Confirmed delivery date|Date|Delivery date for which the supplier commits to deliver.|
|Created by|String|Supplier contact who created this purchase order confirmation.|
|Confirmation status|Choice|Confirmation status provided by the supplier for this order line and quantity.|
|Sequence number|String|An identifier used to define sequence order when multiple confirmation segments for the same purchase order line are present.|
|Updates|Integer|Number of fields edited every time the record is updated.|
|Unit|Reference|Unit of measure of this confirmation line.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/master-data-tables-for-pom.md)

**Related topics**  


[View a purchase order exception](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/view-purch-order-exception.md)

