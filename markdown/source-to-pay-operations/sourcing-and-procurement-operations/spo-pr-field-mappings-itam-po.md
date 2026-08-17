---
title: SPO PR field mappings to Asset Management PO
description: Lists the field mappings between SPO purchase requisition \(PR\) records and Asset Management purchase order \(PO\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-pr-field-mappings-itam-po.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, asset management, purchase requisition, purchase requisition line, field mapping, PR, PRL]
breadcrumb: [SPO Asset Management data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO PR field mappings to Asset Management PO

Lists the field mappings between SPO purchase requisition \(PR\) records and Asset Management purchase order \(PO\) records.

Fields in the SPO PR record align to fields in the Asset Management PO and purchase order line \(POL\) data model. The latest record in SPO takes precedent over legacy fields, with the exception of product model. Data flows between the SPO records and Asset Management PO in both directions.

|SPO Record|SPO Parent Field|SPO Child Field|Corresponding Asset Management PO Field|Corresponding Asset Management POL Field|
|----------|----------------|---------------|---------------------------------------|----------------------------------------|
|PR|Supplier|N/A|Vendor|N/A|
|PR|Total Amount|N/A|Total Cost|N/A|
|PR \(PRL\)|N/A|Purchased Quantity|N/A|Ordered Quantity|
|PR \(PRL\)|N/A|Negotiated Unit Price|N/A|Cost|
|PR \(PRL\)|N/A|Delivery Location.Location|Ship To|N/A|
|PR \(PRL\)|N/A|Total line amount|N/A|Total Cost|

**Parent Topic:**[SPO and Asset Management data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to Asset Management PO]()

[SPO PO state mappings to Asset Management PO]()

[SPO PR state mappings to Asset Management PO]()

[SPO SR field mappings to Asset Management PO]()

[SPO SR state mappings to Asset Management PO]()

[Asset Management shipment field and state mappings to SPO]()

[Asset Management receipt field mappings to SPO receipt records]()

