---
title: SPO SR state mappings to ITAM PO
description: Lists the state mappings between SPO sourcing request \(SR\) records and ITAM purchase order \(PO\) records.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, ITAM, sourcing request, state mapping, sourcing request, purchase order, SR, PO]
breadcrumb: [SPO and ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO SR state mappings to ITAM PO

Lists the state mappings between SPO sourcing request \(SR\) records and ITAM purchase order \(PO\) records.

State alignment between SPO SR records and ITAM PO follows the mappings in this table. SPO PO states take precedent over PR states. SPO PR states take precedent over SR states. If any SPO purchase requisition lines \(PRLs\) are rejected, the ITAM purchase order lines \(POLs\) in sourcing flow \(suppliers that are not awarded\) are updated to Closed Cancel state.

|SPO Record|State|State on ITAM PO|
|----------|-----|----------------|
|SR|Closed Rejected|Closed Cancel|
|SR|Closed Canceled|Closed Cancel|
|SR|Closed No Decision|Closed Cancel|
|SR|Any other state|Requested|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

