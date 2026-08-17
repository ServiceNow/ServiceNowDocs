---
title: SPO SR state mappings to Asset Management PO
description: Lists the state mappings between SPO sourcing request \(SR\) records and Asset Management purchase order \(PO\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-sr-state-mappings-itam-po.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, asset management, sourcing request, state mapping, sourcing request, purchase order, SR, PO]
breadcrumb: [SPO Asset Management data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO SR state mappings to Asset Management PO

Lists the state mappings between SPO sourcing request \(SR\) records and Asset Management purchase order \(PO\) records.

State alignment between SPO SR records and Asset Management PO follows the mappings in this table. SPO PO states take precedent over PR states. SPO PR states take precedent over SR states. If any SPO purchase requisition lines \(PRLs\) are rejected, the Asset Management purchase order lines \(POLs\) in sourcing flow \(suppliers that are not awarded\) are updated to Closed Cancel state.

|SPO Record|State|State on Asset Management PO|
|----------|-----|----------------------------|
|SR|Closed Rejected|Closed Cancel|
|SR|Closed Canceled|Closed Cancel|
|SR|Closed No Decision|Closed Cancel|
|SR|Any other state|Requested|

**Parent Topic:**[SPO and Asset Management data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to Asset Management PO]()

[SPO PO state mappings to Asset Management PO]()

[SPO PR field mappings to Asset Management PO]()

[SPO PR state mappings to Asset Management PO]()

[SPO SR field mappings to Asset Management PO]()

[Asset Management shipment field and state mappings to SPO]()

[Asset Management receipt field mappings to SPO receipt records]()

