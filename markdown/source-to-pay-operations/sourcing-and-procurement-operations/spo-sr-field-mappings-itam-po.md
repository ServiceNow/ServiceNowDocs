---
title: SPO SR field mappings to Asset Management PO
description: Lists the field mappings between SPO sourcing request \(SR\) records and Asset Management purchase order \(PO\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-sr-field-mappings-itam-po.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SPO Asset Management data model mappings, Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# SPO SR field mappings to Asset Management PO

Lists the field mappings between SPO sourcing request \(SR\) records and Asset Management purchase order \(PO\) records.

The SR initiates the sourcing workflow, and quantity, price, and delivery location mappings defined at the SR line level are carried into the purchase requisition \(PR\).

These same PR line mappings are reused to create purchase order line \(POL\) records after supplier award, automatically populating the **Quantity**, **Price**, and **Delivery Address**/**Ship To** fields.

**Parent Topic:**[SPO and Asset Management data model mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/itam-spo-data-model.md)

**Related topics**  


[SPO PO field mappings to Asset Management PO]()

[SPO PO state mappings to Asset Management PO]()

[SPO PR field mappings to Asset Management PO]()

[SPO PR state mappings to Asset Management PO]()

[SPO SR state mappings to Asset Management PO]()

[Asset Management shipment field and state mappings to SPO]()

[Asset Management receipt field mappings to SPO receipt records]()

