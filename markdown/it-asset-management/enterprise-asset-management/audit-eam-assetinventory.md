---
title: Audit enterprise asset inventory
description: Audit your enterprise asset inventory to learn where your assets are and what their current status is.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Stockroom audit access by role, Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Audit enterprise asset inventory

Audit your enterprise asset inventory to learn where your assets are and what their current status is.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager, sn\_eam.asset\_technician, sn\_itam\_common.asset\_audit\_user, or sn\_itam\_common.asset\_audit\_admin

## About this task

You can use the [Mobile Agent application for Enterprise Asset Management](../concept/eam-mobile-agent-app.md) to scan asset tags or enter them manually. If an asset is scanned but its asset tag does not exist in our database, then by default, that asset is mapped to an unknown model record. The unknown model record appears on the **All enterprise models** tab of the **Model Management** view in the Enterprise Asset Workspace. The asset manager manually associates this asset to the appropriate model. You can't change, update or delete an unknown model.

**Note:** Starting with Enterprise Asset Management version 9.0, you can also audit the licensed hardware assets in the Enterprise Asset Workspace only if the Hardware Asset Management application is activated.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Asset audits**.

2.  Select **New**.

    The Create New Enterprise Asset Audit page opens.

3.  On the Create New Asset Audits form, fill in the fields.

    For a description of the field values, see [Asset audit fields for enterprise assets](../reference/asset-audit-record-fields-eam.md).

4.  Select **Save**.


## Result

The asset audit inventory record is created and appears with the **Expected Assets** and **Scanned Assets** tabs.

## What to do next

Scan the assets in the inventory using the ServiceNow Agent app.

**Parent Topic:**[Stockroom audit access by role](../concept/stockroom-audit-access-eam.md)

**Related topics**  


[Asset audit fields for enterprise assets](../reference/asset-audit-record-fields-eam.md)

[Audit results](../reference/audit-results-eam.md)

[Complete a single scan enterprise asset inventory audit using the ServiceNow Agent app](scan-assets-agent-app-eam.md)

[Complete multi scan enterprise asset inventory audit using the ServiceNow Agent app](complete-multi-scan-inventory-audit-using-mobile-app-eam.md)

