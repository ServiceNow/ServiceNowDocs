---
title: Request funds for an investment
description: Request funds from a funding source for your investment.
locale: en-US
release: yokohama
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Investment Funding, Strategic Portfolio Management]
---

# Request funds for an investment

Request funds from a funding source for your investment.

## Before you begin

Role required: sn\_invst\_pln\_v2.investment\_user

## About this task

You cannot request funds for a generic investment from any other generic investment.

You can request funds only from generic source investments that have allocated funds to your investment in the past.

You can request funds only in the funding frequency configured in the [Investment Funding Preferences](set-funding-preferences.md).

You can request funds from only those entities that were added in the **Fundable entities** field while creating the entity.

You can withdraw funding requests that are in the requested and planning state and are for past funding periods or non-editable funding periods.

## Procedure

1.  Navigate to **All** &gt; **Investment Funding** &gt; **My Funds**.

2.  Click an investment card to open the investment for which you need funds.

    If you want to open a different investment, access the drop-down menu next to the name of the currently displayed investment. Either search for another investment by entering its name in the **Search My Investments** field or choose it from the five most recently visited investments.

3.  Click the **View/Request Funds** tab.

4.  Select a working period and click **Apply**.

    The Request Funds list displays only funding sources that you previously requested funds from for your investment.

5.  Click the **Add New Source** link to select the funding source.

6.  In the **Select a Source** pane, select one or more source investments from the list, and then click **Add Selected**.

    The specified funding source is added in the Request Funds grid.

7.  In the Request Funds grid, specify the amount in the **CapEx** and **OpEx** columns under **New/Modify Request** of the funding sources from which you want to request funds.

    The state of all updated funding sources changes to Draft or Planning, which is indicated by highlighted cells.

8.  Click **Request**.

9.  In the Confirm request dialog box, verify your requests and add a comment if required.

10. Click **Request**.

11. Right-click on a column on the **New/Modify Request** field and select **Withdraw** to withdraw a funding request.


## Result

-   Funds are requested from the source investments sources for the specified period.
-   The state of the fund request record changes to Requested.

**Parent Topic:**[Investment Funding](../concept/investment-funding-overview.md)

