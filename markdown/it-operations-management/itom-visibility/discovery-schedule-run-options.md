---
title: Run options for discovery schedules
description: Both horizontal and top-down discovery use these run options.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Run options for discovery schedules

Both horizontal and top-down discovery use these run options.

<table id="table_qtt_ldf_br"><thead><tr><th>

Run option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

On Demand

</td><td>

Doesn’t run on a schedule. Select **Discover now** to run Discovery. This is the default option.

</td></tr><tr><td>

Daily

</td><td>

Runs every day. Use the **Time** field to specify the time of day.

</td></tr><tr><td>

Weekly

</td><td>

Runs on one designated day of each week. Use the **Time** field to specify the time of day.

</td></tr><tr><td>

Monthly

</td><td>

Runs on one designated day of each month. Use the **Day** field to select the day of the month. Use the **Time** field to specify the time of day. If the designated day doesn’t occur in the month, the schedule doesn’t run that month. For example, if you designate day 30, the schedule doesn’t run in February.

</td></tr><tr><td>

Periodically

</td><td>

Runs every designated time. Use the **Repeat Interval** field to define the time in days, hours, minutes, and seconds. The first Discovery runs at the point in time defined in the **Starting** field. The subsequent discoveries run after each **Repeat Interval** period passes.

 **Note:** For schedules configured as "Periodically", the "Time" column won't display the next scheduled run time. To determine the next execution time for schedule that is configured to run "Periodically", navigate to the Schedule \[sys\_trigger\] table and locate the corresponding schedule record. The **Next Action** field will indicate the next scheduled run.

</td></tr><tr><td>

Once

</td><td>

Run one time as designated by the date and time defined in the **Starting** field.

</td></tr><tr><td>

Weekdays

</td><td>

Runs every Monday, Tuesday, Wednesday, Thursday, and Friday. Use the **Time** field to select the time of day.

</td></tr><tr><td>

Weekends

</td><td>

Runs every Saturday and Sunday. Use the **Time** field to select the time of day.

</td></tr><tr><td>

Month Last Day

</td><td>

Run the last day of every month. Use the **Time** field to select the time of day.

</td></tr><tr><td>

Calendar Quarter End

</td><td>

Runs on March 31, June 30, September 30, and December 31. Use the **Time** field to select the time of day. To change the dates, modify the DiscoveryScheduleRunType script include.

</td></tr><tr><td>

After Discovery

</td><td>

Allows you to sequentially stagger the schedule. Use this option to run this schedule after the Discovery designated in the **Run after** field finishes. Select the **Even if canceled** check box to designate that this discovery should run, even if the **Run after** Discovery is canceled before it finishes.

 -   This option isn’t valid when Discovery is started via DiscoverNow, or when using the Discover CI feature.
-   You can’t designate an inactive Discovery schedule.
-   You can’t create a loop by designating the run after Discovery to be the same Discovery.
-   This Discovery doesn’t run if the **Run after** Discovery doesn’t finish, with the exception that the **Even if canceled** check box is selected and the Discovery is canceled.

</td></tr></tbody>
</table>**Parent Topic:**[ITOM Visibility reference](visibility-reference.md)

**Related topics**  


[Schedule a top-down discovery by Service Mapping](../../service-mapping/task/t_CreateDiscoSchedForCITypes.md)

[Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md)

