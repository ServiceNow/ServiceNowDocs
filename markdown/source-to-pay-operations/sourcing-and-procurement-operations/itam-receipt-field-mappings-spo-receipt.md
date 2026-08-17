---
title: Asset Management receipt field mappings to SPO receipt records
description: Lists the field mappings between Asset Management receipt line records and SPO receipt records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/itam-receipt-field-mappings-spo-receipt.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [asset management, SPO, receipt, field mapping, receiving]
breadcrumb: [SPO Asset Management data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Asset Management receipt field mappings to SPO receipt records

Lists the field mappings between Asset Management receipt line records and SPO receipt records.

SPO receipt is auto-generated in the background after receipt of any items. Based on the Asset Management data model, the Asset Management receipt line field corresponds to the equivalent of SPO receipt. The Asset Management receiving slip can contain multiple receiving lines. SPO receipt is read-only, with data captured from the Asset Management purchase order \(PO\) whenever the Asset Management receiving experiences are active.

|Asset Management Receipt Line Fields|SPO Receipt Fields|
|------------------------------------|------------------|
|Asset Management Purchase Order Line|SPO Purchase Order Line|
|Quantity|Quantity Received|
|N/A|Type = Default or "Good Receipt"|
|Received By|Received By|
|N/A|Supplier Product \(based on POL\)|

**Parent Topic:**[SPO and Asset Management data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to Asset Management PO]()

[SPO PO state mappings to Asset Management PO]()

[SPO PR field mappings to Asset Management PO]()

[SPO PR state mappings to Asset Management PO]()

[SPO SR field mappings to Asset Management PO]()

[SPO SR state mappings to Asset Management PO]()

[Asset Management shipment field and state mappings to SPO]()

