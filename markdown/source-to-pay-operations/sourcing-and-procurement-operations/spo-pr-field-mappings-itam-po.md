---
title: SPO PR field mappings to ITAM PO
description: Lists the field mappings between SPO purchase purchase requisition \(PR\) records and ITAM purchase order \(PO\) records.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, ITAM, purchase requisition, purchase requisition line, field mapping, PR, PRL]
breadcrumb: [SPO and ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PR field mappings to ITAM PO

Lists the field mappings between SPO purchase purchase requisition \(PR\) records and ITAM purchase order \(PO\) records.

Fields in the SPO PR record align to fields in the ITAM PO and purchase order line \(POL\) data model. The latest record in SPO takes precedent over legacy fields, with the exception of product model. Data flows between the SPO records and ITAM PO in both directions.

|SPO Record|SPO Parent Field|SPO Child Field|Corresponding ITAM PO Field|Corresponding ITAM POL Field|
|----------|----------------|---------------|---------------------------|----------------------------|
|PR|Supplier|N/A|Vendor|N/A|
|PR|Total Amount|N/A|Total Cost|N/A|
|PR \(PRL\)|N/A|Purchased Quantity|N/A|Ordered Quantity|
|PR \(PRL\)|N/A|Negotiated Unit Price|N/A|Cost|
|PR \(PRL\)|N/A|Delivery Location.Location|Ship To|N/A|
|PR \(PRL\)|N/A|Total line amount|N/A|Total Cost|

**Parent Topic:**[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO](spo-po-field-mappings-itam-po.md)

[SPO PO state mappings to ITAM PO](spo-po-state-mappings-itam-po.md)

[SPO PR state mappings to ITAM PO](spo-pr-state-mappings-itam-po.md)

[SPO SR field mappings to ITAM PO](spo-sr-field-mappings-itam-po.md)

[SPO SR state mappings to ITAM PO](spo-sr-state-mappings-itam-po.md)

[ITAM shipment field and state mappings to SPO](itam-shipment-field-state-mappings-spo.md)

[ITAM receipt field mappings to SPO receipt](itam-receipt-field-mappings-spo-receipt.md)

