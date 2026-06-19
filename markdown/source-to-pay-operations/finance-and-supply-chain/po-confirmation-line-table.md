---
title: Purchase Order Confirmation Line table
description: A purchase order confirmation line is a line-level response from a supplier that acknowledges a specific purchase order line or a portion of it. It confirms whether the order can be delivered under the requested terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/finance-and-supply-chain/po-confirmation-line-table.html
release: australia
product: Finance and Supply Chain
classification: finance-and-supply-chain
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Confirmation Line table

A purchase order confirmation line is a line-level response from a supplier that acknowledges a specific purchase order line or a portion of it. It confirms whether the order can be delivered under the requested terms.

## sn\_poem\_po\_confirmation\_line table

The Purchase Order Confirmation Line \[sn\_poem\_po\_confirmation\_line\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|ERP number|String|The ID of this PO confirmation in external systems \(e.g. ERP \).|
|Purchase order line|Reference|The ID of the purchase order line to which this PO confirmation line refers.|
|Additional comments|Journal Input|Free text for the supplier to enter any comments relevant to the entire order confirmation line.|
|Created|Date/Time|Date and time on which this PO Confirmation was created.|
|Purchase order confirmation|Reference|The ServiceNow ID of this PO confirmation line.|
|Quantity|Decimal|The quantity for which supplier is confirming, which may be a subtotal of the order line quantity.|
|Confirmed supplier part number|String|The supplier part the supplier commits to deliver. Applicable only if the Confirmation status is set to Changes requested.|
|Confirmed amount|FX Currency|The confirmed total monetary amount for the confirmation line quantity.|
|Updated|Date/Time|Date and time when this record was last modified.|
|Confirmed unit price|FX Currency|The unit price for which the supplier commits to deliver. Applicable only if the Confirmation status is set to Changes requested.|
|Updated by|String|The user who last modified this record.|
|Confirmed delivery date|Date|The delivery date for which the supplier commits to deliver. Applicable only if the Confirmation status is set to Changes requested.|
|Created by|String|The supplier contact who created this purchase order confirmation.|
|Confirmation status|Choice|The Confirmation status provided by the supplier for this order line and quantity. Status can be Confirmed, Rejected, Changes requested.|
|Updates|Integer|Number of fields edited every time the record is updated.|
|Unit|Reference|The unit of measure of this confirmation line.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/finance-and-supply-chain/master-data-tables-for-pom.md)

