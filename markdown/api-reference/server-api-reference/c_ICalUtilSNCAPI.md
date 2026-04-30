---
title: ICalUtilSNC - Global
description: The ICalUtilSNC script include provides functions to generate iCalendar compliant events.Generates a formatted VCALENDAR component.Generates a formatted VEVENT.Formats the RRULE property for a VEVENT.Returns the date from the GlideScheduleDateTime.Returns a GlideScheduleDateTime object based on the passed date and time string.Returns the time from the GlideScheduleDateTime.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ICalUtilSNC- Global

The ICalUtilSNC script include provides functions to generate iCalendar compliant events.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ICalUtilSNC - formatICalComponent\(Array arrEvents\)

Generates a formatted VCALENDAR component.

|Name|Type|Description|
|----|----|-----------|
|arrEvents|Array|Properties that make up a VCALENDAR component.|

|Type|Description|
|----|-----------|
|Array|Properties needed to form a VCALENDAR.|

## ICalUtilSNC - formatICalEvent\(Array arrEvent, Boolean useAlarm\)

Generates a formatted VEVENT.

|Name|Type|Description|
|----|----|-----------|
|arrEvent|Array|Contains the individual properties that make up a VEVENT.|
|useAlarm|Boolean|If true, adds a VALARM to the VEVENT.|

|Type|Description|
|----|-----------|
|String|The formatted VEVENT.|

## ICalUtilSNC - formatRecurringRule \(Object ruleObj\)

Formats the RRULE property for a VEVENT.

|Name|Type|Description|
|----|----|-----------|
|ruleObj|Object|Contains the properties for the RRULE property.|

|Type|Description|
|----|-----------|
|String|The formatted RRULE property.|

## ICalUtilSNC - getDateFromScheduleDateTime \(GlideScheduleDateTime scheduleDateTime\)

Returns the date from the GlideScheduleDateTime.

|Name|Type|Description|
|----|----|-----------|
|scheduleDateTime|GlideScheduleDateTime|A GlideScheduleDateTime representation of the date and time.|

|Type|Description|
|----|-----------|
|String|Formatted date.|

### cURL example

```
var scheduleDateTime = new GlideScheduleDateTime();
var myICalUtilSNC = new ICalUtilSNC();
var scheduleDate = myICalUtilSNC.getDateFromScheduleDateTime(scheduleDateTime);

gs.info(scheduleDateTime);
gs.info(scheduleDate);
```

Output:

```
2023-02-08 09:05:22
20230208
```

## ICalUtilSNC - getSDT\(String sdtStr, String timeZone\)

Returns a GlideScheduleDateTime object based on the passed date and time string.

|Name|Type|Description|
|----|----|-----------|
|sdtStr|String|Formatted ScheduleDateTime.|
|timeZone|String|Optional. Time zone to use when generating the GlideScheduleDateTime object.|

|Type|Description|
|----|-----------|
|GlideScheduleDateTime|A GlideScheduleDateTime representation of the passed date and time string.|

## ICalUtilSNC - getTimeFromScheduleDateTime \(GlideScheduleDateTime scheduleDateTime\)

Returns the time from the GlideScheduleDateTime.

|Name|Type|Description|
|----|----|-----------|
|scheduleDateTime|GlideScheduleDateTime|A GlideScheduleDateTime representation of the date and time.|

|Type|Description|
|----|-----------|
|String|Formatted time.|

The following code example shows how to call this method.

```
var scheduleDateTime = new GlideScheduleDateTime();
var myICalUtilSNC = new ICalUtilSNC();
var scheduleDate = myICalUtilSNC.getTimeFromScheduleDateTime(scheduleDateTime);

gs.info(scheduleDateTime);
gs.info(scheduleDate);
```

Output:

```
2023-02-08 10:21:43
102143Z
```

