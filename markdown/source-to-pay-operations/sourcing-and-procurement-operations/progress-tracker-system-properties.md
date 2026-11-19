---
title: System properties for Progress Tracker visibility
description: Two system properties control whether the Progress Tracker displays on purchase requisition and purchase order records. The procurement administrator role is required to read or write these properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-system-properties.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Progress Tracker overview, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# System properties for Progress Tracker visibility

Two system properties control whether the Progress Tracker displays on purchase requisition and purchase order records. The procurement administrator role is required to read or write these properties.

## System properties

<table id="table_tracker-properties"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_spend\_workspace.pr.progress\_tracker\_UI.enabled**

</td><td>

Controls whether the Progress Tracker displays on purchase requisition records in the workspace. When set to true, the tracker shows the states the purchase requisition progresses through.

</td></tr><tr><td>

**sn\_spend\_workspace.po.progress\_tracker\_UI.enabled**

</td><td>

Controls whether the Progress Tracker displays on purchase order records in the workspace. When set to true, the tracker shows the states the purchase order progresses through.

</td></tr></tbody>
</table><table id="table_tracker-property-attributes"><thead><tr><th>

Attribute

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Type

</td><td>

true \| false

</td></tr><tr><td>

Default

</td><td>

true

</td></tr><tr><td>

Read/Write role

</td><td>

sn\_shop.procurement\_administrator

</td></tr><tr><td>

Application

</td><td>

Source-to-Pay Workspace

</td></tr><tr><td>

Suffix

</td><td>

PR: **pr.progress\_tracker\_UI.enabled**; PO: **po.progress\_tracker\_UI.enabled**

</td></tr><tr><td>

Ignore cache / Private

</td><td>

Both cleared \(default\) on the purchase requisition record.

</td></tr></tbody>
</table>The record form header and the area below the Write roles field each show **Delete** and **Update** buttons. Select **Update** to save a changed value in the **Value** field.

\[Omitted image "progress-tracker-sys-property.png"\] Alt text: System property record showing configurable fields for Progress Tracker visibility

## Required administrator role

A user must have the sn\_shop.procurement\_administrator role to read or change either property.

**Parent Topic:**[Progress Tracker for purchase requisitions and purchase orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/progress-tracker-overview.md)

**Related topics**  


[Progress Tracker component reference]()

