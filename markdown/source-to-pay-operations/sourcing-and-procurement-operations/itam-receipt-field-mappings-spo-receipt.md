---
title: ITAM receipt field mappings to SPO receipt
description: Lists the field mappings between ITAM receipt line records and SPO receipt records.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-02-12"
reading_time_minutes: 1
keywords: [ITAM, SPO, receipt, field mapping, receiving]
breadcrumb: [SPO and ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# ITAM receipt field mappings to SPO receipt

Lists the field mappings between ITAM receipt line records and SPO receipt records.

SPO receipt is auto-generated in the background after receipt of any items. Based on the ITAM data model, the ITAM receipt line field corresponds to the equivalent of SPO receipt. The ITAM receiving slip can contain multiple receiving lines. SPO receipt is read-only, with data captured from the ITAM purchase order \(PO\) whenever the ITAM receiving experiences are active.

|ITAM Receipt Line Fields|SPO Receipt Fields|
|------------------------|------------------|
|ITAM Purchase Order Line|SPO Purchase Order Line|
|Quantity|Quantity Received|
|N/A|Type = Default or "Good Receipt"|
|Received By|Received By|
|N/A|Supplier Product \(based on POL\)|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

