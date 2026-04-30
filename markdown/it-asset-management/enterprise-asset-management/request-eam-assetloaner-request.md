---
title: Request a loaner asset in Enterprise Asset Workspace
description: Request a temporary or loaner asset or a consumable and use it for a specified period of time.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create and manage enterprise asset inventory, Managing enterprise asset inventory and contracts, Enterprise Asset Management, IT Asset Management]
---

# Request a loaner asset in Enterprise Asset Workspace

Request a temporary or loaner asset or a consumable and use it for a specified period of time.

## Before you begin

Role required: sys\_admin

## About this task

You can request a loner asset for yourself, for another employee of your organization, or for a third-party vendor. Before the asset is installed, you can cancel the loaner asset request at any time. You can submit a loaner order even if the product is not available at the moment in the location you want to select. In this case, your order is placed in queue.

While requesting a loaner asset, ensure that the start date is within three months from the date of submission and the end date is within six months from the start date.

## Procedure

1.  Navigate to **Service Catalog**.

2.  Select the **Enterprise Asset Lifecycle** catalog.

    The sys \_admin role needs to add the Enterprise Asset Lifecycle catalog. For more details, see Service Catalog documentation.

3.  Select **Enterprise Asset Loaner Request**.

    The Enterprise Asset Loaner Request page opens.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Requested for|Person for who you are requesting the asset. You can make a request for yourself, for another employee of your organization, or for a third-party vendor.|
    |Requested for user|User for who you requested the asset. This field appears only when **For company user** is selected in the **Requested for** field.|
    |Location|Location where the requested asset needs to be provided.|
    |Model|Model of the asset that you are requesting.|
    |Start date|Date when you want to start using the asset.|
    |Return date|Date when you want to return the asset.|
    |Justification|Reason why you need the asset.|

    After entering the **Start date** and **Return date**, if there are no loaner assets available in the selected location and for the selected time period, a warning appears. If you still submit the loaner order, your loaner order will be in a waitlist. For more information on waitlisted loaner orders, see [Loaner asset reservation](../../hardware-asset-management/concept/loaner-asset.md#).

5.  Select **Submit**.

    A message appears and shows whether your loaner order was placed successfully or the order was placed in a waitlist.


## What to do next

To view your request, navigate to **Self-Service** &gt; **My Requests**.

Before you receive your loaner asset, you can cancel the loaner asset request by selecting **Cancel**. After you receive your loaner asset, the **Cancel** button doesn't appear anymore. You can also return your loaner asset before the specified **Return date**.

-   **[Prepare, deploy, and reclaim loaner assets in Enterprise Asset Workspace](prepare-deploy-reclaim-eamassets.md)**  
Select and prepare the loaner asset or consumable for deployment and reclamation by using loaner asset tasks. Deploy the loaner asset or consumable for a specific period of time, and reclaim it on the return date.

**Parent Topic:**[Create and manage enterprise asset inventory](../concept/managing-enterprise-asset-inventory.md)

