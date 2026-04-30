---
title: Create a reserve entitlement for Microsoft online services in Software Asset Management classic
description: Create a reserve entitlement for all Microsoft online services in the Software Asset Management classic application so that you can add licenses to an existing Microsoft 365 subscription.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating reserve entitlements for Microsoft online services, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a reserve entitlement for Microsoft online services in Software Asset Management classic

Create a reserve entitlement for all Microsoft online services in the Software Asset Management classic application so that you can add licenses to an existing Microsoft 365 subscription.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement** and then select a Microsoft Office 365 entitlement.

2.  Select the **Create Reserve Entitlement** related link.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for the new licenses.|
    |End date|The earliest anniversary of the source entitlement end date. This field is calculated automatically.|
    |Purchased rights|Number of new licenses.|
    |Monthly unit cost|Unit cost of the source entitlement divided by the duration of the source entitlement \(in months\). This field is calculated automatically.|
    |Software model|Software model for the existing entitlement. This field populates automatically.|
    |Source entitlement|Existing entitlement used to create the reserve entitlement. This field populates automatically.|

4.  Select **Submit**.

    The new reserve entitlement is added to the **Reserve Entitlements** related list in the source entitlement. The state of the reserve entitlement is In use and the **Reserve entitlement** check box is selected.


## What to do next

Run a reconciliation to include the new reserve entitlement in the true-up cost calculation. Navigate to **Software Asset** &gt; **Office 365 &amp; Adobe Cloud** to view the [Office 365 &amp; Adobe Cloud dashboard](../reference/dashboard-microsoft.md). The cost of the reserve entitlement is included in True-up Cost and is not included in Current Subscription Spend.

When you pass the end date of the reserve entitlement, the SAM - Subscription Maintenance scheduled job creates a new entitlement to replace it.

**Note:** The new entitlement is not added to the Reserve Entitlements related list in the original source entitlement.

|Field|Value|
|-----|-----|
|Reserve entitlement|Option that indicates whether the new entitlement is a reserve entitlement. This option is not selected.|
|Start date|Date that the new entitlement is created.|
|End date|End date of the original source entitlement.|
|Source entitlement|Original source entitlement.|
|Purchased rights|Same number of purchased rights as the reserve entitlement.|
|Active rights|Same number of active rights as the reserve entitlement.|
|Allocations available|Same number of allocations available as the reserve entitlement.|
|State|State of the entitlement. This field is set to **In use**.|

The state of the reserve entitlement updates to **Retired**. On the Office 365 &amp; Adobe Cloud dashboard, the cost of the retired reserve entitlement is removed from the True-up Cost. The cost of the new entitlement is included in Current Subscription Spend.

**Parent Topic:**[Creating reserve entitlements for Microsoft online services](../concept/creating-0365-reserve-entitlements.md)

