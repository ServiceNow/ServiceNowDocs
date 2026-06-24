---
title: Purchase Order Exception Split Line Table
description: A purchase order exception split line is a subdivided line item created when a line item requires delivery in phases. A split line is created when a supplier selects the Delivery plan change exception type and the Phased delivery subtype.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/po-exception-split-line-table.html
release: zurich
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Master data tables for Purchase Order Management, Reference, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Purchase Order Exception Split Line Table

A purchase order exception split line is a subdivided line item created when a line item requires delivery in phases. A split line is created when a supplier selects the **Delivery plan change** exception type and the **Phased delivery** subtype.

## sn\_poem\_exception\_split\_line table

The Purchase Order Exception Split Line \[sn\_poem\_exception\_split\_line\] table contains the following fields.

|Field|Data type|Description|
|-----|---------|-----------|
|Proposed delivery date|Date|The revised delivery date proposed for this split line as part of the exception resolution.|
|Updated|Date/Time|The revised delivery quantity proposed for this split line.|
|Notes|String|Additional comments related to this split line.|
|Created|Date/Time|Date and time when this split line record was created.|
|Updates|Integer|Number of fields edited every time the record is updated.|
|Parent exception|Reference|Reference to the purchase order exception record that this split line belongs to.|
|Updated by|String|The user who last modified this split line record.|
|Proposed delivery quantity|Decimal|Revised delivery quantity proposed by the supplier.|
|Created by|String|The user who created this split line record.|

**Parent Topic:**[Master data tables for Purchase Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/master-data-tables-for-pom.md)

