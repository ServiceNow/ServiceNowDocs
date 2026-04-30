---
title: Create a reserve entitlement for Microsoft online services in the Software Asset Workspace
description: Create a reserve entitlement for Microsoft online services in the Software Asset Workspace so that you can add licenses to an existing Microsoft 365 subscription.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating reserve entitlements for Microsoft online services, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a reserve entitlement for Microsoft online services in the Software Asset Workspace

Create a reserve entitlement for Microsoft online services in the Software Asset Workspace so that you can add licenses to an existing Microsoft 365 subscription.

## Before you begin

To create reserve entitlements for Microsoft online services in the Software Asset Workspace, you must request and activate the Software Asset Workspace \(sn\_sam\_workspace\) store application. For details on requesting and activating the Software Asset Workspace \(sn\_sam\_workspace\) store application, see [Request Software Asset Management](t_RequSoftwareAssetMgmt.md).

Role required: sam\_user or sam\_admin

## Procedure

1.  From your ServiceNow instance, navigate to **Software Asset** &gt; **Software Asset Workspace**.

    The Software Asset Workspace launches in a new tab.

2.  From the left navigation menu of the Software Asset Workspace, select **License operations**.

    The License operations view opens.

3.  From the left navigation menu of the License operations view, navigate to **Licensing** &gt; **Software entitlements**.

4.  From the list of available software entitlements, select a Microsoft Office 365 entitlement.

    The software entitlement details page opens in a new tab.

5.  Select **Create Reserve Entitlement**.

6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for the new licenses.|
    |End date|The earliest anniversary of the source entitlement end date. This field is calculated automatically.|
    |Purchased rights|Number of new licenses.|
    |Monthly unit cost|Unit cost of the source entitlement divided by the duration of the source entitlement \(in months\). This field is calculated automatically.|
    |Software model|Software model for the existing entitlement. This field populates automatically.|
    |Source entitlement|Existing entitlement that is used to create the reserve entitlement. This field populates automatically.|

7.  Select **Submit**.

8.  After your request is successfully submitted, select **Close**.

    The new reserve entitlement is added to the **Reserve Entitlements** related list in the source entitlement. The state of the reserve entitlement is In use and the **Reserve entitlement** check box is selected.


## What to do next

Run a reconciliation to include the new reserve entitlement in the true-up cost calculation. View your reconciliation results in the [Microsoft publisher overview](../reference/publisher-overview-microsoft.md). The cost of the reserve entitlement is included in the **True-up cost** report.

When you pass the end date of the reserve entitlement, the SAM - Subscription Maintenance scheduled job creates a new entitlement to replace it.

**Note:** The new entitlement isn’t added to the **Reserve Entitlements** related list in the original source entitlement.

|Field|Value|
|-----|-----|
|Reserve entitlement|Option that indicates whether the new entitlement is a reserve entitlement. This option isn’t selected.|
|Start date|The date that the new entitlement is created.|
|End date|End date of the original source entitlement.|
|Source entitlement|Original source entitlement.|
|Purchased rights|Same number of purchased rights as the reserve entitlement.|
|Active rights|Same number of active rights as the reserve entitlement.|
|Allocations available|The same number of allocations available as the reserve entitlement.|
|State|State of the entitlement. This field is set to **In use**.|

The state of the reserve entitlement updates to **Retired**. On the Microsoft publisher overview, the cost of the retired reserve entitlement is removed from the **True-up cost** report. The cost of the new entitlement is included in the Current Subscription Spend.

