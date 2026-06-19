---
title: Purchase Order Confirmation table
description: Purchase order confirmations are supplier-generated transactions that acknowledge a buyer's order and communicate the supplier's ability to fulfill it as specified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/finance-and-supply-chain/po-confirmation-table.html
release: australia
product: Finance and Supply Chain
classification: finance-and-supply-chain
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Confirmation table

Purchase order confirmations are supplier-generated transactions that acknowledge a buyer's order and communicate the supplier's ability to fulfill it as specified.

## sn\_poem\_po\_confirmation table

The Purchase Order Confirmation \[sn\_poem\_po\_confirmation\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Created by|String|The supplier contact who created this purchase order confirmation record.|
|Purchase order|Reference|Reference to the purchase order associated with this confirmation.|
|Confirmation source|Choice|Indicates how the confirmation was received, such as manually entered, imported from an ERP, or submitted by the supplier.|
|Number|String|Auto-generated unique identifier for this PO confirmation record.|
|Active|True/False|Indicates whether this confirmation record is currently active.|
|Created|Date/Time|Date and time on which this PO Confirmation was created.|
|ERP number|String|Reference purchase order ID in the external ERP system.|
|Updates|Integer|Number of fields edited every time the record is updated.|
|Additional comments|Journal Input|Free text for the supplier to enter any comments relevant to the entire order confirmation.|
|Updated by|String|The user who last modified this record.|
|ERP Source|Reference|Reference to the ERP system from which this confirmation originated.|
|Updated|Date/Time|Date and time when this record was last modified.|
|Status|Choice|Indicates the current stage of the confirmation record. Possible values are Draft or Submitted.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/finance-and-supply-chain/master-data-tables-for-pom.md)

