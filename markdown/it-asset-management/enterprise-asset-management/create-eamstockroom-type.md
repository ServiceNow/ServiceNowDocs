---
title: Create a stockroom type for enterprise assets
description: If the base system stockroom types don't meet your needs, you can create a custom stockroom type in the Enterprise Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/enterprise-asset-management/create-eamstockroom-type.html
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise asset inventory, Manage enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Create a stockroom type for enterprise assets

If the base system stockroom types don't meet your needs, you can create a custom stockroom type in the Enterprise Asset Workspace.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterptrise\_asset\_manager

## About this task

Stockroom types are categories of stockrooms. For detailed information on stockroom types, see [Stockroom types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/r_StockroomTypes.md).

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Inventory** &gt; **Stockroom types**.

2.  Select **New**.

3.  On the form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Name|Display name of the stockroom type.|
    |Description|General information about the stockroom type.|
    |Priority|Level of precedence for this type of stockroom.|
    |Value|Internal identifier of the stockroom type.|
    |Shipment required|Option that determines if stockrooms of this type require shipment by default.|
    |External stockroom|Indicates if stockrooms of this type are managed internally \(check box cleared\) or managed externally by a third party \(check box selected\).|

4.  Select **Save**.

    The newly created stockroom type appears in the **Stockroom types** tab.


**Parent Topic:**[Create and manage enterprise asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/enterprise-asset-management/managing-enterprise-asset-inventory.md)

