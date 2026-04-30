---
title: Renewals calendar view
description: Use the Renewals calendar in the Software Asset Workspace to view the entitlements nearing their expiry date and contracts nearing their expiry date or are already expired.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Workspace, Explore, Software Asset Management, IT Asset Management]
---

# Renewals calendar view

Use the Renewals calendar in the Software Asset Workspace to view the entitlements nearing their expiry date and contracts nearing their expiry date or are already expired.

The sam\_user and sam\_admin roles can gain an understanding of the upcoming contract and entitlement renewals and expired contracts by navigating to **Software Asset Workspace** &gt; **Renewals calendar**.

**Note:** Activate the Software Asset Workspace \(sn\_sam\_workspace\) store application to view the Renewals calendar.

This view shows upcoming and expired renewals with the following conditions:

-   The contract must be active.
-   Contracts expiring in 90 days or fewer.
-   The end date of the contract must not be empty.
-   The state of the contract is active or expired.
-   The substate of the contract is either Awaiting review or Renewal rejected.
-   Contracts with contract model types such as Subscription, Software License, and Maintenance.
-   Entitlements with only license types of Perpetual or Subscription.
-   Entitlements without any associated contract.

![Renewals calendar showing the upcoming and expired renewals.](../image/renewal-calendar.png "Renewals calendar view")

The Renewals calendar lets you view:

-   Calendar and list view of contracts and entitlements
-   Details of contracts and entitlements in the calendar view

    You can switch to the list view from the top-most right corner of the Renewals calendar page.

    -   Contracts
        -   Contract name
        -   Renewal start date for contracts nearing their end date
        -   Renewal start date for expired contracts
        -   Contract end date
        -   Total cost
    -   Entitlements
        -   Entitlement name
        -   Start date
        -   End date

            **Note:** The end date for perpetual entitlements is the maintenance expiration date.

        -   Total cost
    **Note:** The calendar view shows the Renewal start date, which is calculated by

    ```
    End date - Days past/until renewal
    ```

    . Select the Days past/until renewal value such as 60, 90, 120, or 150 days. You must open the contract and entitlement record to view the actual start date.

-   Number of upcoming contracts and entitlements renewals grouped based on the cost center in the left pane
-   Contract information form on selecting the contract bar

    **Note:** You can renew, adjust, or cancel a contract from this record form.

-   Entitlement information form on selecting the entitlement bar

    **Note:** You must create or associate a contract to proceed with the contract renewal workflow.

-   A red line showing the current date. The contract or entitlement bar on the calendar view displays the start date as six months before the current date and the end date as six months after the current date.

You can filter and narrow down your results by:

-   Upcoming renewals based on the time scale in the calendar view
-   Days past or until renewal such as for 60, 90, 120, or 150 days
-   Renewal types such as All contracts, All entitlements, and All contracts and all entitlements
-   Publisher, Product, Contract model, and Cost Center subfilter based on the renewal type
-   Domain

    **Note:** You must install the Domain Extension Installer \[com.glide.domain.msp\_extensions.installer\] and Domain Support \[com.snc.pa.domain\_support\] plugins to view the domain data on the Renewal calendar view.


