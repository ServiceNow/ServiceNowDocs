---
title: Create campaign success goals
description: Create your own success goals to see how your campaign is progressing and learn how to use baselines to compare against your target goals.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Analyzing your campaign for effectiveness, Creating campaigns, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create campaign success goals

Create your own success goals to see how your campaign is progressing and learn how to use baselines to compare against your target goals.

## Before you begin

Role required: sn\_ca.campaign\_manager

## Procedure

1.  Navigate to **All** &gt; **Content Experiences** &gt; **Content Experience Builder** and select a campaign.

2.  Click the **Campaign Success Goals** tab and select **New**.

3.  On the form, fill in the fields.

4.  <table id="table_lkq_jdl_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the success goal.

</td></tr><tr><td>

Description

</td><td>

Description of the success goal.**Note:** The title and description help to identify how you are measuring the success of your campaign.

</td></tr><tr><td>

Success Goal Type

</td><td>

How you want to create and calculate your campaign success goal.-   Deflection: You want your campaign to inform employees so the number of inquiry cases decreases.
-   Drive action: You want your campaign to drive employees to create cases, like enrolling in health benefits.


</td></tr><tr><td>

Table

</td><td>

Provides field that the **Success Goal Type** uses to calculate from.You can use to create filter conditions to create specific success goals.

 **Note:** This field is not editable.

</td></tr><tr><td>

Case date field

</td><td>

Shows the field from the HR Case \[sn\_hr\_core\_case\] table that the **Success Goal Type** uses to calculate on. After the Content Experiences: Evaluate Campaign Success Goals scheduled job runs, and the first active case that is related to the HR service is created, tracking starts for your success criteria. Use the filters to identify specific conditions you want to track.

 **Note:** This field is not editable.

</td></tr><tr><td>

Active

</td><td>

Option to activate this campaign success goal.

</td></tr><tr><td>

Filters

</td><td>

Filters that you use to determine your evaluation and target goals. For example, for a Drive Action type, you can set your filters to this condition:

-   HR service
-   is
-   General Benefits Inquiry
After selecting your evaluation criteria and target, you can see the number of general benefits inquiry cases that were created and compare it to your target count.

</td></tr></tbody>
</table>5.  Select the **Evaluation Criteria** tab.

6.  <table id="table_b2s_3hl_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Evaluation type

</td><td>

How you want to define your campaign data collection. You can select three types:-   Target count only: Use this type when you have no historical data to compare your campaign to. This type uses date ranges and a specific **Target value** \(see Target tab\) to determine campaign success.
-   Date range: Use this type when you want to compare your campaign data to a past campaign.
-   Relative to campaign: Use this type when you only want to compare success within the campaign and not compare it to historical data. For example, you can define the type to start 10 days before and after the campaign and view the activity. You can also specify a date that is related to a campaign like Created, Publish time, Updated, and others.
 **Note:** The fields change based on the evaluation type that you select.

</td></tr><tr><td>

From date

</td><td>

Date that you want the evaluation period to start. The start date can be:

-   Before the campaign starts.
-   The start date of the campaign.
-   Any date after the campaign starts.


</td></tr><tr><td>

To date

</td><td>

Date that you want the evaluation period to end.The end date can be:

-   After the campaign ends.
-   The date that the campaign ends.
-   Any date before the campaign ends.


</td></tr></tbody>
</table>7.  From the **Evaluation type** field, select the **Date range**.

8.  On the **Campaign Success Goal** form, fill in the fields.

9.  <table id="table_kdw_kjl_xkb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Evaluation date range:From date

</td><td>

Date that you want the evaluation period to start. The start date can be:

-   Before the campaign starts.
-   The date that the campaign starts.
-   Any date after the campaign starts.


</td></tr><tr><td>

To date

</td><td>

Date that you want the evaluation period to end.The end date can be:

-   After the campaign ends.
-   The date the campaign ends.
-   Any date before the campaign ends.


</td></tr><tr><td>

Baseline date rangeFrom date

</td><td>

Date that you want the baseline period to start. Baseline dates are for past campaigns or any period you want to establish as your baseline to compare against your campaign data.The start date for your baseline can be:

-   Before the campaign starts.
-   The date the campaign starts.
-   Any date after the campaign starts.


</td></tr><tr><td>

To date

</td><td>

Date that you want the baseline period to end.The end date can be:

-   After the campaign ends.
-   The date that the campaign ends.
-   Any date before the campaign ends.
**Note:** Select the **Calculate baseline** related link to quickly see what your historical data is for the date ranges that you selected. If the calculation doesn't show data, you can expand your date range.

</td></tr></tbody>
</table>10. From the **Evaluation type** field on the Campaign Success Goal form, select **Relative to campaign**.

11. On the **Campaign Success Goal** form, fill in the fields.

12. <table id="table_axs_skl_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date offset quantity

</td><td>

Number of days, weeks, or months that you want to collect campaign data before and after the value you select in the **Campaign date** field.

</td></tr><tr><td>

Date offset units

</td><td>

Unit of time measurement that you want to define as your period to evaluate campaign data. The values you can select are:-   Days
-   Weeks
-   Months


</td></tr><tr><td>

Date offset type

</td><td>

Value that indicates the date offset quantity and units collect data before and after these values.

</td></tr><tr><td>

Campaign date field

</td><td>

Dates or times that are affiliated with a campaign that the evaluation period uses to collect data.

</td></tr></tbody>
</table>13. Select the **Target** tab.

14. On the **Campaign Success Goal** form, fill in the fields.

15. <table id="table_rpy_4ll_xkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target value

</td><td>

Only appears when you select Target count only from the Evaluation type field.The number of cases deflected or created you target for your campaign.

</td></tr><tr><td>

Direction

</td><td>

Identifies the data based on the success goal type that you select. The values are:-   Maximize: Drive action
-   Minimize: Deflection
Only appears when you select Date range and Relative to campaign evaluation types.

</td></tr><tr><td>

Percentage

</td><td>

Percentage of cases deflected or created that you target for your campaign.

</td></tr></tbody>
</table>16. Click **Submit** or **Update**.

    After the Content Experiences: Evaluate Campaign Success Goals scheduled job runs \(daily by default\), the base count and evaluation period count populates.


