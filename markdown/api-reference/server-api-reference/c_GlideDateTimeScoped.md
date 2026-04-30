---
title: GlideDateTime - Scoped
description: The scoped GlideDateTime class provides methods for performing operations on GlideDateTime objects.Instantiates a new GlideDateTime object with the current date and time.Instantiates a new GlideDateTime object using the passed-in date and time value.Instantiates a new GlideDateTime object set to the time of a specified GlideDateTime object.Adds a GlideTime object to the current GlideDateTime object.Adds the specified number of milliseconds to the current GlideDateTime object.Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the local date and time values.Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the UTC date and time values.Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the local date and time values.Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the UTC date and time values.Adds the specified number of seconds to the current GlideDateTime object.Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the local date and time values.Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the UTC date and time values.Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts years using the local date and time values.Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years. The date and time value stored by GlideDateTime object is interpreted as being in the UTC time zone.Determines if the GlideDateTime object's date and time occurs after the specified object's date and time.Determines if the GlideDateTime object's date and time occurs before the specified GlideDateTime object's date and time.Compares two date and time objects to determine whether they are equivalent or one occurs before or after the other.Compares a datetime with an existing value for equality.Returns the date stored by the GlideDateTime object. Expressed in the standard format, yyyy-MM-dd, and in the system time zone, GMT by default.Gets the day of the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the day of the month stored by the GlideDateTime object, expressed in the UTC time zone.Gets the day of the week stored by the GlideDateTime object, expressed in the user's time zone.Returns the day of the week stored by the GlideDateTime object, expressed in the UTC time zone.Gets the number of days in the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.Gets the date and time value in the current user's display format and time zone.Gets the display value in the internal format \(yyyy-MM-dd HH:mm:ss\).Returns a date and time value in the current users' locale according to a specified language and date style.Gets the amount of time that daylight saving time is offset.Gets the current error message.Returns the object's time in the local time zone and in the internal format.Gets the date stored by the GlideDateTime object, expressed in the standard format, yyyy-MM-dd, and the current user's time zone.Returns a GlideTime object that represents the time portion of the GlideDateTime object in the user's time zone.Gets the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the month stored by the GlideDateTime object, expressed in the UTC time zone.Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.Returns a GlideTime object that represents the time portion of the GlideDateTime object.Gets the time zone offset in milliseconds.Returns the object's time in the local time zone and in the user's format.Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, in the UTC time zone.Gets the number of the week stored by the GlideDateTime object, expressed in the current user's time zone.Gets the number of the week stored by the GlideDateTime object, expressed in the UTC time zone.Gets the year stored by the GlideDateTime object, expressed in the current user's time zone.Gets the year stored by the GlideDateTime object, expressed in the UTC time zone.Determines if an object's date is set.Determines if an object's time uses a daylight saving offset.Determines if a value is a valid date and time.Determines if the GlideDateTime object's data and time occurs on or after the specified GlideDateTime object's date and time.Determines if the GlideDateTime object's data and time occurs on or before the specified GlideDateTime object's date and time.Sets the day of the month to a specified value in the current user's time zone.Sets the day of the month to a specified value in the UTC time zone.Sets a date and time value using the current user's display format and time zone.Sets a date and time value using the current user's time zone and the specified date and time format.Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.Sets a date and time using a specified style and format according to the current user's locale.Sets a date and time using a specified style, language, and format according to the current user's locale.Sets the date and time of the current object using an existing GlideDateTime object. This method is equivalent to instantiating a new object with a GlideDateTime parameter.Sets the month stored by the GlideDateTime object to the specified value using the current user's time zone.Sets the month stored by the GlideDateTime object to the specified value using the UTC time zone.Sets the date and time of the GlideDateTime object.Sets a date and time value using the UTC time zone and the specified date and time format. This method throws a runtime exception if the date and time format used in the dt parameter does not match the format parameter. You can retrieve the error message by calling getErrorMsg\(\) on the GlideDateTime object after the exception is caught.Sets the year stored by the GlideDateTime object to the specified value using the current user's time zone.Sets the year stored by the GlideDateTime object to the specified value using the UTC time zone.Subtracts a specified amount of time from the current GlideDateTime object.Subtracts the specified number of milliseconds from the GlideDateTime object.Returns the duration difference between two specified GlideDateTime objects.Gets the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, and the system time zone, UTC by default. This method is equivalent to getValue\(\).
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 28
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDateTime- Scoped

The scoped GlideDateTime class provides methods for performing operations on GlideDateTime objects.

Use the GlideDateTime methods to perform date-time operations, such as instantiating a GlideDateTime object, performing date-time calculations, formatting a date-time, or converting between date-time formats.

For guidance on date time input strings with a list of common format conflicts, refer to [Date and time format guidelines](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideDateTime - GlideDateTime\(\)

Instantiates a new GlideDateTime object with the current date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

This example instantiates a GlideDateTime object.

```
var gdt = new GlideDateTime();
gs.info(gdt);
```

Output:

```
2022-08-08 16:51:44
```

## Scoped GlideDateTime - GlideDateTime\(String value\)

Instantiates a new GlideDateTime object using the passed-in date and time value.

The system attempts to match the passed-in value with the specified internal system format. If the argument does not match the system format, the system attempts to match it to one of the following formats in this order:

-   yyyy-MM-dd HH:mm:ss
-   MM/dd/yyyy HH:mm:ss
-   MM-dd-yyyy HH:mm:ss
-   MM-dd-yyyy HH:mm
-   MM-dd-yyyy
-   MM/dd/yyyy
-   dd-MM-yyyy HH:mm:ss
-   dd-MM-yyyy HH.mm.ss
-   dd-MM-yyyy HH.mm
-   dd-MM-yy HH.mm.ss
-   dd/MM/yyyy
-   dd-MM-yyyy
-   yyyy-MM-dd HH:mm
-   yyyy-MM-dd
-   dd.MM.yyyy HH:mm:ss
-   dd.MM.yyyy HH.mm.ss
-   dd.MM.yyyy hh:mm:ss a
-   dd.MM.yyyy hh.mm.ss a
-   dd.MM.yyyy

**Note:** The following format is not supported:

-   yyyy-MM-dd'T'HH:mm:ss.SSSZ

|Name|Type|Description|
|----|----|-----------|
|value|String|UTC date and time to set in the GlideDateTime object.|

This example shows how to instantiate a GlideDateTime object using a string.

```
var gdt = new GlideDateTime("2023-01-01 12:00:00");
gs.info(gdt);
```

Output:

```
2023-01-01 12:00:00
```

## Scoped GlideDateTime - GlideDateTime\(GlideDateTime g\)

Instantiates a new GlideDateTime object set to the time of a specified GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|g|GlideDateTime|Object used to set the time of the new object.|

This example shows how to instantiate a GlideDateTime object \(gdt1\) using a string in the format `yyyy-MM-dd HH:mm:ss`, and a second GlideDateTime object \(gdt2\) using gdt1.

```
var gdt1 = new GlideDateTime("2025-01-28 12:00:00"); // GlideDateTime(String g)
var gdt2 = new GlideDateTime(gdt1); // GlideDateTime(GlideDateTime g)
gs.info(gdt1);
gs.info(gdt2);
```

Output:

```
2025-01-28 12:00:00
2025-01-28 12:00:00
```

## Scoped GlideDateTime - add\(GlideTime gd\)

Adds a GlideTime object to the current GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|gd|GlideTime|GlideTime object whose time value to add to the specified GlideDateTime object.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
var gtime1 = new GlideTime();
gtime1.setValue("00:00:20");
gdt.add(gtime1);
var gtime2 = gdt.getTime();
gs.info(gtime2.getByFormat('hh:mm:ss'));
```

Output:

```
08:00:20
```

## Scoped GlideDateTime - add\(Number milliseconds\)

Adds the specified number of milliseconds to the current GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|The number of milliseconds to add.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getNumericValue());
gdt.add(10);
gs.info(gdt.getNumericValue());
```

Output:

```
1314777600000 1314777600010
```

## Scoped GlideDateTime - addDaysLocalTime\(Number days\)

Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|days|Number|The number of days to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addDaysLocalTime(-1);
gs.info(gdt.getLocalDate());
```

Output:

```
2011-08-30
```

## Scoped GlideDateTime - addDaysUTC\(Number days\)

Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the UTC date and time values.

|Name|Type|Description|
|----|----|-----------|
|days|Number|The number of days to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addDaysUTC(-1);
gs.info(gdt.getDate());
```

Output:

```
 2011-08-30
```

## Scoped GlideDateTime - addMonthsLocalTime\(Number months\)

Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|months|Number|The number of months to add. use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addMonthsLocalTime(2);
gs.info(gdt.getDate());
```

Output:

```
2011-10-31
```

## Scoped GlideDateTime - addMonthsUTC\(Number months\)

Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the UTC date and time values.

|Name|Type|Description|
|----|----|-----------|
|months|Number|The number of months to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addMonthsUTC(2);
gs.info(gdt.getDate());
```

Output:

```
2011-10-31
```

## Scoped GlideDateTime - addSeconds\(Number seconds\)

Adds the specified number of seconds to the current GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|seconds|Number|The number of seconds to add.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-12-07 08:00:00");
gdt.addSeconds(1000);
gs.info(gdt.getValue());
```

Output:

```
2011-12-07 08:16:40
```

## Scoped GlideDateTime - addWeeksLocalTime\(Number weeks\)

Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|weeks|Number|The number of weeks to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addWeeksLocalTime(-1);
gs.info(gdt.getDate());
```

Output:

```
2011-08-24
```

## Scoped GlideDateTime - addWeeksUTC\(Number weeks\)

Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks. The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the UTC date and time values.

|Name|Type|Description|
|----|----|-----------|
|weeks|Number|The number of weeks to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addWeeksUTC(-1);
gs.info(gdt.getDate());
```

Output:

```
2011-08-24
```

## Scoped GlideDateTime - addYearsLocalTime\(Number years\)

Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years. The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts years using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|years|Number|The number of years to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2010-08-31 08:00:00");
gdt.addYearsLocalTime(1);
gs.info(gdt.getDate());
```

Output:

```
2011-08-31
```

## Scoped GlideDateTime - addYearsUTC\(Number years\)

Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years. The date and time value stored by GlideDateTime object is interpreted as being in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|years|Number|The number of years to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2010-08-31 08:00:00");
gdt.addYearsUTC(1);
gs.info(gdt.getDate());
```

Output:

```
2011-08-31
```

## Scoped GlideDateTime - after\(GlideDateTime gdt\)

Determines if the GlideDateTime object's date and time occurs after the specified object's date and time.

|Name|Type|Description|
|----|----|-----------|
|gdt|GlideDateTime|Date and time to check against.|

<table id="table_pp2_nqq_yv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the GlideDateTime object's date and time is after the date and time specified by the parameter.Possible values:

-   true: GlideDateTime object date and time is after the specified object's date and time.
-   false: GlideDateTime object date and time is before or equal to the specified object's date and time.

</td></tr></tbody>
</table>```
var gdt1 = new GlideDateTime("2016-05-09 10:11:12");
var gdt2 = new GlideDateTime("2017-06-12 15:11:12");
gs.info(gdt1.after(gdt2)); 
```

Output:

```
False
```

## Scoped GlideDateTime - before\(GlideDateTime gdt\)

Determines if the GlideDateTime object's date and time occurs before the specified GlideDateTime object's date and time.

|Name|Type|Description|
|----|----|-----------|
|gdt|GlideDateTime|Date and time to check against.|

<table id="table_k5h_vrq_yv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the GlideDateTime object's date and time is before the date and time specified by the parameter.Possible values:

-   true: GlideDateTime object date and time is before the specified date and time.
-   false: GlideDateTime object date and time is after or equal to the specified date and time.

</td></tr></tbody>
</table>```
var gdt1 = new GlideDateTime("2016-05-09 10:11:12");
var gdt2 = new GlideDateTime("2017-06-12 15:11:12");
gs.info(gdt1.before(gdt2));  
```

Output

```
true
```

## Scoped GlideDateTime - compareTo\(Object o\)

Compares two date and time objects to determine whether they are equivalent or one occurs before or after the other.

|Name|Type|Description|
|----|----|-----------|
|o|Object|Date and time object in GlideDateTime format|

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

-   0 = Dates are equal
-   1 = The object's date is after the date specified in the parameter
-   -1 = The object's date is before the date specified in the parameter

</td></tr></tbody>
</table>```
var initDate = new GlideDateTime("2011-08-01 12:00:00");
var compDate1 = new GlideDateTime("2011-08-01 12:00:00");
var compDate2 = new GlideDateTime("2011-07-31 12:00:00");
var compDate3 = new GlideDateTime("2011-08-04 16:00:00");
 
gs.info(initDate.compareTo(compDate1)); // Equals (0)
gs.info(initDate.compareTo(compDate2)); // initDate is after compDate2 (1)
gs.info(initDate.compareTo(compDate3)); // initDate is before compDate3 (-1)
```

Output:

```
0
1
-1
```

## Scoped GlideDateTime - equals\(Object dateTime\)

Compares a datetime with an existing value for equality.

|Name|Type|Description|
|----|----|-----------|
|dateTime|GlideDateTime object or String|The datetime to compare.|

|Type|Description|
|----|-----------|
|Boolean|Returns true if they are equal; otherwise, false.|

```
var gdt = new GlideDateTime("2011-08-31 00:00:00");
gs.info(gdt.equals("2011-09-30 00:12:01"));
```

Output:

```
false
```

## Scoped GlideDateTime - getDate\(\)

Returns the date stored by the GlideDateTime object. Expressed in the standard format, yyyy-MM-dd, and in the system time zone, GMT by default.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Date in the system time zone.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getDate());
```

Output:

```
2011-08-31
```

## Scoped GlideDateTime - getDayOfMonthLocalTime\(\)

Gets the day of the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the user's time zone, from 1 to 31.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00");
gs.info(gdt.getDayOfMonthLocalTime());
```

Output:

```
2
```

## Scoped GlideDateTime - getDayOfMonthUTC\(\)

Gets the day of the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the UTC time zone, from 1 to 31.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00");
gs.info(gdt.getDayOfMonthUTC());
```

Output:

```
02
```

## Scoped GlideDateTime - getDayOfWeekLocalTime\(\)

Gets the day of the week stored by the GlideDateTime object, expressed in the user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of week value, in the user's time zone, from 1 to 7. Monday equals 1, Sunday equals 7.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");//Thursday
gs.info(gdt.getDayOfWeekLocalTime());
```

Output:

```
4
```

## Scoped GlideDateTime - getDayOfWeekUTC\(\)

Returns the day of the week stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Day of week value from 1 to 7. Monday equals 1, Sunday equals 7.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00"); //Thursday
gs.info(gdt.getDayOfWeekUTC());
```

Output:

```
4
```

## Scoped GlideDateTime - getDaysInMonthLocalTime\(\)

Gets the number of days in the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of days in the current month in the user's time zone.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00"); //December
gs.info(gdt.getDaysInMonthLocalTime());
```

Output:

```
30
```

## Scoped GlideDateTime - getDaysInMonthUTC\(\)

Gets the number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.|

```
var gdt = new GlideDateTime("2011-11-02 12:00:00"); //November
gs.info(gdt.getDaysInMonthUTC());
```

Output:

```
30
```

## Scoped GlideDateTime - getDisplayValue\(\)

Gets the date and time value in the current user's display format and time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Date and time in the user's format and time zone. Keep in mind when designing business rules or script includes that this method may return values in different formats for different users.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getDisplayValue()); //uses current user session time zone (US/Pacific)
```

Output:

```
2011-08-31 01:00:00
```

## Scoped GlideDateTime - getDisplayValueInternal\(\)

Gets the display value in the internal format \(yyyy-MM-dd HH:mm:ss\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The date and time values for the GlideDateTime object in the current user's time zone and the internal date and time format of `yyyy-MM-dd HH:mm:ss`.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00"); 
gs.info(gdt.getDisplayValueInternal()); //uses current user session time zone (US/Pacific)
```

Output:

```
2011-08-31 01:00:00
```

## Scoped GlideDateTime - getDisplayValueLang\(String style, String language\)

Returns a date and time value in the current users' locale according to a specified language and date style.

<table id="id_wvq_jww_dwb" class="parameters"><thead><tr><th>

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

Specifies the date and time format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API will default to use *medium*. Accepted values are not case sensitive.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Returns the date according to a specified language value. Accepts language tags that conform with the BCP-47 standard. For example, `fr` for French or `en-UK` for British English. For a full list of accepted values, see [BCP 47 Language Code List](https://appmakers.dev/bcp-47-language-codes-list/).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|A string representation of the date in the style specified and in the appropriate format for the locale of the current user.|

The following example returns the date and time of the user's locale in all language and date styles.

```
var gdt = new GlideDateTime(); // This will fetch the current date


gs.info('date: ' + gdt.getDisplayValue());

gs.info('date: ' + gdt.getDisplayValueLang("full", "fr"));
gs.info('date: ' + gdt.getDisplayValueLang("long", "en-GB"));
gs.info('date: ' + gdt.getDisplayValueLang("medium", "de"));
gs.info('date: ' + gdt.getDisplayValueLang("short", "es-MX"));```
```

Output:

```
date: 2023-01-18 06:49:02
mercredi 18 janvier 2023 06:49:02
18 January 2023 06:49:02
18.01.2023 06:49:02
18/01/23 06:49:02
```

## Scoped GlideDateTime - getDSTOffset\(\)

Gets the amount of time that daylight saving time is offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Amount of time, in milliseconds, that daylight saving is offset. Returns 0 if there is no offset or if the time is not during daylight saving time.|

```
var gdt = new GlideDateTime("2014-08-31 08:00:00"); 
gs.info(gdt.getDSTOffset()); //uses current user session time zone (US/Pacific)
```

Output:

```
3600000
```

## Scoped GlideDateTime - getErrorMsg\(\)

Gets the current error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The error message.|

```
var gdt = new GlideDateTime(); 
gdt.setDisplayValue("2011-aa-01 00:00:00"); 
gs.info(gdt.getErrorMsg());
```

Output:

```
Could not parse DateTime: 2011-aa-01 00:00:00
```

## Scoped GlideDateTime - getInternalFormattedLocalTime\(\)

Returns the object's time in the local time zone and in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The object's time in the local time zone and the internal format.|

This example displays the time in the system time format of the user's timezone.

```
var gdt = new GlideDateTime('2022-10-08 01:00:00');
gs.info(gdt.getDisplayValue());
gs.info(gdt.getInternalFormattedLocalTime());
```

Output

```
2022-10-07 06:00:00 PM
18:00:00
```

## Scoped GlideDateTime - getLocalDate\(\)

Gets the date stored by the GlideDateTime object, expressed in the standard format, yyyy-MM-dd, and the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type| |
|----|---|
|GlideDate|The date in the user's time zone.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getLocalDate());
```

Output:

```
2011-08-31
```

## Scoped GlideDateTime - getLocalTime\(\)

Returns a GlideTime object that represents the time portion of the GlideDateTime object in the user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideTime|The time in the user's time zone.|

```
var gdt = new GlideDateTime("2014-08-31 08:00:00");
gt = gdt.getLocalTime();
gs.info("local time is " + gt.getByFormat('hh:mm:ss'));
```

Output:

```
local time is 01:00:00
```

## Scoped GlideDateTime - getMonthLocalTime\(\)

Gets the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month.|

```
var gdt = new GlideDateTime("2011-11-02 12:00:00"); //November
gs.info(gdt.getMonthLocalTime());
```

Output:

```
11
```

## Scoped GlideDateTime - getMonthUTC\(\)

Gets the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month.|

```
var gdt = new GlideDateTime("2011-11-02 12:00:00"); //November
gs.info(gdt.getMonthUTC());
```

Output:

```
11
```

## Scoped GlideDateTime - getNumericValue\(\)

Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of milliseconds since January 1, 1970, 00:00:00 GMT.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getNumericValue());
```

Output:

```
1314777600000
```

## Scoped GlideDateTime - getTime\(\)

Returns a GlideTime object that represents the time portion of the GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideTime|The Unix duration stamp in system format based on GMT time.|

```
var gdt = new GlideDateTime("2014-08-31 08:00:00");
gt = gdt.getTime();
gs.info(gt.getByFormat('hh:mm:ss'));
```

Output:

```
08:00:00
```

## Scoped GlideDateTime - getTZOffset\(\)

Gets the time zone offset in milliseconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of milliseconds of time zone offset.|

```
var gdt = new GlideDateTime();
gdt.getLocalTime(); // PST local time
gs.info(gdt.getTZOffset());
```

Output:

```
-25200000
```

## Scoped GlideDateTime - getUserFormattedLocalTime\(\)

Returns the object's time in the local time zone and in the user's format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The object's time in the local time zone and in the user's format.|

This example shows the object's time in the local time zone.

```
var gdt = new GlideDateTime('2022-10-08 01:00:00');
gs.info(gdt.getDisplayValue());
gs.info(gdt.getUserFormattedLocalTime());
```

Output:

```
2022-10-07 06:00:00 PM
06:00:00 PM
```

## Scoped GlideDateTime - getValue\(\)

Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time in the internal format and system time zone.Format: yyyy-MM-dd HH:mm:ss in the UTC time zone.

</td></tr></tbody>
</table>```
var gdt = new GlideDateTime("2014-08-31 08:00:00");
gs.info(gdt.getValue());
```

Output:

```
2014-08-31 08:00:00
```

## Scoped GlideDateTime - getWeekOfYearLocalTime\(\)

Gets the number of the week stored by the GlideDateTime object, expressed in the current user's time zone.

All weeks begin on Sunday. The first week of the year is the week that contains at least one day of the new year. The week beginning Sunday 2015-12-27 is considered the first week of 2016 as that week contains January 1 and 2.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of the current week. The highest week number in a year is either 52 or 53.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");//49th week, 1st week in december 
gs.info(gdt.getWeekOfYearLocalTime());
```

Output:

```
49
```

## Scoped GlideDateTime - getWeekOfYearUTC\(\)

Gets the number of the week stored by the GlideDateTime object, expressed in the UTC time zone.

All weeks begin on Sunday. The first week of the year is the week that contains at least one day of the new year. The week beginning Sunday 2015-12-27 is considered the first week of 2016 as that week contains January 1 and 2.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of the current week in UTC time. The highest week number in a year is either 52 or 53.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");//49th week, 1st week in December 
gs.info(gdt.getWeekOfYearUTC());
```

Output:

```
49
```

## Scoped GlideDateTime - getYearLocalTime\(\)

Gets the year stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|Number|Four-digit year value in the user's time zone.|

```
var gdt = new GlideDateTime("2011-11-02 12:00:00");
gs.info(gdt.getYearLocalTime());
```

Output:

```
2011
```

## Scoped GlideDateTime - getYearUTC\(\)

Gets the year stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|4-digit year value in the UTC time zone.|

```
var gdt = new GlideDateTime("2011-11-02 12:00:00"); 
gs.info(gdt.getYearUTC());
```

Output:

```
2011
```

## Scoped GlideDateTime - hasDate\(\)

Determines if an object's date is set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the object date is set; otherwise, returns false.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.hasDate());
```

Output:

```
true
```

## Scoped GlideDateTime - isDST\(\)

Determines if an object's time uses a daylight saving offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the time is daylight saving; otherwise, returns false.|

```
var gdt = new GlideDateTime("2014-08-31 00:00:00");
gs.info(gdt.isDST()); //true
```

Output:

```
var gdt = new GlideDateTime("2014-08-31 00:00:00");
gs.info(gdt.isDST()); //true
```

## Scoped GlideDateTime - isValid\(\)

Determines if a value is a valid date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if value is valid; otherwise, returns false.|

```
var gdt = new GlideDateTime("2011-aa-31 aa:00:00"); 
gs.info(gdt.isValid()); //true
gs.info(gdt.getErrorMsg()); //reason
```

Output:

```
false
Invalid date time: '2011-aa-31 aa:00:00', ignored
```

## Scoped GlideDateTime - onOrAfter\(GlideDateTime gdt\)

Determines if the GlideDateTime object's data and time occurs on or after the specified GlideDateTime object's date and time.

|Name|Type|Description|
|----|----|-----------|
|gdt|GlideDateTime|Date and time to check against.|

<table id="table_tst_nsq_yv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the GlideDateTime object's date and time is on or after the date and time specified by the parameter.Possible values:

-   true: GlideDateTime object date and time is on or after the specified object's date and time.
-   false: GlideDateTime object date and time is before the specified object's date and time.

</td></tr></tbody>
</table>```
var gdt1 = new GlideDateTime("2016-05-09 10:11:12");
var gdt2 = new GlideDateTime("2017-06-12 15:11:12");
gs.info(gdt1.onOrAfter(gdt2));   
```

Output

```
false
```

## Scoped GlideDateTime - onOrBefore\(GlideDateTime gdt\)

Determines if the GlideDateTime object's data and time occurs on or before the specified GlideDateTime object's date and time.

|Name|Type|Description|
|----|----|-----------|
|gdt|GlideDateTime|Date and time to check against.|

<table id="table_trp_2tq_yv" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the GlideDateTime object's date and time is on or before the date and time specified by the parameter.Possible values:

-   true: GlideDateTime object date and time is on or before the specified object's date and time.
-   false: GlideDateTime object date and time is after the specified object's date and time.

</td></tr></tbody>
</table>```
var gdt1 = new GlideDateTime("2016-05-09 10:11:12");
var gdt2 = new GlideDateTime("2017-06-12 15:11:12");
gs.info(gdt1.onOrBefore(gdt2));   
```

Output

```
true
```

## Scoped GlideDateTime - setDayOfMonthLocalTime\(Number day\)

Sets the day of the month to a specified value in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|day|Number|The day of month to change to, from 1 to 31. If this value is greater than the maximum number of days in the month, the value is set to the last day of the month.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setDayOfMonthLocalTime(9);
gs.info(gdt.getDayOfMonthLocalTime());
```

Output:

```
9
```

## Scoped GlideDateTime - setDayOfMonthUTC\(Number day\)

Sets the day of the month to a specified value in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|day|Number|The day of month to change to, from 1 to 31. If this value is greater than the maximum number of days in the month, the value is set to the last day of the month.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setDayOfMonthUTC(9);
gs.info(gdt.getDayOfMonthUTC());
```

Output:

```
9
```

## Scoped GlideDateTime - setDisplayValue\(String asDisplayed\)

Sets a date and time value using the current user's display format and time zone.

|Name|Type|Description|
|----|----|-----------|
|asDisplayed|String|The date and time in the current user's display format and time zone. The parameter must be formatted using the current user's preferred display format, such as MM-dd-yyyy HH:mm:ss. To assign the current date and time to a variable in a workflow script, use *variable* `.setDisplayValue(gs.nowDateTime);`.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2014-02-02 12:00:00");
gdt.setDisplayValue("2014-01-01 12:00:00");//uses current user session time zone (US/Pacific) 
gs.info(gdt.getValue());
```

Output:

```
2014-01-01 20:00:00
```

## Scoped GlideDateTime - setDisplayValue\(String value, String format\)

Sets a date and time value using the current user's time zone and the specified date and time format.

This method throws a runtime exception if the date and time format used in the **value** parameter does not match the **format** parameter. You can retrieve the error message by calling getErrorMsg\(\) on the GlideDateTime object after the exception is caught.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

value

</td><td>

String

</td><td>

Date and time in the current user's time zone.

</td></tr><tr><td>

format

</td><td>

String

</td><td>

Date and time format to use to parse the **value** parameter. Use the following values to describe the **value** parameter:

-   dd: Day of the month
-   MM: Month of the year
-   yyyy: Year
-   HH: Hour
-   mm: Minutes
-   ss: Seconds

 For example: "dd-MM-yyyy HH:mm:ss" or "MM-dd-yyyy HH:mm".

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-02-02 12:00:00");
gdt.setDisplayValue("20-5-2011 12:00:00", "dd-MM-yyyy HH:mm:ss"); //uses current user session time zone
gs.info(gdt.getValue());
```

Output

```
"20-05-2011 12:00:00"
```

## Scoped GlideDateTime - setDisplayValueInternal\(String value\)

Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|value|String|The date and time in internal format.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2014-02-02 12:00:00");
gdt.setDisplayValueInternal("2014-01-01 12:00:00"); //uses current user session time zone (US/Pacific)
gs.info(gdt.getValue());
```

Output:

```
2014-01-01 20:00:00
```

## Scoped GlideDateTime - setDisplayValueLang\(String dateTime, String style\)

Sets a date and time using a specified style and format according to the current user's locale.

<table id="id_wc2_nww_dwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dateTime

</td><td>

String

</td><td>

Date and time value for the GlideDate object in the current user's time zone. Valid values are any date and time output from the getDisplayValueLang\(\) function.For instance, using output from the getDisplayValueLang\(String style, String language\) example earlier in this topic, **November 28, 2022 07:03:41** or **28.11.2022 07:03:41** are accepted values.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Specifies the date format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API will default to use *medium*. Accepted values are not case sensitive.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Void| |

The following example returns the date and time in short and full styles.

```
var glideDateFR = new GlideDateTime();
glideDateFR.setDisplayValueLang("2/3/2023 17:27:56", "short");

gs.info('date: ' + glideDateFR.getDisplayValue());
gs.info('date: ' + glideDateFR.getDisplayValueLang("full"));
```

Output:

```
date: 2023-02-03 17:27:56
date: Friday, February 3, 2023 17:27:56
```

## Scoped GlideDateTime - setDisplayValueLang\(String dateTime, String style, String language\)

Sets a date and time using a specified style, language, and format according to the current user's locale.

<table id="id_sgm_qww_dwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dateTime

</td><td>

String

</td><td>

Date and time value for the GlideDate object in the current user's time zone. Valid values are any date and time output from the getDisplayValueLang\(\) function.For instance, using output from the getDisplayValueLang\(String style, String language\) example earlier in this topic, **November 28, 2022 07:03:41** or **28.11.2022 07:03:41** are accepted values.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Specifies the date format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API will default to use *medium*. Accepted values are not case sensitive.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Sets the language using a language tag that conforms with the BCP-47 standard. For example, `fr` for French or `en-UK` for British English. For a full list of accepted values, see [BCP 47 Language Code List](https://appmakers.dev/bcp-47-language-codes-list/).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Void| |

The following example returns the date and time in short and full styles for English and French.

```
var glideDateFR = new GlideDateTime(); 

glideDateUS.setDisplayValueLang("2/3/2023 18:00:00", "short", "en-US" );
glideDateFR.setDisplayValueLang("2/3/2023 18:00:00", "short", "fr-FR" );

gs.info('en-US date: ' + glideDateUS.getDisplayValue());
gs.info('en-US date: ' + glideDateUS.getDisplayValueLang("full"));

gs.info('fr-FR date: ' + glideDateFR.getDisplayValue());
gs.info('fr-FR date: ' + glideDateFR.getDisplayValueLang("full"));
```

Output:

```
en-US date: 2023-02-03 18:00:00
en-US date: Friday, February 3, 2023 18:00:00
fr-FR date: 2023-03-02 18:00:00
fr-FR date: Thursday, March 2, 2023 18:00:00
```

## Scoped GlideDateTime - setGlideDateTime\(GlideDateTime g\)

Sets the date and time of the current object using an existing GlideDateTime object. This method is equivalent to instantiating a new object with a GlideDateTime parameter.

|Name|Type|Description|
|----|----|-----------|
|g|GlideDateTime|The object to use for setting the datetime value.|

|Type|Description|
|----|-----------|
|None| |

```
var dt1 = new GlideDateTime("2011-01-01 12:00:00");
var dt2 = new GlideDateTime("2011-02-02 08:00:00");
dt1.setGlideDateTime(dt2);
gs.info(dt1.getValue());
```

Output:

```
2011-02-02 08:00:00
```

## Scoped GlideDateTime - setMonthLocalTime\(Number month\)

Sets the month stored by the GlideDateTime object to the specified value using the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|month|Number|The month to change to.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setMonthLocalTime(1);
gs.info(gdt.getMonthLocalTime());
```

Output:

```
1
```

## Scoped GlideDateTime - setMonthUTC\(Number month\)

Sets the month stored by the GlideDateTime object to the specified value using the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|month|Number|The month to change to.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setMonthUTC(1);
gs.info(gdt.getMonthUTC());
```

Output:

```
1
```

## Scoped GlideDateTime - setValue\(String o\)

Sets the date and time of the GlideDateTime object.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

o

</td><td>

String

</td><td>

The date and time to use. This parameter may be one of several types: -   A string in the UTC time zone and the internal format of yyyy-MM-dd HH:mm:ss. Sets the value of the object to the specified date and time. Using the method this way is equivalent to instantiating a new GlideDateTime object using the GlideDateTime\(String value\) constructor. If the date and time format used does not match the internal format, the method attempts to set the date and time using other available formats. Resolving the date and time this way can lead to inaccurate data due to ambiguity in the day and month values. When using a non-standard date and time format, use setValueUTC\(String dt, String format\) instead.
-   A GlideDateTime object. Sets the value of the object to the date and time stored by the GlideDateTime passed in the parameter. Using the method this way is equivalent to instantiating a new GlideDateTime object using the GlideDateTime\(GlideDateTime g\) constructor.
-   A JavaScript Number. Sets the value of the object using the Number value as milliseconds past January 1, 1970 00:00:00 UTC.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-01-01 12:00:00");
gdt.setValue("2011-02-02 08:00:00");  // value set =  2011-02-02 08:00:00
gs.info(gdt.getValue());
```

Output:

```
2011-02-02 08:00:00
```

## Scoped GlideDateTime - setValueUTC\(String dt, String format\)

Sets a date and time value using the UTC time zone and the specified date and time format. This method throws a runtime exception if the date and time format used in the **dt** parameter does not match the **format** parameter. You can retrieve the error message by calling `getErrorMsg()` on the GlideDateTime object after the exception is caught.

|Name|Type|Description|
|----|----|-----------|
|dt|String|The date and time to use.|
|format|String|The date and time format to use.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-01-01 12:00:00");
gdt.setValueUTC("15-02-2011 08:00:00", "dd-MM-yyyy HH:mm:ss");
gs.info(gdt.getValue());
```

Output:

```
2011-02-15 08:00:00
```

## Scoped GlideDateTime - setYearLocalTime\(Number year\)

Sets the year stored by the GlideDateTime object to the specified value using the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|year|Number|The year to change to.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setYearLocalTime(2013);
gs.info(gdt.getYearLocalTime());
```

Output:

```
2013
```

## Scoped GlideDateTime - setYearUTC\(Number year\)

Sets the year stored by the GlideDateTime object to the specified value using the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|year|Number|The year to change to.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime();
gdt.setYearUTC(2013);
gs.info(gdt.getYearUTC());
```

Output:

```
2013
```

## Scoped GlideDateTime - subtract\(GlideTime time\)

Subtracts a specified amount of time from the current GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|time|GlideTime|The time value to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
var gtime1 = new GlideTime();
gtime1.setValue("00:00:20");
gdt.subtract(gtime1);
var gtime2 = gdt.getTime();
gs.info(gtime2.getByFormat('hh:mm:ss'));
```

Output:

```
07:59:40
```

## Scoped GlideDateTime - subtract\(Number milliseconds\)

Subtracts the specified number of milliseconds from the GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|Number of milliseconds to subtract.|

|Type|Description|
|----|-----------|
|None| |

```
var gdt = new GlideDateTime("2011-12-07 08:00:00");
gdt.subtract(1000);
gs.info(gdt.getValue());
```

Output:

```
2011-12-07 07:59:59
```

## Scoped GlideDateTime - subtract\(GlideDateTime start, GlideDateTime end\)

Returns the duration difference between two specified GlideDateTime objects.

|Name|Type|Description|
|----|----|-----------|
|Start|GlideDateTime|Start date object.|
|End|GlideDateTime|End date object.|

|Type|Description|
|----|-----------|
|GlideDuration|Duration difference between the two specified dates.|

```
var gdt1 = new GlideDateTime("2011-08-28 09:00:00");
var gdt2 = new GlideDateTime("2011-08-31 08:00:00");
 
var dur = GlideDateTime.subtract(gdt1, gdt2); //the difference between gdt1 and gdt2
gs.info(dur.getDisplayValue());
```

Output:

```
2 Days 23 Hours
```

## Scoped GlideDateTime - toString\(\)

Gets the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, and the system time zone, UTC by default. This method is equivalent to getValue\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type| |
|----|---|
|String|The date and time stored by the GlideDateTime object in the system time zone and format.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.toString());
```

Output:

```
2011-08-31 08:00:00
```

