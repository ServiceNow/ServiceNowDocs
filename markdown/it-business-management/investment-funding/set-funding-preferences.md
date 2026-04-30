---
title: Set Investment Funding preferences
description: As an administrator, you can set global defaults for Investment Funding preferences, which affect the funding behavior.
locale: en-US
release: xanadu
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Investment Funding administration, Investment Funding, Strategic Portfolio Management]
---

# Set Investment Funding preferences

As an administrator, you can set global defaults for Investment Funding preferences, which affect the funding behavior.

## Before you begin

Role required: sn\_invst\_pln\_investment\_admin

## Procedure

1.  Navigate to **All** &gt; **Investment Funding** &gt; **Setup** &gt; **Preferences**.

2.  In the **Funding frequency** list, select a frequency of periods in which you can request or allocate funds to an investment.

    The list shows options based on the configured fiscal calendar.

    For example, if you set up the Standard fiscal calendar and you want to fund your investments quarterly, select **Quarter**.

    The default value is Quarter for the Standard fiscal calendar setup or Period for any other fiscal calendar setup.

3.  In the **Number of editable past periods** field, enter a number to specify the number of past periods enabled for you to modify the allocated or requested fund.

    For example, if the funding frequency is Quarter and you enter 2 in the field, you can edit funds for the previous two quarters.

    The default value is 0 \(editing of past period funding is not enabled\).

4.  Select the **Hide actuals in tree view** check box to hide the actual amount of an investment in the tree view cards.

5.  Select the **Allow fund overallocation** check box to enable allocation of funds in addition to the received funds.

    The **Fund overallocation percent \(%\)** and **Allow fund overallocation at investment level** fields are enabled.

6.  In the **Fund overallocation percent \(%\)** field, enter the percentage by which funds can be allocated in addition to the received funds.

    For example, if the received fund amount is $200,000, and you enter 10% in the **Fund overallocation percent** field, a total of $220,000 can be used for funding.

7.  Select the **Allow fund overallocation at investment level** check box to enable source investment owners who have funded the investment and are not removed from the allocation to override the fund overallocation percent at investment level.

8.  Click **Save**.

9.  Select an option from the confirmation window that is displayed:

    -   Update the overallocation preferences at the investment level for all existing investments
    -   Update the overallocation preferences at the investment level for existing investments that have not overridden the overallocation percentage
    -   Update the overallocation preferences at the investment level only for new investments
10. Click **Confirm**.


**Parent Topic:**[Investment Funding administration](../concept/investment-funding-administration.md)

