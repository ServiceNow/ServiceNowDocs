---
title: Assign and map breakdowns
description: Select which breakdowns to assign to an indicator. Map which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to associate the indicator and breakdown sources.Collect a matrix of the two-breakdown combinations for an indicator. Exclude unnecessary or meaningless combinations of breakdowns from being collected.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 9
breadcrumb: [Automated indicators, Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Assign and map breakdowns

Select which breakdowns to assign to an indicator. Map which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to associate the indicator and breakdown sources.

## Before you begin

The desired breakdowns must be defined with breakdown sources.

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

## About this task

You can create multiple mappings for the same breakdown, enabling you to use that breakdown for multiple indicators.

**Note:**

-   You can only map breakdowns to an automated indicator. If you are assigning breakdowns to a formula indicator, try to select breakdowns that are already mapped to the automated indicators in the formula.
-   The maximum number of [breakdown elements](../concept/performance-analytics-glossary.md#) that can be included in data collection is set in the property **com.snc.pa.dc.max\_breakdown\_elements\_limit**. Warnings appear in the tool when this value is exceeded. For more information, see [Performance Analytics properties](../reference/pa-properties.md).
-   The procedure on this page uses a graphical tool. You can instead select the breakdowns for the indicator in the **Breakdowns** related list on the indicator form. You also can map the indicator fields or queries for the indicator source on the breakdown form. For more information, see [Create a breakdown mapping on a breakdown record](t_CrtBkdnBreakdownMpngs.md).

## Procedure

1.  Navigate to the indicator that you want to assign a breakdown to.

2.  Press **Manage Breakdowns**.

    If you also see a button to **Enable data snapshots**, your instance supports unlimited breakdowns. For more information, see [Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md).

3.  Move the breakdown you want to assign to the indicator from **Available Breakdowns** to **Selected Breakdowns**.

    ![Manage Breakdowns slushbucket with unmapped flag highlighted.](../image/manage-breakdowns-slush.png)

    If you add an unmapped breakdown, the **Breakdown mapping** dialog appears.

    ![Breakdown mapping dialog](../image/form-ind-new-bkdwn-map.png)

    **Note:** If you are assigning breakdowns to a formula indicator, **Unmapped** icons are not displayed and the **Breakdown mapping** dialog never appears. You cannot map breakdowns to a formula indicator. To apply a breakdown successfully to a formula indicator, check that it is mapped to all automated indicators in the formula. If the formula contains other formula indicators, check the automated indicators in those formulas. Check all the way down, recursively. You do not have to check automated indicators that have been [prevented from following breakdowns](../concept/c_ExcludingBreakdownsFromFormulas.md).

4.  Complete the breakdown mapping as follows.

<table id="choicetable_xmg_r3d_pdb"><tbody><tr><td id="d196611e219">

**Use a field to map values to elements.**

</td><td>

Select the **Field** in the indicator source that maps to records in the breakdown. See the use of the **Category** field in [Example: Field mapping](../concept/example-field-mapping.md).

</td></tr><tr><td id="d196611e247">

**Use a script to map values to elements.**

</td><td>

Select **Scripted**, then select the **Script** that defines the association between indicator records and breakdown elements.Use a script when you do not have the simple use case of a field in the indicator source that maps to a breakdown source table. A script can define a wide range of mapping relationships. The most common use case is when the breakdown source is a [bucket group](../concept/performance-analytics-glossary.md#) and the script returns an integer to assign an indicator score to a bucket. See [Example: Script mapping](../concept/example-script-mapping.md).

 You cannot show real-time scores for an indicator that uses a scripted breakdown.

 **Tip:** Try to implement scripted breakdown mappings so that \[mapping of level 1 &amp;&amp; mapping of level 2\] is equal to the intersection of \[mapping of level 1\] and \[mapping of level 2\]. Otherwise, the score and the number of records may not agree for second-level breakdowns. If these values disagree, the score is correct. For more details and an example, see [KB0748969](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748969). Now Support login is required.

</td></tr></tbody>
</table>    **Note:** If you click the **Facts table** choice list, it opens, but you cannot select a different facts table.

    ![Breakdown mapping — New record pop-up with Facts table shown and choice list disabled and Field choice list enabled and the Scripted check box cleared](../image/manage-breakdowns-facts-table.png)

5.  Click **Submit**.

6.  Repeat steps 2–5 as needed, to define additional mappings.


## What to do next

If you have assigned at least two breakdowns to an automated indicator, you can collect the two-breakdown combinations. If you do so, save system resources by excluding meaningless combinations of breakdowns from being collected. See [Collect and manage a matrix of breakdowns](create-breakdown-mapping.md#).

**Important:** If you enable Data snapshots for an indicator, you are not limited to two-breakdown combinations and the indicator does not have a breakdown matrix. For more information, see [Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md).

Apply the breakdowns in one of the following ways. In the classic environment:

-   On the Analytics Hub
-   When configuring a Performance Analytics [widget](../concept/c_Widgets.md) for a dashboard
-   On a [breakdown dashboard](../concept/c_SpecialDashboards.md)
-   In a [breakdown widget](../concept/c_WidgetInteractivity.md) on a dashboard

In the Platform Analytics experience:

-   In KPI Details
-   When configuring a [data visualization](../concept/analytics-center-data-visualizations.md) for an indicator data source

**Parent Topic:**[Automated indicators](../concept/automated-indicators.md)

**Previous topic:**[Create an automated indicator](t_CreateAnAutomatedIndicator.md#)

**Next topic:**[Add a collection job to an indicator](t_EditAJobForTheIndicator.md)

## Collect and manage a matrix of breakdowns

Collect a matrix of the two-breakdown combinations for an indicator. Exclude unnecessary or meaningless combinations of breakdowns from being collected.

### Before you begin

Breakdowns must be assigned to the indicator. See [Assign and map breakdowns](create-breakdown-mapping.md#).

**Important:** If you enable Data snapshots for an indicator, you are not limited to two-breakdown combinations and the indicator does not have a breakdown matrix. For more information, see [Data snapshots and multiple breakdowns](../concept/multi-level-breakdowns.md).

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

### About this task

Sometimes, not all breakdown combinations give useful information. For example, the combination \[Country, Region\] gives the same scores as the breakdown Country. You can prevent the instance from collecting data for these invalid combinations with breakdown matrix exclusions. These exclusions are not shown in the Analytics Hub, in KPI Details, or in the scoresheet. You also cannot select excluded breakdown combinations when you create widgets or data visualizations.

To prevent performance issues, the property **com.snc.pa.dc.max\_breakdown\_elements\_level2\_limit** limits the number of elements from breakdown connections that are included in data collection. If you exceed this limit, some of the combinations in your matrix are grayed out. By excluding some breakdown combinations, you can help to avoid exceeding this limit. For more information, see [Performance Analytics properties](../reference/pa-properties.md).

**Note:**

-   The scores for individual breakdowns are still collected when the combination of those breakdowns has been excluded.
-   Scores that were collected in previous jobs for breakdown combinations are not deleted when those combinations are later excluded. New scores for those combinations are not collected.
-   These instructions are for using the graphical tool to manage breakdown matrix exclusions. However, you can also manage them in the **Breakdown matrix exclusion** tab of the indicator form.

### Procedure

1.  Navigate to **Automated Indicators**.

2.  Select the automated indicator for which you want to configure the breakdown matrix.

3.  Under **Indicator properties**, select the **Collect breakdown matrix** tab.

4.  Select the **Collect breakdown matrix** check box.

5.  Click **Manage Breakdowns**.

6.  Click **Configure Breakdown Matrix**.

    The matrix shows the number of element combinations for each breakdown pair, calculated by multiplying the number of elements for the two breakdowns. Breakdown pairs with a higher number of combinations are shown in a darker color, to help you spot possible performance bottlenecks at a glance. By default, all combinations are included in data collection. You can select combinations to exclude from data collection.

7.  In the **Breakdown Matrix** pop-up, select breakdown combinations to exclude from Analytics Hub and dashboard widgets.

    Included combinations are shaded in the breakdown matrix. Excluded combinations are white. If the number of breakdown combinations exceeds the value of **com.snc.pa.dc.max\_breakdown\_elements\_level2\_limit**, some combinations are grayed out.![Breakdown matrix with one combination excluded and another with the "Exclude breakdown combination" tool tip.](../image/exclude-breakdown-combination.png)

8.  On the indicator form, open the **Breakdown matrix exclusion** tab and see which breakdown combinations have been excluded.

    You can manage which breakdown combinations to exclude in this tab instead of using the graphical tool.


