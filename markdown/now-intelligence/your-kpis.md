---
title: Managing indicators from the Platform Analytics library
description: The indicator library lists all the Performance Analytics indicators/KPIs to which you have access. Users who can create or edit indicators or Performance Analytics collection jobs have additional information.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Platform Analytics experience, Platform Analytics]
---

# Managing indicators from the Platform Analytics library

The indicator library lists all the Performance Analytics indicators/KPIs to which you have access. Users who can create or edit indicators or Performance Analytics collection jobs have additional information.

Open the list of indicators at **Platform Analytics** &gt; **Library** &gt; **Indicators**. The configuration of the Indicators page and the data access depends on your roles. All users with at least read access to an indicator get the basic indicator management functionality that is included in the default view.

## Basic indicator management

![Default view of indicator library for non-admin users.](../../par-for-workspace/image/ind-lib-default.png "Default indicator library view with basic functionality")

You can see any automated, formula, external, or manual indicator that has **Show in library** enabled on its indicator record and to which you have access, including benchmark indicators. Select the name of an indicator to open it in KPI Details, in a new tab.

You have several options for filtering what appears in the library. The numbered callouts in [Default indicator library view with basic functionality](your-kpis.md#fig_kdl_fcn_ngc) match the numbers in the following list:

1.  Under **Filter by**, you have the option to filter on bookmarked indicators. If you have the right to create indicators, you can also filter on the indicators that you have created.
2.  Use the Search field to search by indicator name or description.
3.  Expand the Filter list ![](../../../administer/process-mining/image/filter.png) and add conditions for filtering the indicators. Under **Saved filters**, you can save the filters you currently have open and reopen them later. You can also toggle the labels on the filter fields on and off.

    ![Conditional filter list on indicator library.](../../par-for-workspace/image/ind-list-conditions.png)

4.  Open the Edit columns ![](../../par-for-workspace/image/icon-edit-list-columns.png) dialog, and select which indicator parameters appear as columns in the list.

Sort the records according to a column's values by selecting the column label. Repeatedly select the label to switch between forward and reverse sorting. The type of sorting depends on the type of data in the column, such as alphanumeric sorting for text or date sorting for dates.

## Indicator management for users who can edit indicators or collection jobs

**Note:** The functionality in this section is available only to users with the pa\_power\_user or pa\_data\_collector role or higher. Users also have all the basic functionality that was described in the previous section.

![Platform Analytics indicator library](../../par-for-workspace/image/analytics-center-kpis-tab.png "Default indicator library view for privileged users, data snapshots not enabled")

Privileged users have the following extra functionality:

-   Creating indicators: Press **Create indicator** to open a blank Indicator form. For more information, see [Create an automated indicator](../task/t_CreateAnAutomatedIndicator.md#) or [Create a formula indicator](../task/t_CreateAFormulaIndicator.md).
-   Editing indicators: Select the pencil icon next to an indicator to open that indicator's record. Security restrictions may apply.
-   Deleting indicators: Select one or more indicators by ticking the box in its row, then press **Delete**. The **Delete** button shows you how many indicators are selected for deletion.
-   Indicator health: A row of tiles shows you useful statistics about the health of your indicators, such as how many automated and formula indicators do not have active collection jobs. The No active data collection job, Not viewed in 6 months, and Not viewed in one year tiles suggest how many indicators you may be able to delete. Conversely, Updated in the last 30 days gives you an idea how many indicators are truly active. Press a tile to filter the indicator list by that statistic.

    **Note:** Filters on the list of indicators do not currently filter the tiles.

-   Indicators you created: You have an additional **Filter by** option, to see only the indicators you have created.

Privileged users also see a different set of default columns. In place of the Description field, you see the following information:

-   The indicator source for each automated indicator
-   The state of the data collection job
-   The last time the indicator was viewed
-   How many times in total it was viewed in the last year

## Indicator management for admin users with data snapshots enabled

If you have not tried to enable data snapshots on your instance, you have a banner at the top of KPI Details.

![Banner for checking data snapshots eligibility.](../../par-for-workspace/image/datasnap-eligibility-banner.png)

Press **Check instance eligibility** to see if your instance is eligible for data snapshots and, if not, why. For more information, see [Activate data snapshots](../task/activate-unlimited-breakdowns.md#).

When your instance is eligible for data snapshots, you have a banner announcing this fact and two new tiles, Data snapshots enabled and Data snapshots supported. You can select one or more indicators in the list and press **Enable Data Snapshots \(quantity of indicators selected\)**.

**Tip:** If you show the data snapshot status column, you can see which indicators support data snapshots.

![Indicator library with data snapshots eligible on the instance.](../../par-for-workspace/image/kpis-ds-enabled.png "Default indicator library view for privileged users, with data snapshots enabled")

**Related topics**  


[KPI Details](../../par-for-workspace/concept/kpi-details.md)

[Performance Analytics indicators](c_Indicators.md)

[Performance Analytics Essentials training](https://learning.servicenow.com/lxp?course_id=cbf7fac4db1a7340760a71043996194c&id=learning_course_prev)

