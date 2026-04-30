---
title: DurationCalculator - Global
description: The DurationCalculator script include provides methods for calculating durations and due dates.Constructor for DurationCalculator class.Calculates an end date and time based on current start date and time and passed in duration \(seconds\).Calculates the due date starting at the passed in start time and adding the number of days using the current schedule and time zone.Calculates the duration using the specified relative duration script.Returns the duration between the startTime and the endTime within the already-specified schedule and optionally overridden timezone.Returns the duration between the startTime and the endTime within the already-specified schedule and optionally overridden timezone.Gets the endDateTime property that was set by calcDuration/calcRelativeDuration, indicating the end date and time for the duration.Returns the this.seconds property that was set by calcDuration/calcRelativeDuration, indicating the total number of seconds of work to be performed for the duration.Returns the totalSeconds value that was set by a call to calculate\(record\).Compares the passed in time to the time value in the passed in GlideDateTime object.Sets the schedule and time zone to use for calculating the due date.Sets the start date and time for the duration calculations.Sets the start date and time for the duration calculations.Sets the time zone to use for calculating the due date.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DurationCalculator- Global

The DurationCalculator script include provides methods for calculating durations and due dates.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DurationCalculator - DurationCalculator\( \)

Constructor for DurationCalculator class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var dc = new DurationCalculator();
```

## DurationCalculator - calcDuration\(Number seconds\)

Calculates an end date and time based on current start date and time and passed in duration \(seconds\).

This method also sets the **this.endDateTime**, **this.seconds**, and **this.totalSeconds** properties with the updated values. The **seconds** property represents the total number of seconds of work to be performed in the duration based on the work schedule. The **totalSeconds** property represents the total number of seconds between the start and end times of the duration, which includes both work and non-work.

Prior to calling this method, you must call setStartDateTime\(\) with the start time to use for the duration.

|Name|Type|Description|
|----|----|-----------|
|seconds|Number|Number of seconds to add to the start date and time to compute the end date and time, seconds, and total seconds values.|

|Type|Description|
|----|-----------|
|Boolean|False if the input value is not a number.|

```
var gdt = new GlideDateTime("2020-05-01 00:00:00");

var dc = new DurationCalculator();
dc.setStartDateTime(gdt);

if(!dc.calcDuration(2*24*3600)){ // 2 days
  gs.log("*** Error calculating duration");
  return;
}
var secs = dc.getSeconds();
var totalSecs = dc.getTotalSeconds();

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output

```
***SCHEDULE DURATION: SECS=172800 TOTALSECS=970534 ENDTIME = 2020-05-03 00:00:00
```

## DurationCalculator - calcRelativeDueDate\(GlideDateTime start, Number days, String endTime\)

Calculates the due date starting at the passed in start time and adding the number of days using the current schedule and time zone.

Called from relative duration definitions, initiated by calcRelativeDuration\(\), as `calculator.calcRelativeDueDate(calculator.startDateTime, days)`. Once the day that the work is due is determined, the method sets the time to the passed in **endTime** of that day. If there are not enough days left in the schedule, uses the last day in the schedule.

<table id="table_vw4_gvb_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

start

</td><td>

GlideDateTime

</td><td>

GlideDateTime object that contains the start date for the computation.

</td></tr><tr><td>

days

</td><td>

Number

</td><td>

Number of days to add to the start date.

</td></tr><tr><td>

endTime

</td><td>

String

</td><td>

Time of day that the work is due on the computed due date.If blank, defaults to the end of the work day.

 Format: HH:mm:ss

</td></tr></tbody>
</table><table id="table_ww4_gvb_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the completion date is within the schedule.Possible values:

-   true: Completion date is within the schedule.
-   false: Completion date falls outside the schedule. Undefined if no schedule was set prior to calling this method.

</td></tr></tbody>
</table>```
var dc = new DurationCalculator();
var startTime = new GlideDateTime();

// Settings for calculations
// Optional: Specify the schedule to use for the following calculations
dc.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
// Optional: Specify a different timezone to use
dc.setTimeZone("Los Angeles");
// Optional: Set a start date and time, otherwise the current time is assumed
dc.setStartDateTime("2020-04-10 08:00:00")
// Calculate end time, from number of seconds required in the schedule
dc.calcDuration(3*24*3600); // 3 days
dc.calcRelativeDueDate(startTime, "3", "07:00:00");
```

## DurationCalculator - calcRelativeDuration\(String relativeDurationID\)

Calculates the duration using the specified relative duration script.

Upon completion, the **this.endDateTime** and **this.seconds** properties are set to indicate the results of the calculation.

|Name|Type|Description|
|----|----|-----------|
|relativeDurationID|String|sys\_id of relative duration schedule \(table cmn\_relative\_duration\).|

|Type|Description|
|----|-----------|
|Boolean|The result of the duration script.|

```
var dc = new DurationCalculator();
dc.calcRelativeDuration('08fcd0830a0a1b2600074f56b1ad7cb');
```

## DurationCalculator - calcScheduleDuration\(String startTime, String endTime\)

Returns the duration between the **startTime** and the **endTime** within the already-specified schedule and optionally overridden timezone.

This method also sets **this.endDateTime**, **this.seconds**, and **this.totalSeconds** in the current schedule object.

<table id="table_lw4_gvb_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

startTime

</td><td>

String

</td><td>

Optional. Display value for the end time. Default: Uses the current date and time \(set using setStartDateTime\(\)\). You must pass a placeholder if this parameter it not passed, such as `dur.calcScheduleDuration("", endDateTime);`.

</td></tr><tr><td>

endTime

</td><td>

String

</td><td>

Optional. Display value for the start time.Default: Uses the current date and time \(set using setEndDateTime\(\)\).

</td></tr></tbody>
</table><table id="table_mw4_gvb_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Schedule duration. Returns 0 if **endTime** is before **startTime**.Unit: Seconds

</td></tr></tbody>
</table>```
var dur = new DurationCalculator();

// Set 9-5 weekday schedule. This is the schedule in which endDateTime, seconds, and totalseconds is set
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae');
dur.calcScheduleDuration("2019-01-02 11:00:00", "2019-01-06 09:00:00");
var secs = dur.getSeconds();
var totalSecs = dur.getTotalSeconds();
var endDateTime = dur.getEndDateTime() + "";

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output

```
***SCHEDULE DURATION: SECS=97200 TOTALSECS=338400 ENDTIME = 2019-01-06 09:00:00
```

## DurationCalculator - calcScheduleDuration\(GlideDateTime startTime, GlideDateTime endTime\)

Returns the duration between the **startTime** and the **endTime** within the already-specified schedule and optionally overridden timezone.

This method also sets **this.endDateTime**, **this.seconds**, and **this.totalSeconds** in the current schedule object.

<table id="table_nw4_gvb_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

startTime

</td><td>

GlideDateTime

</td><td>

Optional. GlideDateTime object that contains the start time to use. Default: Uses the current date and time \(set using setStartDateTime\(\)\). You must pass a placeholder if this parameter it not passed, such as `dur.calcScheduleDuration("", endDateTime);`.

</td></tr><tr><td>

endTime

</td><td>

GlideDateTime

</td><td>

Optional. GlideDateTime object that contains the end time to use. Default: Uses the current date and time \(set using setEndDateTime\(\)\).

</td></tr></tbody>
</table><table id="table_mw4_gvb_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Schedule duration. Returns 0 if **endTime** is before **startTime**.Unit: Seconds

</td></tr></tbody>
</table>```
var startDateTime = new GlideDateTime("2020-11-02 11:00:00");
// Instantiate a new GlideDateTime object which has the end date as the current date and time
var endDateTime = new GlideDateTime(); 
var dur = new DurationCalculator();

// Set 9-5 weekday schedule. This is the schedule in which endDateTime, seconds, and totalseconds is set
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
dur.calcScheduleDuration(startDateTime, endDateTime);
var secs = dur.getSeconds();
var totalSecs = dur.getTotalSeconds();

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output

```
***SCHEDULE DURATION: SECS=293734.24 TOTALSECS=970534 ENDTIME = 2020-11-13 16:35:34
```

## DurationCalculator - getEndDateTime\( \)

Gets the **endDateTime** property that was set by calcDuration/calcRelativeDuration, indicating the end date and time for the duration.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDateTime|The end datetime.|

```
var dc = new DurationCalculator();
dc.calcDuration(52);
gs.print(dc.getEndDateTime());
```

2012-04-17 20:57:27

## DurationCalculator - getSeconds\( \)

Returns the **this.seconds** property that was set by calcDuration/calcRelativeDuration, indicating the total number of seconds of work to be performed for the duration.

This is the total work time, not the total time between start and end times and may be used to determine percentages of the work time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The total work time, in seconds.|

```
var startDateTime = new GlideDateTime("2020-11-02 11:00:00");
// Instantiate a new GlideDateTime object which has the end date as the current date and time
var endDateTime = new GlideDateTime(); 
var dur = new DurationCalculator();

// Set 9-5 weekday schedule. This is the schedule in which endDateTime, seconds, and totalseconds is set
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
dur.calcScheduleDuration(startDateTime, endDateTime);
var secs = dur.getSeconds();
var totalSecs = dur.getTotalSeconds();

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output

```
***SCHEDULE DURATION: SECS=293734.24 TOTALSECS=970534 ENDTIME = 2020-11-13 16:35:34
```

## DurationCalculator - getTotalSeconds\( \)

Returns the **totalSeconds** value that was set by a call to calculate\(record\).

The **totalSeconds** property represents the total number of seconds between the start and end times of the duration, which includes both work and non-work.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The total number of seconds.|

```
var startDateTime = new GlideDateTime("2020-11-02 11:00:00");
// Instantiate a new GlideDateTime object which has the end date as the current date and time
var endDateTime = new GlideDateTime(); 
var dur = new DurationCalculator();

// Set 9-5 weekday schedule. This is the schedule in which endDateTime, seconds, and totalseconds is set
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
dur.calcScheduleDuration(startDateTime, endDateTime);
var secs = dur.getSeconds();
var totalSecs = dur.getTotalSeconds();

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output

```
***SCHEDULE DURATION: SECS=293734.24 TOTALSECS=970534 ENDTIME = 2020-11-13 16:35:34
```

## DurationCalculator - isAfter\(GlideDateTime dt, String tm\)

Compares the passed in time to the time value in the passed in GlideDateTime object.

<table id="table_tw4_gvb_4t" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dt

</td><td>

GlideDateTime or String

</td><td>

Either a GlideDateTime object or a display value date and time to compare to the passed in **tm** value. If you pass a display value date and time, the method converts it to a GlideDateTime object.

</td></tr><tr><td>

tm

</td><td>

String

</td><td>

Display value for the time to compare against the time value in the GlideDateTime object. Assumes same date.Format: HH:mm:ss

</td></tr></tbody>
</table><table id="table_uw4_gvb_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the passed in time value \(**tm**\) is after the time in the GlideDateTime object \(**dt**\). Possible values:

-   true: **tm** is after **dt**.
-   false **tm** is not after **dt**.

</td></tr></tbody>
</table>```
var dc = new DurationCalculator();
gs.print(dc.isAfter("2020-04-10 08:00:00", "09:00:00"));
```

\*\*\* Script: true

## DurationCalculator - setSchedule\(String schedId, String timezone\)

Sets the schedule and time zone to use for calculating the due date.

<table id="table_y5v_nlz_nt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

schedId

</td><td>

String

</td><td>

Sys\_id of the schedule to set. Table: Schedule \[cmn\_schedule\].

</td></tr><tr><td>

timezone

</td><td>

String

</td><td>

Optional. Time zone to set.Default: User's time zone.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following code example shows how to call this method.

```
var startDateTime = new GlideDateTime("2020-11-02 11:00:00");
// Instantiate a new GlideDateTime object which has the end date as the current date and time
var endDateTime = new GlideDateTime(); 
var dur = new DurationCalculator();

// Set 9-5 weekday schedule. This is the schedule in which endDateTime, seconds, and totalseconds is set
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
dur.calcScheduleDuration(startDateTime, endDateTime);
var secs = dur.getSeconds();
var totalSecs = dur.getTotalSeconds();

gs.print("***SCHEDULE DURATION: SECS=" + secs + " TOTALSECS=" + totalSecs + " ENDTIME = " + endDateTime);
```

Output:

```
***SCHEDULE DURATION: SECS=293734.24 TOTALSECS=970534 ENDTIME = 2020-11-13 16:35:34
```

## DurationCalculator - setStartDateTime\(String start\)

Sets the start date and time for the duration calculations.

|Name|Type|Description|
|----|----|-----------|
|start|String|Display value for the start time in GMT for subsequent calculations.|

|Type|Description|
|----|-----------|
|void| |

```
var dc = new DurationCalculator();
dc.setStartDateTime("2020-04-10 08:00:00")
```

## DurationCalculator - setStartDateTime\(GlideDateTime description\)

Sets the start date and time for the duration calculations.

|Name|Type|Description|
|----|----|-----------|
|description|GlideDateTime|GlideDateTime object that contains the start time in GMT for subsequent calculations.|

|Type|Description|
|----|-----------|
|void| |

```
var startDateTime = new GlideDateTime("2020-11-02 11:00:00"); 
var dur = new DurationCalculator();

// Set 9-5 weekday schedule.
dur.setSchedule('08fcd0830a0a0b2600079f56b1adb9ae'); 
dur.setStartDateTime(startDateTime);
```

## DurationCalculator - setTimeZone\(String timezone\)

Sets the time zone to use for calculating the due date.

|Name|Type|Description|
|----|----|-----------|
|timezone|String|Value of the time zone.|

|Type|Description|
|----|-----------|
|void| |

```
var dc = new DurationCalculator();
dc.setTimeZone("Los Angeles");
```

