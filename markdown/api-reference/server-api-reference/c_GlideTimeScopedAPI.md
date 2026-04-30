---
title: GlideTime - Scoped
description: The GlideTime API provides methods for performing operations on GlideTime objects, such as instantiating GlideTime objects or working with GlideTime fields.Instantiates a GlideTime object with the current time.Instantiates a GlideTime object with its time starting at midnight UTC plus the passed in value.Returns the time in the specified format.Gets the time in the current user's display format and time zone.Gets the display value in the current user's time zone and the internal format \(HH:mm:ss\).Returns the hours part of the time using the local time zone.Returns the hours part of the time using the local time zone. The number of hours is based on a 24 hour clock.Returns the hours part of the time using the UTC time zone. The number of hours is based on a 24 hour clock.Returns the hours part of the time using the UTC time zone. The number of hours is based on a 12 hour clock. Noon and midnight are represented by 0, not 12.Returns the number of minutes using the local time zone.Returns the number of minutes in the hour based on the UTC time zone.Returns the number of seconds in the current minute.Gets the time value stored in the database by the GlideTime object in the internal format, HH:mm:ss, and the system time zone.Sets a time value using the current user's display format and time zone.Sets the time of the GlideTime object in the internal time zone.Gets the duration difference between two GlideTime object values.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTime- Scoped

The GlideTime API provides methods for performing operations on GlideTime objects, such as instantiating GlideTime objects or working with GlideTime fields.

For guidance on date time input strings with a list of common format conflicts, refer to [Date and time format guidelines](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideTime - GlideTime\(\)

Instantiates a GlideTime object with the current time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var gt = new GlideTime(); 
gs.info(gt.getDisplayValue());
```

## GlideTime - GlideTime\(Number milliseconds\)

Instantiates a GlideTime object with its time starting at midnight UTC plus the passed in value.

The value is adjusted for the timezone in which the instance resides. For example, if the user's instance is in a time zone that is -8 hours from the UTC, and 1000 is passed in, the time in the GlideTime object is 16:00:10 \(00:00:00 - 8 hours +10 seconds.\)

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

milliseconds

</td><td>

Number

</td><td>

Time to add to midnight UTC.Unit: Milliseconds

</td></tr></tbody>
</table>This example shows adding 10 seconds to midnight \(UTC\), which is then adjusted for the time zone in which the instance resides. In this case, -8 hours from UTC.

```
var gt = new GlideTime(10000); 
gs.info(gt.getDisplayValue());
```

Output:

```
16:00:10
```

## GlideTime - getByFormat\(String format\)

Returns the time in the specified format.

For information on the time formats that you can pass into this method, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US). You can pass these values in any order and add separators such as a dash, space, backslash, or colon. In addition, you can also pass the character "a" to return am/pm.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

format

</td><td>

String

</td><td>

String to use to format the time.For example, if the current time is 10:30:20 then:

-   hh:mm:ss = 10:30:20
-   HH = 10
-   HH –- ss = 10 –- 20
-   hh a = 10 AM
-   s:m:H ss:mm:hh = 20:30:10 20:30:10
-   HH/mm/ss = 10/30/20

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Time in the specified format.|

```
var gt = new GlideTime(); 
gt.setValue('12:00:00');
gs.info(gt.getByFormat("HH:mm"));
```

Output:

```
12:00
```

## GlideTime - getDisplayValue\(\)

Gets the time in the current user's display format and time zone.

When designing business rules or script includes remember that this method may return values in different formats for different users.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The time in the user's format and time zone.|

```
var gt = new GlideTime();
gt.setDisplayValue("12:00:00"); // User Time Zone
gs.info(gt.getDisplayValue()); // User Time Zone
```

## GlideTime - getDisplayValueInternal\(\)

Gets the display value in the current user's time zone and the internal format \(HH:mm:ss\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The time value for the GlideTime object in the current user's time zone and the internal time format of HH:mm:ss.|

```
var gt = new GlideTime();
gt.setValue("01:00:00"); //Internal Time Zone , UTC
gs.info(gt.getDisplayValueInternal()); //User Time Zone
```

## GlideTime - getHourLocalTime\(\)

Returns the hours part of the time using the local time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The hours using the local time zone.|

## GlideTime - getHourOfDayLocalTime\(\)

Returns the hours part of the time using the local time zone. The number of hours is based on a 24 hour clock.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The hours using the local time zone. The number of hours is based on a 24 hour clock.|

## GlideTime - getHourOfDayUTC\(\)

Returns the hours part of the time using the UTC time zone. The number of hours is based on a 24 hour clock.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The hours using the UTC time zone. The number of hours is based on a 24 hour clock.|

## GlideTime - getHourUTC\(\)

Returns the hours part of the time using the UTC time zone. The number of hours is based on a 12 hour clock. Noon and midnight are represented by 0, not 12.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The hours using the UTC time zone. The number of hours is based on a 12 hour clock. Noon and midnight are represented by 0, not 12.|

## GlideTime - getMinutesLocalTime\(\)

Returns the number of minutes using the local time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of minutes using the local time zone.|

## GlideTime - getMinutesUTC\(\)

Returns the number of minutes in the hour based on the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of minutes in the hour using the UTC time zone.|

## GlideTime - getSeconds\(\)

Returns the number of seconds in the current minute.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of seconds in the minute.|

## GlideTime - getValue\(\)

Gets the time value stored in the database by the GlideTime object in the internal format, HH:mm:ss, and the system time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The time value in the internal fomat and system time zone.|

```
var gt = new GlideTime();
gs.info(gt.getValue()); // Internal Time Zone, UTC
```

## GlideTime - setDisplayValue\(String asDisplayed\)

Sets a time value using the current user's display format and time zone.

|Name|Type|Description|
|----|----|-----------|
|asDisplayed|String|The time in the current user's display format and time zone. The parameter must be formatted using the current user's preferred display format, such as HH:mm:ss.|

|Type|Description|
|----|-----------|
|None| |

```
var gt = new GlideTime();
gt.setDisplayValue('01:00:00');   // User Time Zone
gs.info(gt.getDisplayValueInternal()); // User Time Zone
```

## GlideTime - setValue\(String o\)

Sets the time of the GlideTime object in the internal time zone.

If invalid data is provided to this method, the underlying time is set to 00:00:00.

|Name|Type|Description|
|----|----|-----------|
|o|String|The time in hh:mm:ss format.|

|Type|Description|
|----|-----------|
|None| |

```
var gt = new GlideTime();
gt.setValue('01:00:00');  //Internal Time Zone, UTC
gs.info("time is "+ gt.getByFormat('hh:mm:ss'));
```

## GlideTime - subtract\(GlideTime startTime, GlideTime endTime\)

Gets the duration difference between two GlideTime object values.

|Name|Type|Description|
|----|----|-----------|
|startTime|GlideTime|The start value.|
|endTime|GlideTime|The end value.|

|Type|Description|
|----|-----------|
|GlideDuration|The duration between the two values.|

```
var gd1 = new GlideTime(); 
gd1.setDisplayValue("09:00:00"); 
var gd2 = new GlideTime(); 
gd2.setDisplayValue("09:10:00"); 
 
var dur = GlideDate.subtract(gd1, gd2); //the difference between gdt1 and gdt2 
gs.info(dur.getDisplayValue());
```

