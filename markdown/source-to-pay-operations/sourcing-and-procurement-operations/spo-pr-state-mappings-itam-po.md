---
title: SPO PR state mappings to ITAM PO
description: Lists the state mappings between SPO purchase requisition \(PR\) records and ITAM purchase order \(PO\) records.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-02-12"
reading_time_minutes: 1
keywords: [SPO, ITAM, purchase requisition, purchase order, state mapping, PR, PO]
breadcrumb: [SPO and ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PR state mappings to ITAM PO

Lists the state mappings between SPO purchase requisition \(PR\) records and ITAM purchase order \(PO\) records.

State alignment between SPO PR records and ITAM PO follows the mappings in this table. SPO PO states take precedent over PR states. SPO PR states take precedent over SR states.

|SPO Record|State|State on ITAM PO|
|----------|-----|----------------|
|PR|Closed Canceled|Closed Cancel|
|PR|Closed Rejected|Closed Cancel|
|PR|Any other state|Requested|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

