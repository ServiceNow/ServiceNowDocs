---
title: ITAM shipment field and state mappings to SPO
description: Lists the field and state mappings between ITAM Shipment records and SPO Shipment records.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ITAM, SPO, shipment, field mapping, state mapping]
breadcrumb: [SPO ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# ITAM shipment field and state mappings to SPO

Lists the field and state mappings between ITAM Shipment records and SPO Shipment records.

## Field mappings

Shipment records created in asset management have corresponding readN/Aonly records created on the SPO shipment details table. ITAM shipment state mappings are driven by the ITAM shipment table, which contains conditional logic. The SPO shipment table is readN/Aonly.

|Field on ITAM Shipment Table|Field on SPO Shipment Table|
|----------------------------|---------------------------|
|Shipping Carrier \(POL\)|Shipment Details.Carrier \(SPO POL\)|
|Ship Date \(POL\)|Shipment Details.Actual Shipment Date \(SPO POL\)|
|Tracking Number \(POL\)|Shipment Details.Tracking Number \(SPO POL\)|
|Location \(POL\)|N/A|
|Terms \(PO\)|N/A|
|Shipment Rate \(PO\)|N/A|
|Ship Date \(POL\)|Actual Shipment Date \(SPO POL\)|

## State mappings

|State on ITAM Shipment Table|State on SPO Shipment Table|
|----------------------------|---------------------------|
|In Transit|Out for Delivery|
|Delivered|Delivered|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

