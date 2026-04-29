---
title: GlideTime - Scoped
description: The GlideTime API provides methods for performing operations on GlideTime objects, such as instantiating GlideTime objects or working with GlideTime fields.Instantiates a GlideTime object with the current time.Instantiates a GlideTime object with its time starting at midnight UTC plus the passed in value.Returns the time in the specified format.Gets the time in the current user's display format and time zone.Returns the time using the current user's timezone and a specified format.Gets the display value in the current user's time zone and the internal format \(HH:mm:ss\).Returns the time using the current user's timezone and a specified format and language.Returns the hours part of the time using the local time zone.Returns the hours part of the time using the local time zone. The number of hours is based on a 24 hour clock.Returns the hours part of the time using the UTC time zone. The number of hours is based on a 24 hour clock.Returns the hours part of the time using the UTC time zone. The number of hours is based on a 12 hour clock. Noon and midnight are represented by 0, not 12.Returns the number of minutes using the local time zone.Returns the number of minutes in the hour based on the UTC time zone.Returns the number of seconds in the current minute.Gets the time value stored in the database by the GlideTime object in the internal format, HH:mm:ss, and the system time zone.Sets a time value using the current user's display format and time zone.Sets the time using the current user's timezone and a specified format.Sets the time using the current user's timezone and a specified format and language.Sets the time of the GlideTime object in the internal time zone.Gets the duration difference between two GlideTime object values.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
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

For information on the time formats that you can pass into this method, see [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US). You can pass these values in any order and add separators such as a dash, space, backslash, or colon. In addition, you can also pass the character "a" to return am/pm.

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

## GlideTime - getDisplayValueEx\(String style\)

Returns the time using the current user's timezone and a specified format.

<table id="table_tg4_ckc_b3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

style

</td><td>

String

</td><td>

Format to use for the time.Valid values \(case insensitive\):

-   `short`: HH:mm \(AM/PM\)
-   `medium`: HH:mm:ss \(AM/PM\)
-   `long`: HH:mm:ss \(AM/PM\) timezone abbreviation
-   `full`: HH:mm:ss \(AM/PM\) timezone

The time is returned in the current user's language. The language determines whether the time is returned in 12 hour or 24 hour format.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The time in the specified format.|

This example returns the time using the current user's timezone and each formatting option.

```
var gt = new GlideTime();
gs.info(gt.getDisplayValueEx("short"));
gs.info(gt.getDisplayValueEx("medium"));
gs.info(gt.getDisplayValueEx("long"));
gs.info(gt.getDisplayValueEx("full"));
```

Output:

```
8:52 AM  //short
8:52:24 AM  //medium
8:52:24 AM PST  //long
8:52:24 AM Pacific Standard Time  //full
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

## GlideTime - getDisplayValueLang\(String style, String language\)

Returns the time using the current user's timezone and a specified format and language.

<table id="table_ygv_fkc_b3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

style

</td><td>

String

</td><td>

Format to use for the time.Valid values \(case insensitive\):

-   `short`: HH:mm \(AM/PM\)
-   `medium`: HH:mm:ss \(AM/PM\)
-   `long`: HH:mm:ss \(AM/PM\) timezone abbreviation
-   `full`: HH:mm:ss \(AM/PM\) timezone

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Optional. Language to return the time in, provided as a BCP 47 language tag. For example, to return the time in Japanese use the tag `ja`.The language determines whether the time is returned in 12 hour or 24 hour format. For example, times in English use the 12 hour format, while times in Japanese use the 24 hour format.

Default: Current user's language.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The time in the specified format and language.|

This example returns the time in Spanish using the current user's timezone and each formatting option.

```
var gt = new GlideTime();
gs.info(gt.getDisplayValueLang("short", "es"));
gs.info(gt.getDisplayValueLang("medium", "es"));
gs.info(gt.getDisplayValueLang("long", "es"));
gs.info(gt.getDisplayValueLang("full", "es"));
```

Output:

```
9:25  //short
9:25:44  //medium
9:25:44 PST  //long
9:25:44 (hora estándar del Pacífico)  //full
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

## GlideTime - setDisplayValueEx\(String time, String style\)

Sets the time using the current user's timezone and a specified format.

<table id="table_zb5_3kc_b3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

time

</td><td>

String

</td><td>

Value to set for the time. The [getDisplayValueEx\(\)](c_GlideTimeScopedAPI.md#) method returns times in a valid format, or times can be formatted as shown below.

-   HH:mm \(AM/PM\)
-   HH:mm:ss \(AM/PM\)
-   HH:mm:ss \(AM/PM\) timezone abbreviation
-   HH:mm:ss \(AM/PM\) timezone

The current user's language determines whether 12 hour \(AM/PM\) or 24 hour time values are accepted. For example, if the current user's language is English `6:25 PM PST` is a valid value while `18:25 PST` is not.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Format to use for the time.You must use the same format as the provided **time** value.

Valid values \(case insensitive\):

-   `short`: HH:mm \(AM/PM\)
-   `medium`: HH:mm:ss \(AM/PM\)
-   `long`: HH:mm:ss \(AM/PM\) timezone abbreviation
-   `full`: HH:mm:ss \(AM/PM\) timezone

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example sets the time using the current user's timezone and a specified format.

```
gt = new GlideTime();
gt.setDisplayValueEx("8:25:25 AM", "medium");
gs.info(gt.getDisplayValueEx("full"));
```

Output:

```
8:25:25 AM Pacific Standard Time
```

## GlideTime - setDisplayValueLang\(String time, String style, String language\)

Sets the time using the current user's timezone and a specified format and language.

<table id="table_zb5_3kc_b3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

time

</td><td>

String

</td><td>

Value to set for the time. The [getDisplayValueLang\(\)](c_GlideTimeScopedAPI.md#) and [getDisplayValueEx\(\)](c_GlideTimeScopedAPI.md#) methods return times in a valid format, or times can be formatted as shown below.

-   HH:mm \(AM/PM\)
-   HH:mm:ss \(AM/PM\)
-   HH:mm:ss \(AM/PM\) timezone abbreviation
-   HH:mm:ss \(AM/PM\) timezone

The **language** parameter determines whether 12 hour \(AM/PM\) or 24 hour time values are accepted. For example, if the language is `en` \(English\), `6:25 PM PST` is a valid value while `18:25 PST` is not.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Format to use for the time.You must use the same format as the provided **time** value.

Valid values \(case insensitive\):

-   `short`: HH:mm \(AM/PM\)
-   `medium`: HH:mm:ss \(AM/PM\)
-   `long`: HH:mm:ss \(AM/PM\) timezone abbreviation
-   `full`: HH:mm:ss \(AM/PM\) timezone

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Language to set the time in, provided as a BCP 47 language tag. For example, to set the time in Japanese, use the tag `ja`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example sets the time in English using the current user's timezone and retrieves it in Spanish.

```
gt = new GlideTime();
gt.setDisplayValueLang("4:15:00 PM PST", "long", "en");
gs.info(gt.getDisplayValueLang("full", "es"));
```

Output:

```
16:15:00 (hora estándar del Pacífico)
```

## GlideTime - setValue\(String o\)

Sets the time of the GlideTime object in the internal time zone.

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

