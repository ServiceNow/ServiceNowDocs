---
title: GlideSchedule - Scoped
description: The scoped GlideSchedule API provides methods for performing operations on GlideSchedule objects, such as adding new schedule segments to a schedule, determining if a date/time is within the schedule, or setting the schedule timezone.Instantiates an empty GlideSchedule object.Instantiates a GlideSchedule object and loads the schedule information. If a time zone is not specified, the current session time zone is used.Adds a new schedule segment to the current schedule.Determines the elapsed time in the schedule between two date time values using the timezone of the schedule or, if that is not specified, the timezone of the session.Retrieves the schedule name.Determines if the specified date and time is within the current schedule.Determines if the current schedule is valid. A schedule is valid if it has at least one schedule span.Loads a schedule with the schedule information.Sets the timezone for the current schedule.Determines how much time \(in milliseconds\) until start time of the next schedule item.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSchedule- Scoped

The scoped GlideSchedule API provides methods for performing operations on GlideSchedule objects, such as adding new schedule segments to a schedule, determining if a date/time is within the schedule, or setting the schedule timezone.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSchedule - GlideSchedule\(\)

Instantiates an empty GlideSchedule object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideSchedule - GlideSchedule\(String sysID, String timeZone\)

Instantiates a GlideSchedule object and loads the schedule information. If a time zone is not specified, the current session time zone is used.

<table id="table_emk_4cg_1r" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysID

</td><td>

String

</td><td>

The system ID for the schedule.

</td></tr><tr><td>

timeZone

</td><td>

String

</td><td>

Optional. The time zone to use.Default: The current session time zone.

Time zones can be provided in the following formats.

-   `Country/City`. For example, `America/Los_Angeles`.
-   `Country/Time zone`. For example, `US/Pacific`.
-   `Time zone abbreviation`. For example, `PST`.

For a complete list of valid timezones, see the **Time zone** field in the User \[sys\_user\] table. For more information about time zones, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>```
var schedule = new GlideSchedule('090eecae0a0a0b260077e1dfa71da828', 'US/Pacific');
```

## GlideSchedule - add\(GlideDateTime startDate, GlideDuration offSet\)

Adds a new schedule segment to the current schedule.

|Name|Type|Description|
|----|----|-----------|
|startDate|GlideDateTime|The starting date of the new schedule segment.|
|offSet|GlideDuration|The time offset of the new schedule segment.|

|Type|Description|
|----|-----------|
|GlideDateTime|The schedule updated with the new schedule segment.|

```
var startDate = new GlideDateTime('2014-01-02');
var days = 2;
var dur = new GlideDuration(60 * 60 * 24 * 1000 * days);
var schedule = new GlideSchedule();
var end = schedule.add(startDate, dur);
gs.info(end);
```

Output:

```
2014-01-04 00:00:00
```

## GlideSchedule - duration\(GlideDateTime startDate, GlideDateTime endDate\)

Determines the elapsed time in the schedule between two date time values using the timezone of the schedule or, if that is not specified, the timezone of the session.

|Name|Type|Description|
|----|----|-----------|
|startDate|GlideDateTime|The starting datetime.|
|endDate|GlideDateTime|The ending datetime.|

|Type|Description|
|----|-----------|
|GlideDuration|The difference between the starting and ending datetime.|

```
var startDate = new GlideDateTime('2014-10-16 02:00:00');
var endDate = new GlideDateTime('2014-10-18 04:00:00');
var schedule = new GlideSchedule();
 
schedule.load('090eecae0a0a0b260077e1dfa71da828'); // loads "8-5 weekdays excluding holidays" schedule
var duration = schedule.duration(startDate, endDate);
gs.info(duration.getDurationValue()); // gets the elapsed time in schedule
```

## GlideSchedule - getName\(\)

Retrieves the schedule name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the current schedule.|

```
sys_id ='04e664654a36232701a2247dcd8fc4cf'; // sys_id for "Application" schedule record
var sched = new GlideSchedule(sys_id);
gs.info(sched.getName());
```

## GlideSchedule - isInSchedule\(GlideDateTime time\)

Determines if the specified date and time is within the current schedule.

|Name|Type|Description|
|----|----|-----------|
|time|GlideDateTime|Date and time value to check.|

<table id="table_nvd_jkg_1r" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the specified date and time is within the schedule.Valid values:

-   true: Date and time is within the schedule.
-   false: Date and time are outside of the schedule.

</td></tr></tbody>
</table>```
var glide = new GlideRecord('cmn_schedule');
glide.addQuery('type', 'blackout');
glide.query();
if (glide.next()) {
   var sched = new GlideSchedule(glide.sys_id);
   var date = new GlideDateTime();
   date.setDisplayValue("2007-09-18 12:00:00");
   if (sched.isInSchedule(date)) 
      gs.info("Is in the schedule");
   else
      gs.info("Is NOT in the schedule");
}
```

## GlideSchedule - isValid\(\)

Determines if the current schedule is valid. A schedule is valid if it has at least one schedule span.

|Type|Description|
|----|-----------|
|Boolean|True if the schedule is valid.|

```
var glide = new GlideRecord('cmn_schedule');
glide.addQuery('type', 'blackout');
glide.query();
if (glide.next()) {
   var sched = new GlideSchedule(glide.sys_id);
   var date = new GlideDateTime();
   date.setDisplayValue("2007-09-18 12:00:00");
   if (sched.isValid()) 
      gs.info("Is valid");
 
   else
      gs.info("Is not valid");
}
```

## GlideSchedule - load\(String sysID, String timeZone, String excludeSpanID\)

Loads a schedule with the schedule information.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|The system ID of the schedule.|
|timeZone|String|\(Optional\) The timezone. If a timezone is not specified, or is nil, the current session timezone is used for the schedule.|
|excludeSpanID|String|Any span to exclude.|

|Type|Description|
|----|-----------|
|void| |

```
var x = new GlideSchedule();
x.load('08fcd0830a0a0b2600079f56b1adb9ae');
```

## GlideSchedule - setTimeZone\(String timeZone\)

Sets the timezone for the current schedule.

<table id="table_sdh_hzg_1r" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

timeZone

</td><td>

String

</td><td>

The time zone to use.Time zones can be provided in the following formats.

-   `Country/City`. For example, `America/Los_Angeles`.
-   `Country/Time zone`. For example, `US/Pacific`.
-   `Time zone abbreviation`. For example, `PST`.

For a complete list of valid timezones, see the **Time zone** field in the User \[sys\_user\] table. For more information about time zones, see [Time zones](https://www.servicenow.com/docs/access?context=r_TimeZones&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example sets the timezone for the schedule to US/Pacific.

```
var schedule = new GlideSchedule();
schedule.setTimeZone('US/Pacific');
```

## GlideSchedule - whenNext\(GlideDateTime time, String timeZone\)

Determines how much time \(in milliseconds\) until start time of the next schedule item.

This function is intended to be called when the GlideSchedule object \(cmn\_schedule table\) is not currently in the schedule window. The whenNext\(\) call returns duration \(in ms\) until the GlideSchedule object is within the schedule. This function does not return a meaningful value if called when the GlideSchedule object is within the schedule.

|Name|Type|Description|
|----|----|-----------|
|time|GlideDateTime|Time to be evaluated|
|timeZone|String|Timezone|

|Type|Description|
|----|-----------|
|Number|Number of milliseconds until the start time of the next schedule item. Returns -1 if never.|

```
var startDate = new GlideDateTime('2014-10-25 08:00:00');
var glideSchedule = new GlideSchedule('08fcd0830a0a0b2600079f56b1adb9ae', 'UTC');
gs.info(glideSchedule.whenNext(startDate));
```

Output:

```
172800000
```

```
testScript(); 
function testScript() { 
var now = new GlideDateTime(); //current date and time
var sched = new GlideSchedule("<sys_id>"); // Use a cmn_schedule sys_id 
if (sched.isInSchedule(now)){ 
gs.info('We are in an active schedule window so whenNext() is not helpful'); 
} else{  
gs.info('Not currently in schedule so call whenNext()'); 
var msUntilNext = sched.whenNext(new GlideDateTime(), 'US/Pacific'); 
gs.info('Next schedule starts in '+msUntilNext+' milliseconds'); 
} 
}
\\ Output [schedule inactive)]:
\\ *** Script: Not currently in schedule so call whenNext() 
\\ *** Script: Next schedule starts in -1 milliseconds
```

Output:

```
[Scheduled for future] *** Script: Not currently in schedule *** Script: Next schedule starts in 332894000 milliseconds
```

