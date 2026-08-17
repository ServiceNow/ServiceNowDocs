---
title: SPO PO field mappings to Asset Management PO
description: Lists the field mappings between SPO purchase order \(PO\) records and Asset Management purchase order \(PO\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-po-field-mappings-itam-po.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [SPO, Asset Management, purchase order, field mapping, PO, POL]
breadcrumb: [SPO Asset Management data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PO field mappings to Asset Management PO

Lists the field mappings between SPO purchase order \(PO\) records and Asset Management purchase order \(PO\) records.

Fields in the SPO PO record align to fields in the Asset Management PO and purchase order line \(POL\) data model. The latest record in SPO takes precedent over legacy fields, with the exception of product model. Data flows from Asset Management PO to SPO PO or SPO purchase requisition \(PR\) records.

|SPO Record|SPO Parent Field|SPO Child Field|Corresponding Asset Management PO Field|Corresponding Asset Management POL Field|
|----------|----------------|---------------|---------------------------------------|----------------------------------------|
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

**Parent Topic:**[SPO and Asset Management data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO state mappings to Asset Management PO]()

[SPO PR field mappings to Asset Management PO]()

[SPO PR state mappings to Asset Management PO]()

[SPO SR field mappings to Asset Management PO]()

[SPO SR state mappings to Asset Management PO]()

[Asset Management shipment field and state mappings to SPO]()

[Asset Management receipt field mappings to SPO receipt records]()

