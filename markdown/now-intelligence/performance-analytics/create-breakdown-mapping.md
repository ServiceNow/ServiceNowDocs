---
title: Assign and map breakdowns
description: Select which breakdowns to assign to an indicator. Map which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to associate the indicator and breakdown sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/create-breakdown-mapping.html
release: brazil
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 6
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
-   The maximum number of [breakdown elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) that can be included in data collection is set in the property **com.snc.pa.dc.max\_breakdown\_elements\_limit**. Warnings appear in the tool when this value is exceeded. For more information, see [Performance Analytics properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/pa-properties.md).
-   The procedure on this page uses a graphical tool. You can instead select the breakdowns for the indicator in the **Breakdowns** related list on the indicator form. You also can map the indicator fields or queries for the indicator source on the breakdown form. For more information, see [Create a breakdown mapping on a breakdown record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CrtBkdnBreakdownMpngs.md).

## Procedure

1.  Navigate to the indicator that you want to assign a breakdown to.

2.  Press **Manage Breakdowns**.

    If you also see a button to **Enable data snapshots**, your instance supports unlimited breakdowns. For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md).

3.  Move the breakdown you want to assign to the indicator from **Available Breakdowns** to **Selected Breakdowns**.

    \[Omitted image "manage-breakdowns-slush.png"\] Alt text: Manage Breakdowns slushbucket with unmapped flag highlighted.

    If you add an unmapped breakdown, the **Breakdown mapping** dialog appears.

    \[Omitted image "form-ind-new-bkdwn-map.png"\] Alt text: Breakdown mapping dialog

    **Note:** If you are assigning breakdowns to a formula indicator, **Unmapped** icons are not displayed and the **Breakdown mapping** dialog never appears. You cannot map breakdowns to a formula indicator. To apply a breakdown successfully to a formula indicator, check that it is mapped to all automated indicators in the formula. If the formula contains other formula indicators, check the automated indicators in those formulas. Check all the way down, recursively. You do not have to check automated indicators that have been [prevented from following breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_ExcludingBreakdownsFromFormulas.md).

4.  Complete the breakdown mapping as follows.

<table id="choicetable_xmg_r3d_pdb"><tbody><tr><td id="d204272e215">

**Use a field to map values to elements.**

</td><td>

Select the **Field** in the indicator source that maps to records in the breakdown. See the use of the **Category** field in [Example: Field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/example-field-mapping.md).

</td></tr><tr><td id="d204272e243">

**Use a script to map values to elements.**

</td><td>

Select **Scripted**, then select the **Script** that defines the association between indicator records and breakdown elements.Use a script when you do not have the simple use case of a field in the indicator source that maps to a breakdown source table. A script can define a wide range of mapping relationships. The most common use case is when the breakdown source is a [bucket group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) and the script returns an integer to assign an indicator score to a bucket. See [Example: Script mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/example-script-mapping.md).

 You cannot show real-time scores for an indicator that uses a scripted breakdown.

 **Tip:** Try to implement scripted breakdown mappings so that \[mapping of level 1 &amp;&amp; mapping of level 2\] is equal to the intersection of \[mapping of level 1\] and \[mapping of level 2\]. Otherwise, the score and the number of records may not agree for second-level breakdowns. If these values disagree, the score is correct. For more details and an example, see [KB0748969](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748969). Now Support login is required.

</td></tr></tbody>
</table>    **Note:** If you click the **Facts table** choice list, it opens, but you cannot select a different facts table.

    \[Omitted image "manage-breakdowns-facts-table.png"\] Alt text: Breakdown mapping — New record pop-up with Facts table shown and choice list disabled and Field choice list enabled and the Scripted check box cleared

5.  Click **Submit**.

6.  Repeat steps 2–5 as needed, to define additional mappings.


## What to do next

If you have assigned at least two breakdowns to an automated indicator, you can collect the two-breakdown combinations. If you do so, save system resources by excluding meaningless combinations of breakdowns from being collected. See [Collect and manage a matrix of breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/configure-breakdown-matrix.md).

**Important:** If you enable Data snapshots for an indicator, you are not limited to two-breakdown combinations and the indicator does not have a breakdown matrix. For more information, see [Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/multi-level-breakdowns.md).

Apply the breakdowns in one of the following ways. In the classic environment:

-   On the Analytics Hub
-   When configuring a Performance Analytics [widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_Widgets.md) for a dashboard
-   On a [breakdown dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_SpecialDashboards.md)
-   In a [breakdown widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/c_WidgetInteractivity.md) on a dashboard

In the Platform Analytics experience:

-   In KPI Details
-   When configuring a [data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/analytics-center-data-visualizations.md) for an indicator data source

**Parent Topic:**[Automated indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/automated-indicators.md)

**Previous topic:**[Create an automated indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/t_CreateAnAutomatedIndicator.md)

**Next topic:**[Collect and manage a matrix of breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/configure-breakdown-matrix.md)

