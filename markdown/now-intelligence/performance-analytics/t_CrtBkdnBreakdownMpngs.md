---
title: Create a breakdown mapping on a breakdown record
description: Specify which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to query the indicator source.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Automated breakdowns, Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a breakdown mapping on a breakdown record

Specify which field on the indicator source references the breakdown source. If no appropriate field is available, specify a script to query the indicator source.

## Before you begin

Assign a breakdown source to the breakdown before creating the mapping.

Role required: The same as for creating a breakdown.

## About this task

You can create multiple mappings for the same breakdown, enabling you to use that breakdown for multiple indicators.

**Note:** The procedure on this page uses a related list on the breakdown form. You can instead use a graphical tool that you access from the indicator form. See [Assign and map breakdowns](create-breakdown-mapping.md#).

## Procedure

1.  If you are adding a mapping to an existing breakdown, find that breakdown in the relevant list of breakdowns and open it.

2.  In the **Breakdown Mapping** related list, click **New**.

3.  Select the **Facts table**.

    This table is the indicator source that you want to break down.

4.  Do one of these actions.

<table id="choicetable_vmj_4t3_twb"><tbody><tr><td id="d116399e120">

**Use a field to map values to elements.**

</td><td>

Select the **Field** in the indicator source that maps to records in the breakdown. See the use of the **Category** field in [Example: Field mapping](../concept/example-field-mapping.md).

</td></tr><tr><td id="d116399e148">

**Use a script to map values to elements.**

</td><td>

Select **Scripted**, then select the **Script** that defines the association between indicator records and breakdown elements.Use a script when you do not have the simple use case of a field in the indicator source that maps to a breakdown source table. A script can define a wide range of mapping relationships. The most common use case is when the breakdown source is a [bucket group](../concept/performance-analytics-glossary.md#) and the script returns an integer to assign an indicator score to a bucket. See [Example: Script mapping](../concept/example-script-mapping.md).

 You cannot show real-time scores for an indicator that uses a scripted breakdown.

 **Tip:** Try to implement scripted breakdown mappings so that \[mapping of level 1 &amp;&amp; mapping of level 2\] is equal to the intersection of \[mapping of level 1\] and \[mapping of level 2\]. Otherwise, the score and the number of records may not agree for second-level breakdowns. If these values disagree, the score is correct. For more details and an example, see [KB0748969](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0748969). Now Support login is required.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  Repeat steps 2–5 as needed, to define additional mappings.


**Parent Topic:**[Automated breakdowns](../concept/automated-breakdowns.md)

**Previous topic:**[Create an automated breakdown](t_CreatingABreakdownForIndicators.md)

**Next topic:**[Assign an indicator to an automated breakdown](t_AssigningAnIndicatorToABreakdown.md)

