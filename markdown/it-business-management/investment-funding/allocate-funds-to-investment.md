---
title: Allocate funds to an investment
description: Allocate funds to investments based on your business goals and available funds.
locale: en-US
release: xanadu
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Investment Funding, Strategic Portfolio Management]
---

# Allocate funds to an investment

Allocate funds to investments based on your business goals and available funds.

## Before you begin

Role required: sn\_invst\_pln\_v2.investment\_user

## About this task

You can allocate funds only in the funding frequency configured in the [Investment Funding Preferences](set-funding-preferences.md).

If you allocated funds to an investment earlier, you can increase or decrease the funded amount by entering an amount greater or lesser than the existing amount. Entering a lesser value unfunds the investment by the difference amount.

If you allocate funds to an investment that are in addition to the received funds, a warning message is displayed in the **Totals** row indicating that you are overallocating, and the additional fund amount will be deducted from the buffer amount set in your funding preferences. For more information on setting up overallocation of funds, see the [Set Investment Funding preferences](set-funding-preferences.md) topic. If you try to allocate beyond the available fund plus the buffer amount, an error message indicates that new funds cannot be submitted for allocation.

You can allocate funds to only those entities that are added in the **Fundable entities** field while creating the entity.

**Note:** For generic investments, you can allocate funds to investments that you own.

## Procedure

1.  Navigate to **All** &gt; **Investment Funding** &gt; **My Funds**.

2.  Click an investment card to open an active investment that has sufficient funds to allocate to another investment.

    If you want to open a different investment, access the drop-down menu next to the name of the currently displayed investment. Either search for another investment by entering its name in the **Search My Investments** field or choose it from the five most recently visited investments.

3.  Click the **Allocate Funds** tab.

4.  Select a working period and click **Apply**.

    -   If you have allocated funds earlier or there are incoming fund requests, those investments are listed in the **Allocate Funds** list.
    -   You can filter for pending \(planning and requested\) investments by clicking the filter icon \(![Icon to filter pending investments](../image/filter-icon.png)\).
5.  Add more investments to the **Allocate Funds** list for allocating funds.

    1.  Click **Add**.

    2.  Click **New** to create a new entity record if you have sufficient privileges for the source entity.

    3.  In the **Add** pane, select one or more investments from the list, and then click **Add Selected**.

        To include all the listed investments, click **Add All**.

6.  In the **Allocate Funds** list, enter the amount under the **CapEx** and **OpEx** columns under **New Fund** for all investments to which you want to allocate funds.

    **Note:** For an incoming request, take into account the amount in the **New Request** column while entering amounts in the **CapEx** and **OpEx** columns under **New Fund**.

    The state of all updated investments changes to Planning, which is indicated by highlighted cells.

7.  Click **Fund**.

8.  In the Confirm Allocate Funds dialog box, verify your allocations and click **Fund**.

    While confirming fund allocations, you can view all the details of the quarters where funds are available for funding in one section, and the details of the quarters where funds are not available for funding in another section.

9.  Right-click on a column on the grid and select **View Past Funding Details** to view the funding details of your child investments for the past fiscal periods.

    For more information, see the [View past funding details](view-past-funding-details.md) topic.


## Result

-   Funds are allocated to selected investments for the specified period.
-   The state of funded investments changes to Funded.

**Parent Topic:**[Investment Funding](../concept/investment-funding-overview.md)

