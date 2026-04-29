---
title: Enter actual spends for an investment
description: Enter actual spends for your investments to track fund utilization.
locale: en-US
release: australia
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investment Funding, Strategic Portfolio Management]
---

# Enter actual spends for an investment

Enter actual spends for your investments to track fund utilization.

## Before you begin

Role required: sn\_invst\_pln\_v2.investment\_user

## About this task

You can use funds in your investments to execute business activities or allocate funds to other investments to meet business goals. You can record the amount spent as actual spends \("actuals"\) in the respective investment. Tracking actuals enables you to do the following:

-   Track where and how you spent your funds.
-   Add up to the parent investment actuals.

Actual cost incurred for projects or demands will be summed up and displayed in the Investment Funding grid automatically if there is a single funded source. If there are multiple sources, you need to perform the following steps to enter the actuals manually.

**Note:**

-   \(For customers upgraded from legacy Investment Funding plugin to the ServiceNow Store application\) If you have entered actuals manually prior to upgrade, then the same does not match with the actuals posted in the project post-upgrade.
-   If the **Budget** field on the cost plan breakdown of a project or demand has been edited post funding, the CapEx and OpEx budgets do not match the amount funded from the Investment Funding flow.

## Procedure

1.  Navigate to **All** &gt; **Investment Funding** &gt; **My Funds**.

2.  Open an investment for which you want to enter actuals.

    If you want to open a different investment, access the drop-down menu next to the name of the currently displayed investment. Either search for another investment by entering its name in the **Search My Investments** field or choose it from the five most recently visited investments.

3.  Click the **View/Request Funds** tab.

4.  Select a working period and click **Apply**.

5.  In the Request Funds list, specify the actual amount spent under the **Actual CapEx** and **Actual OpEx** columns for your investments.

    **Note:** If you do not see the **Actual CapEx** and **Actual OpEx** columns in the list, click the configuration icon \(![Configuration](../../planning-and-policy/image/configuration-icon.png)\) and select them.


## Result

-   The entered amount is updated as actual funds spent through the investment.
-   The amount rolls-up to its parent investment, which in turn rolls-up until the top-level investment.

**Parent Topic:**[Investment Funding](../concept/investment-funding-overview.md)

