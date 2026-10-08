---
title: SupplyOn integration status values
description: The integration-status values that the outbound staging header and lines move through, and which component sets each value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/source-to-pay-operations/supplyon-integration-status-values.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [SupplyOn integration architecture and processing, Purchase Order Management integration with SupplyOn, Integrate with Purchase Order Management, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# SupplyOn integration status values

The integration-status values that the outbound staging header and lines move through, and which component sets each value.

Both outbound streams move the Purchase Order Management outbound staging records through the framework integration-status life cycle. The header \(sn\_spend\_intg\_outbound\_purchase\_order\) and its lines \(sn\_spend\_intg\_outbound\_purchase\_order\_line\) move together.

|Status|Meaning|Set by|
|------|-------|------|
|5|Draft|The existing Purchase Order Management flow, before this integration is involved.|
|10|New|The existing Purchase Order Management flow, when it writes the outbound staging row. This is the outbound trigger event.|
|20|In process|The send subflow, immediately before POST /purchaseorder \(header and lines\).|
|30|Processed|The async status callback, on status OK.|
|40|Failed|The send subflow \(synchronous non-201 or callback timeout\) or the async callback \(status ERROR\).|

## Cost allocation

The related sn\_spend\_intg\_outbound\_cost\_allocation table \(buyer-side financial coding\) carries its own **erp\_integration\_status** field with the same values. Cost-allocation rows are not sent to SupplyOn. The integration keeps them in sync with parent order transitions so they don't remain open after the order closes.

