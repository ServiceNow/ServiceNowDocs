---
title: Loaner assets
description: Request a loaner asset or consumable when you need it for a short period of time.Waitlisted loaner orders give visibility to future demands for loaner asset.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Loaner assets

Request a loaner asset or consumable when you need it for a short period of time.

A loaner order request is completed through the following stages:

-   Prepare task: Prepare the loaner asset such as by installing the required software before handing over the loaner asset to the requested user. By default, the Prepare task is created two days before the start day. You can change this setting by modifying the *Number of days required for preparing the loaner asset* variable on the Loaner Asset Request catalog item.

    **Note:** The *Number of days required for preparing the loaner asset* variable is not shown on the catalog form when you request a loaner asset. To find this variable, go to the Catalog Item module. Only users with the catalog\_admin role can change the value of this variable.

-   Deploy task: Hand over the loaner asset to the requested user or install the loaner asset at the user's machine. The Deploy task is created after the Prepare task is closed.
-   Reclaim task: Reclaim the loaner asset after a period of time. The Reclaim task is created one day before the return day.

**Note:**

Loaner assets are not counted in the stockroom count when stock rules are being processed.

You can't allocate an excluded loaner asset. For more information, see [Hardware Asset Management license exclusion](ham-license-exclusion.md).

**Related topics**  


[Manage loaner assets](../task/manage-loaner-asset.md)

## Loaner asset reservation

Waitlisted loaner orders give visibility to future demands for loaner asset.

With the available loaner assets, the user who submits a loaner order first gets the loaner asset. Loaner assets are automatically assigned to the users by a daily scheduled job on the Preparation start day. When there is no loaner asset in a stockroom, all the loaner orders become part of a Waitlist. The Waitlisted Orders module under Loaner shows all the wait listed loaners orders. If new loaner assets are added to a stock room or confirmed loaner order are canceled, the wait listed loaner orders are confirmed in a sequence of when they were submitted. A loaner order that was submitted before gets precedence over the order that was submitted later.

As an inventory admin, if you want to confirm a wait listed loaner order, uncheck the **Waitlisted** box in the Loaner Asset Order form and in the **Asset** field, select the asset. If you want to move a confirmed loaner order to wait list, check out the **Waitlisted** box and remove the Asset from the **Asset** field. You can assign a loaner asset from any locations and with any of the following states and substates:

-   In stock
-   Available
-   Pending install
-   Reserved
-   In use

**Note:** You can't select an excluded loaner asset. For more information, see [Hardware Asset Management license exclusion](ham-license-exclusion.md).

