---
title: SPO PO field mappings to ITAM PO
description: Lists the field mappings between SPO purchase order \(PO\) records and ITAM purchase order \(PO\) records.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-02-12"
reading_time_minutes: 2
keywords: [SPO, ITAM, purchase order, field mapping, PO, POL]
breadcrumb: [SPO and ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PO field mappings to ITAM PO

Lists the field mappings between SPO purchase order \(PO\) records and ITAM purchase order \(PO\) records.

Fields in the SPO PO record align to fields in the ITAM PO and purchase order line \(POL\) data model. The latest record in SPO takes precedent over legacy fields, with the exception of product model. Data flows from ITAM PO to SPO PO or SPO purchase requisition \(PR\) records.

|SPO Record|SPO Parent Field|SPO Child Field|Corresponding ITAM PO Field|Corresponding ITAM POL Field|
|----------|----------------|---------------|---------------------------|----------------------------|
|PO|Total Amount|N/A|Total Cost|N/A|
|PO|Vendor|N/A|Supplier|N/A|
|PO|Requested Delivery|N/A|Requested Delivery|N/A|
|PO \(POL\)|N/A|Supplier|N/A|Vendor|
|PO \(POL\)|N/A|Supplier Part Number|N/A|Part Number|
|PO \(POL\)|N/A|Requested Delivery Date|N/A|Expected Delivery|
|PO \(POL\)|N/A|Purchased Quantity|N/A|Ordered Quantity|
|PO \(POL\)|N/A|Unit Price|N/A|Cost|
|PO \(POL\)|N/A|Total Line Amount|N/A|Total Cost|
|PO \(POL\)|N/A|Delivery Location|Ship To|N/A|
|PO \(POL\)|N/A|Received Quantity|N/A|Received Quantity|
|PO \(POL\)|N/A|Remaining Quantity|N/A|Remaining Quantity|
|PO \(POL\)|N/A|Short Description|N/A|Short Description|
|PO \(POL\)|N/A|Shipment Details.Carrier|N/A|Shipment.Shipping Carrier|
|PO \(POL\)|N/A|Shipment Details.Tracking Number|N/A|Shipment.Tracking Number|
|PO \(POL\)|N/A|Shipment Details.Actual Shipment Date|N/A|Shipment.Ship Date|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR field mappings to ITAM PO](spo-pr-field-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

