---
title: SPO SR state mappings to ITAM PO
description: Lists the state mappings between SPO sourcing request \(SR\) records and ITAM purchase order \(PO\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-sr-state-mappings-itam-po.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [SPO, ITAM, sourcing request, state mapping, sourcing request, purchase order, SR, PO]
breadcrumb: [SPO ITAM data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
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

**Parent Topic:**[SPO and ITAM data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to ITAM PO]()

[SPO PO state mappings to ITAM PO]()

[SPO PR field mappings to ITAM PO]()

[SPO PR state mappings to ITAM PO]()

[SPO SR field mappings to ITAM PO]()

[ITAM shipment field and state mappings to SPO]()

[ITAM receipt field mappings to SPO receipt]()

