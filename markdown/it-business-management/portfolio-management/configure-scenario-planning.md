---
title: Configure the scenario planning type and scope
description: Configure the scenario planning type and select the scope of portfolios to determine the way you want to plan and work on your portfolios. You can also specify using Investment Funding for funding demands and projects in your portfolios.
locale: en-US
release: australia
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure the scenario planning type and scope

Configure the scenario planning type and select the scope of portfolios to determine the way you want to plan and work on your portfolios. You can also specify using Investment Funding for funding demands and projects in your portfolios.

## Before you begin

**Important:** Modifying the planning type and scope deletes all your existing scenarios and confirmed plans.

Role required: it\_pps\_admin

## About this task

The option to use Investment Funding for funding your portfolios is available only when you activate the Investment Funding plugin.

## Procedure

1.  Navigate to **All** &gt; **Project** &gt; **Portfolios** &gt; **Configure Planning**.

2.  Open the scenario planning configuration record.

3.  Configure the planning type and scope.

<table id="choicetable_zkm_1vk_knb"><thead><tr><th align="left" id="d92655e94">

Planning type

</th><th align="left" id="d92655e97">

Steps

</th></tr></thead><tbody><tr><td id="d92655e103">

**If you want to plan for a single fiscal year and single portfolio**

</td><td>

1.  Select **Annual Financial and Resource Capacity Based Planning** from the Planning Type list.
2.  Select **Single Selected Portfolio** from the Planning Scope list.


</td></tr><tr><td id="d92655e127">

**If you want to plan for a single fiscal year and all portfolios**

</td><td>

1.  Select **Annual Financial and Resource Capacity Based Planning** from the Planning Type list.
2.  Select **All Portfolios** from the Planning Scope list.


</td></tr><tr><td id="d92655e151">

**If you want to plan for multiple years and single portfolio**

</td><td>

1.  Select **Multi-Year Resource Capacity Based Planning** from the Planning Type list.
2.  Select **Single Selected Portfolio** from the Planning Scope list.
3.  Select your default planning duration from the **Default Planning Window** list.

When you select a planning window, all the demands and projects falling within the selected duration appear on the Portfolio Planning Workbench.

</td></tr><tr><td id="d92655e183">

**If you want to plan for multiple years and all portfolios**

</td><td>

1.  Select **Multi-Year Resource Capacity Based Planning** from the Planning Type list.
2.  Select **All Portfolios** from the Planning Scope list.
3.  Select your default planning duration from the **Default Planning Window** list.


</td></tr></tbody>
</table>4.  If you want to enable selection of demands and projects that are in completed or inactive state, select **Allow Selection of Completed Projects**.

5.  If you want to retrieve the target amount from Investment Funding, select **Investment Funding Integration**.

    **Note:** This option is available only when the Investment Funding for PPM \(com.snc.investment\_planning\_pmo\) plugin is active and planning type is selected as **Annual Financial and Resource Capacity Based Planning**.

    -   If the planning scope is **Single Selected Portfolio**, the target amount of that portfolio is retrieved from the **New Fund** column for the selected portfolio investment. For more information, see [Allocate funds to an investment](../../investment-funding/task/allocate-funds-to-investment.md).
    -   If the planning scope is **All Portfolios**, specify a source to retrieve the target amount.
        1.  Select a funding entity from the Funding Entity list from which your demands and projects will be funded.
        2.  Select the transaction table for the selected funding entity from the Funding Record list.
6.  Click **Update**.


## Result

The scenario planning configuration is updated and all scenario plans and confirmed plans are deleted. The configuration changes also updates the Portfolio Planning Workbench to enable you to do scenario planning based on the updated planning type and scope.

-   **[Impact of modifying the scenario planning type and scope](../reference/change-planning-mode-type.md)**  
Modifying the planning type and scope impacts the demands and project selection in your planning scenarios and portfolio planning. You can change the planning type and scope at any time during portfolio planning.

**Parent Topic:**[Scenario Planning for PPM](../concept/portfolio-planning-overview.md)

