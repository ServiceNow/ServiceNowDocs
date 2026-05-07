---
title: SPO PO state mappings to ITAM PO
description: Lists the state mappings between SPO purchase order \(PO\) records and ITAM purchase order \(PO\) records.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, ITAM, purchase order, state mapping, PO, POL]
breadcrumb: [SPO ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PO state mappings to ITAM PO

Lists the state mappings between SPO purchase order \(PO\) records and ITAM purchase order \(PO\) records.

State alignment between SPO PO records and ITAM PO follows the mappings in this table, with the SPO PO driving the state behavior. SPO PO and purchase order line \(POL\) states drive all states except for delivered and partially delivered, which reference receiving actions in ITAM.

|SPO Record|State|State on ITAM PO|
|----------|-----|----------------|
|PO|Ordered|Ordered|
|PO|Partially Delivered|Pending Delivery or Ordered \(depending on whether Advanced Shipment Notification \(ASN\) is implemented. If ASN is enabled, assets move to "In Transit" and the ITAM PO remains in the "Pending Delivery" state.\)|
|PO|Delivered|Received|
|PO|Closed Cancel|Closed Cancel|
|PO|Closed Paid|Closed Complete|
|PO|Pending Submission|Ordered|
|PO|Payment Pending|Received|
|PO|Processing|Ordered|
|POL|Ordered|Ordered|
|POL|Partially Delivered|Pending Delivery or Ordered \(depending on if ASN is implemented\)|
|POL|Delivered|Received|
|POL|Closed Cancel|Cancelled|
|POL|Closed Paid|Received|
|POL|Pending Cancellation|Ordered|
|POL|Pending Submission|Ordered|
|POL|Payment Pending|Received|
|POL|Processing|Ordered|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

