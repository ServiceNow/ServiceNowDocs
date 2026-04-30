---
title: Configure multicurrency for planning items
description: Select investment currency as an additional currency, which can be different from your functional currency, to manage financial records of your planning items.
locale: en-US
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-11-22"
reading_time_minutes: 1
breadcrumb: [Manage financials for planning items, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure multicurrency for planning items

Select investment currency as an additional currency, which can be different from your functional currency, to manage financial records of your planning items.

## Before you begin

-   You can define investment currency for planning items which do not have any financials records, such as cost plans, expense lines, benefit plans, and actual benefits. To define a investment currency for existing work, you should delete all the financial records and configure the investment currency.
-   [Enable monetary benefit plans for planning items](enable-benefitplans-spw-fin.md)
-   Role required: admin

## About this task

Following are the current limitations for multicurrency.

-   Multicurrency for cost plans that are bundled with project tasks. This feature is scheduled to be available starting with the January patch update.
-   Financial baselines do not capture investment currency fields. This feature will be available with the March store release.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** and select portfolio plan.

2.  Select a planning item from the Planning module.

3.  Select the **Financials** tab.

    In the **Currency** field, the current system currency is displayed. For example, if your Functional currency is in USD, the field is displayed as **USD \(Functional\)**.

<table id="choicetable_d3h_yqx_jhc"><thead><tr><th align="left" id="d228445e127">

Planning item type

</th><th align="left" id="d228445e130">

Procedure

</th></tr></thead><tbody><tr><td id="d228445e136">

**Demands**

</td><td>

Users have three sets of configurations:1.  Demand currency, or also called as Functional currency that is managed by your locale.
2.  Define the Investment currency for Demand, which is used to track Demand-level financial records.
3.  Investment currency for converted artifacts, the Investment currency for any planning item created from Demand, such as a Project, Epic, or any other planning item.
Use the following ways to define the investment currency for Demand and artifacts.1.  Select **Currency** field, and select the **Edit investment currency** option.

Edit investment currency modal is displayed with options to select investment currency.

2.  Define the investment currency of you demand using the **Investment currency** list.
3.  Define investment currency for the future artifacts using the **Investment currency for converted artefact** list.


</td></tr><tr><td id="d228445e185">

**Project, Epic, Feature, and Capability**

</td><td>

1.  Select **Currency** field, and select the **Edit investment currency** option.

Edit investment currency modal is displayed with options to select investment currency.

2.  Define the investment currency of you demand to use the **Investment currency** list.


</td></tr></tbody>
</table>4.  Select **Confirm** to save the investment currency selection.


