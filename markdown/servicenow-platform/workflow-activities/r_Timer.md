---
title: Timer workflow activity
description: The Timer activity pauses the workflow for a specified period of time.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Timer workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Timer workflow activity

The **Timer** activity pauses the workflow for a specified period of time.

This duration can be an absolute time value or a relative value based on a defined Creating and using schedules. It is best to adjust the **Duration** so the workflow can progress in a timely manner. To pause a workflow indefinitely until a condition is met, see [wait for condition](r_WaitForCondition.md).

**Note:** Timer activities run as the System user because the system scheduler advances the workflow.

## Results

|Result|Description|
|------|-----------|
|Complete|The activity successfully reached the specified duration.|
|Cancelled|The activity or workflow was canceled before the timer reached the specified duration.|

## Input variables

Input variables determine the initial behavior of the activity.

<table id="table_dl4_ngd_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Timer Information

</td></tr><tr><td>

Timer based on

</td><td>

How the timer duration is computed. The options are:-   **A user specified duration:** The duration is based on the **Duration** fields, such as days and hours.
-   **A relative duration:** The duration is based on the **Relative duration** \(such as End of Next Business Day\) and **Wait** fields.
-   **A date/time or duration field:** The duration is based on the **Field** value and the **Wait** field.
-   **Script:** The duration is based on a script that returns the number of seconds.

</td></tr><tr><td>

DurationAppears only when **Timer based on** is **A user specified duration**.

</td><td>

The specific number of days and hours to wait before proceeding to the next activity in the workflow.

</td></tr><tr><td>

Relative durationAppears only when **Timer based on** is **A relative duration**

</td><td>

The general number and length of business days to wait before progressing to the next workflow activity. .

</td></tr><tr><td>

WaitAppears only when **Timer based on** is **A relative duration** or **A date/time or duration field**.

</td><td>

An additional timer adjustment when **Timer based on** is **A relative duration** or **A date/time or duration field**. The options are: -   **The full duration:** No modification of the calculated duration.
-   **A % of the duration:** The duration is adjusted by multiplying the number of seconds by the \(**Percentage** / 100\).
-   **Some time before:** The duration is shortened by the **Time before** days and hours.
-   **Some time after:** The duration is lengthened by the **Time after** days and hours.

</td></tr><tr><td>

PercentageAppears only when **Timer based on** is **A relative duration** or **A date/time or duration field**.

</td><td>

The **Wait** percentage value when **Timer based on** is **A relative duration** or **A date/time or duration field**.

</td></tr><tr><td>

Time beforeAppears only when **Timer based on** is **A relative duration** or **A date/time or duration field** and **Wait** is **Some time before**.

</td><td>

The modifier time value when **Wait** is **Some time before**.

</td></tr><tr><td>

Time afterAppears only when **Timer based on** is **A relative duration** or **A date/time or duration field** and **Wait** is **Some time after**.

</td><td>

The modifier time value when **Wait** is **Some time after**.

</td></tr><tr><td>

FieldAppears only when **Timer based on** is **A date/time or duration field**.

</td><td>

The date/time or duration field that contains the elapsed wait-time before moving to the next workflow activity.

</td></tr><tr><td>

ScriptAppears only when **Timer based on** is **Script**

</td><td>

The script that sets 'answer' to the number of seconds for the duration.

</td></tr><tr><td class="subhead" colspan="2">

Timer Schedule

</td></tr><tr><td>

Schedule based on

</td><td>

The basic schedule the timer uses to count working hours. If a schedule is specified, the duration will only be considered for times that are specified on the schedule. For example, if the duration is 2 hours and the workflow begins at 4:00pm on a schedule that is 8am - 5pm, then it ends at 9:00am the next day. The options are: -   **This workflow's schedule:** The schedule uses workflow context date, time, and an optional **Time zone based on** value.
-   **A specific schedule:** The schedule uses a pre-defined **Schedule** and an optional **Time zone based on** value.
-   **A schedule field:** The schedule uses a value from a table and an optional **Time zone based on** value.

</td></tr><tr><td>

ScheduleAppears only when **Schedule based on** is **A specific schedule**.

</td><td>

The pre-defined **Schedule** from a list.

</td></tr><tr><td>

Schedule fieldAppears only when **Schedule based on** is **A schedule field**.

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr><tr><td class="subhead" colspan="2">

Timer Time Zone

</td></tr><tr><td>

Time zone based on

</td><td>

The time zone for calculating the duration. The time zone may be based on:-   **No time zone:** Default. Workflow uses the GMT time zone.
-   **A specific time zone:** A predefined **Time zone**.
-   **A time zone field:** A **Time zone field** to track time duration from a field on the form.

</td></tr><tr><td>

Time zoneAppears only when **Time zone based on** is **A specific time zone**.

</td><td>

The predefined time zone.

</td></tr><tr><td>

Time zone fieldAppears only when **Time zone based on** is **A time zone field**.

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The **Timer** activity is in this state very briefly while initializing, after which it immediately changes to **Waiting**.|
|Waiting|The workflow engine waits until the timer reaches the specified duration. The engine then transitions the workflow to the next activity.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

## Example

You can use a **Timer** activity to pause the workflow until the end of the business day.

![](../image/WFTimerExample.png "Timer example")

In this example, the script evaluates the time between the *now* variable and the *eod* variable. The *eod* variable is defined, in 24 hour time, as 4:00 PM. The script then sets the *answer* variable to the difference between these variables, in seconds, and logs a message.

```
// get now and calc end of day (4:00pm)
 
var now =new Date();
 
var eod =new Date();
eod.setHours(16);
eod.setMinutes(0);
eod.setSeconds(0);
 
answer =(eod.getTime()- now.getTime())/1000;
 
workflow.debug('Timer will fire @: '+ eod +'  '+(answer/60)+' minutes from now');
```

**Parent Topic:**[Timer workflow activities](../concept/c_TimerActivities.md)

