---
title: Edit targets in KPI Details
description: Retroactively change one or more existing targets from their start date instead of ending them and starting new targets from a later date. You can edit multiple targets to have the same value, the same change in value, or the same date.
locale: en-US
release: zurich
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 5
breadcrumb: [Targets and thresholds, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Edit targets in KPI Details

Retroactively change one or more existing targets from their start date instead of ending them and starting new targets from a later date. You can edit multiple targets to have the same value, the same change in value, or the same date.

## Before you begin

Role required: pa\_target\_admin to edit all global targets. Any user with a personal target can edit that target.

A responsible user can edit a global target they are responsible for, regardless of role. For more information, see [Responsibility for global indicator targets](../concept/responsibiity-targets-kpi-details.md#).

## About this task

If you have multiple targets set on the same indicator, the Target Configuration panel in KPI Details lets you set them in bulk to have the same start date, review date, or value. As a manager, you can use this feature to modify targets for a set of segments.

You can change only identical target values to new values. You can change differing start and review dates to new, identical start or review dates. However, none of the new periods when the targets would apply can overlap the periods of other targets that match the same filters.

**Note:** An alternative interface is available for a quick edit of a single target. Open the Targets panel and select the tile for a target. You can change the absolute value and the Start and Review dates of the target. For more options in editing a target, or to edit multiple targets, use the following procedure instead.

## Procedure

1.  Open KPI Details for an indicator.

2.  Click the target icon ![Target icon](../image/target-icon.png).

    The **Targets** panel opens.

3.  Click the cogwheel to open the **Targets Configuration** page.

    ![Targets panel top showing config cogwheel.](../image/kpi-details-target-config-cogwheel.png)

    The **Targets configuration** view opens.

4.  Click **Filter** to set whether you see targets that have expired, targets that are currently in effect, or targets that will come into effect in the future.

    By default, you see targets that are currently in effect and those that will come into effect.

    ![Filter on Targets Configuration panel letting you choose whether to select any of past, current, or future targets.](../image/kpi-details-targets-config-past-pres-future.png)

5.  To further filter the selection of targets, select the hidden filter icon on the right side of each column header.

    You can filter or sort by item name, value, start date, or review date. In the following example, the **Item** column is about to be filtered for names containing `priority`. Only targets on the Priority breakdown will show.

    **Tip:** You can filter on item name for either breakdowns or time aggregations. For example, filtering on `7d` returns only targets on weekly time aggregations.

    ![Filtering for targets only on the Assignment Group breakdown.](../image/kpi-details-targets-config-filter.png)

6.  Select one or more targets.

7.  Set new target values, either as an absolute value or through a calculation.

    -   To set an absolute value for the targets, select **None** in **Target calculation** and an absolute value in the **Value** field.
    -   To select a change from the current targets, select the following:

<table id="table_igl_jd4_kpb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Target calculation

</td><td>

Current target \(units\) or Current target \(%\)

</td></tr><tr><td>

Direction

</td><td>

Select **Increase** for the new target value to be higher than the current target or Decrease for the new value to be lower than the current target.

</td></tr><tr><td>

Change \(units\) or Change \(%\)

</td><td>

The value either added or subtracted to the current targets to calculate the new targets, depending on the setting in **Direction**. The value you enter is either an absolute value \(units\) or a percentage.For example, you have selected two targets with values of 20 and 5. You have also selected Current target \(units\) as the target calculation and Decrease as the direction. When you enter 2 in Change \(units\), the new target values are 18 and 3. If you instead select Current target \(%\) as the target calculation and enter 25 under Change \(%\), the new target values are 15 and 4.

</td></tr><tr><td>

Minimum target value

</td><td>

The lowest value you want the target to have, regardless of calculation. You do not need to specify a value.

</td></tr><tr><td>

Maximum target value

</td><td>

The highest value you want the target to have, regardless of calculation. You do not need to specify a value.

</td></tr></tbody>
</table>    -   To select a change from the average score over a period of time, select the following:

        |Field|Value|
        |-----|-----|
        |Target calculation|Average score \(units\) or Average score \(%\)|
        |First score|The opening date of the time period over which to calculate the average score|
        |Last score|The closing date of the time period over which to calculate the average score|
        |Direction|Select **Increase** for the target to be higher than the average score or **Decrease** for the target to be lower than the average score.|
        |Change \(units\) or Change \(%\)|The value either added or subtracted to the average score to calculate the new targets, depending on the setting in **Direction**. The value you enter is either an absolute value \(units\) or a percentage.|
        |Minimum target value|The lowest value you want the target to have, regardless of calculation. You do not need to specify a value.|
        |Maximum target value|The highest value you want the target to have, regardless of calculation. You do not need to specify a value.|

8.  Select the start date, when the targets come into effect, and a review date.

    You expect to meet the target by the review date, or at least to review progress then.


**Parent Topic:**[Indicator targets and thresholds in KPI Details](../concept/kpi-details-targets.md)

**Related topics**  


[Create a target in KPI Details](create-kpi-details-targets.md)

[Create, modify, or delete a threshold in KPI Details](add-mod-pers-tar-thresh-kpi-details.md)

[Add targets for multiple breakdown elements in KPI Details](add-multiple-targets.md)

[Responsibility for global indicator targets](../concept/responsibiity-targets-kpi-details.md#)

