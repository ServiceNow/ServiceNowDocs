---
title: Add targets for multiple breakdown elements in KPI Details
description: Select multiple breakdown elements in the KPI Details target configuration panel. Add a target to each element. This target can be an improvement on a baseline instead of an absolute value.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 5
breadcrumb: [Targets and thresholds, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Add targets for multiple breakdown elements in KPI Details

Select multiple breakdown elements in the KPI Details target configuration panel. Add a target to each element. This target can be an improvement on a baseline instead of an absolute value.

## Before you begin

Role required: pa\_admin, pa\_target\_admin, pa\_power\_user, or admin

## Procedure

1.  Open KPI Details for an indicator.

2.  Click the target icon \(![Target icon](../image/target-icon.png)\).

    The **Targets** panel opens.

3.  Click the cogwheel to open the **Targets Configuration** page.

    ![Targets panel top showing config cogwheel.](../image/kpi-details-target-config-cogwheel.png)

    The **Targets configuration** view opens.

4.  Select **Add targets to breakdowns**.

    ![The Add Targets to Breakdowns button in the Targets Configuration view.](../image/kpi-details-targets-add-2-breakdowns.png)

    The **Add targets to breakdown elements** dialog opens.

5.  Select one breakdown from the list of breakdowns for the indicator.

6.  Select any number of elements for the breakdown and click **Next**.

    **Tip:** If you have many elements to scroll through, sort or filter on a value in any of the columns. You can also click **Filter** and use the condition builder to narrow down the selection.

7.  Set targets for the elements as described in Step [7](edit-multiple-targets.md#step_new-target) in [Edit targets in KPI Details](edit-multiple-targets.md).

8.  Set a start date, when the targets come into effect, and a review date.

9.  If you are calculating the targets from an average or a previous score, and you don't want the new targets to be above or below certain values, set minimum and maximum values.

    In this dialog, a minimum value of 4 is set. No maximum value is set.![Completed dialog for adding targets to multiple breakdown elements, with a minimum value set.](../image/kpi-details-multiple-targets.png)

10. Select **Add**.


## Result

Batch target creation happens asynchronously. You might see a progress bar.

## Configuring targets for multiple elements

Starting February 11, your company began tracking open incidents for each assignment group. By the end of the month, the number of open incidents assigned to your top 4 groups had varied from 18 to 60. The trends also were highly variable.

![Open incidents for each of the 4 top assignment groups for February.](../image/kpi-details-targets-assgroups.png)

You would like consistent improvement across these four groups. Therefore, you want to set them targets that are equivalent despite the differences in absolute values. You also want to set the targets together. To achieve this aim, you open the **Targets configuration** view and click **Add targets to breakdowns**.

![The Add Targets to Breakdowns button in the Targets Configuration view.](../image/kpi-details-targets-add-2-breakdowns.png)

You select the Assignment group breakdown.

![Selecting the Assignment Group breakdown in the Add target to breakdown element dialog.](../image/kpi-details-targets-select-breakdown.png)

You get a list of the elements of the Assignment Group breakdown. There are many elements. The four elements you are looking for all have "Support" in the name, so you filter the **Name** column on "Support."

![Filtering elements for those with "Support" in the name.](../image/kpi-details-targets-filter-name.png)

The filter reduces the number of elements to browse to 9, from which you easily select the 4 that you want and click **Next**.

You can either specify a target value or base it on a calculation. The difference between HR Systems Support and the other three elements is too much to give all four elements the same target value. Therefore, you base the target on a calculation applied to each element.

Calculations can be made on the existing target or on an average score over a time period. There are no existing targets for these elements, so you must select an average score.

You can set the target either as a unit number improvement on the average score, such as 3 or 4.5, or as a percentage improvement. The scores are close enough that you could probably use a unit number. However, you decide to set the target as a percentage improvement on the average score.

![Selecting a percent change to the average score as the basis for the targets of multiple breakdowns.](../image/kpi-details-targets-select-baseline.png)

You take the average score from February 11 until February 28. You think 5% is a good improvement target for the next month, so you set the targets to begin March 1 and to review them March 31. You don't think you want to constrain the target values within a range, so you don't set maximum or minimum values.

![Selecting the percentage value, the time range over which to calculate the average score, and the start and review dates of targets you are adding for multiple breakdowns.](../image/kpi-details-targets-select-pct-dates.png)

After you click **Add** and dismiss the success message, you see the four targets that you created.

![The targets you just created for 4 elements showing in the Targets Configuration list.](../image/kpi-details-targets-new-targets.png)

Here is a table with the targets you created and their values. All targets take effect on 1 March and are scheduled for review on 31 March.

|Target|Value \(rounded to integer\)|
|------|----------------------------|
|Assignment Group: HR Systems Support|20|
|Assignment Group: Oracle Support|31|
|Assignment Group: Technical Services Support|50|
|Assignment Group: Financial Systems Support|43|

**Parent Topic:**[Indicator targets and thresholds in KPI Details](../concept/kpi-details-targets.md)

**Related topics**  


[Create a target in KPI Details](create-kpi-details-targets.md)

[Edit targets in KPI Details](edit-multiple-targets.md)

[Create, modify, or delete a threshold in KPI Details](add-mod-pers-tar-thresh-kpi-details.md)

[Responsibility for global indicator targets](../concept/responsibiity-targets-kpi-details.md#)

