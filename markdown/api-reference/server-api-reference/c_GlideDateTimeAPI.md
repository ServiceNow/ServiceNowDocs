---
title: GlideDateTime - Global
description: The GlideDateTime class provides methods for performing operations on GlideDateTime objects.Instantiates a new GlideDateTime object with the current date and time.Instantiates a new GlideDateTime object using the passed-in date and time value.Instantiates a new GlideDateTime object set to the time of a specified GlideDateTime object.Adds a specified number of milliseconds to the GlideDateTime object.Adds a GlideTime object to the current GlideDateTime object.Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.Adds a specified number of seconds to the GlideDateTime object.Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.Compares two date and time objects to determine whether one occurs before the other or if they are equivalent.Compares an object with an existing value for equality.Returns the date stored by the GlideDateTime object. Expressed in the format yyyy-MM-dd and in the system time zone, UTC by default.Gets the current day of the month in the UTC time zone.Gets the day of the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the day of the month stored by the GlideDateTime object, expressed in the UTC time zone.Retrieves the day of the week stored by the GlideDateTime object, expressed in the user's time zone.Gets the day of the week stored by the GlideDateTime object, expressed in the user's time zone.Gets the day of the week stored by the GlideDateTime object, expressed in the UTC time zone.Gets the number of days in the month stored by the GlideDateTime object, expressed in the Java Virtual Machine time zone.Gets the number of days in the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.Gets the date and time value in the current user's display format and time zone.Returns the display value in the internal format, yyyy-MM-dd HH:mm:ss. This method is useful for date/time fields, but not for date fields.Returns a date and time value in the current user's locale according to the specified date style.Returns a date and time value in the current user's locale according to a specified language and date style.Gets the amount of time that daylight saving time is offset.Gets the current error message.Returns the object's time in the local time zone and in the internal format.Returns a date and time object set to midnight of a specified day using UTC.Gets the date stored by the GlideDateTime object, expressed in the standard format, yyyy-MM-dd, and the current user's time zone.Gets the time in the user's time zone.Retrieves the month stored by the GlideDateTime object, expressed in Java Virtual Machine time zone.Gets the month stored by the GlideDateTime object, expressed in the current user's time zone.Gets the month stored by the GlideDateTime object, expressed in the UTC time zone.Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.Retrieves the amount of time elapsed since the midnight of a specified day to the current time.Gets the Unix duration stamp.Gets the time zone offset in milliseconds.Returns the object's time in local time zone in the user's format.Retrieves the time zone for the current user session.Retrieves a GlideDateTime object with the time set to midnight using the UTC time zone.Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, in the UTC time zone.Gets the number of the week stored by the GlideDateTime object, expressed in the current user's time zone.Gets the number of the week stored by the GlideDateTime object, expressed in the UTC time zone.Retrieves the year stored by the GlideDateTime object, expressed in the Java Virtual Machine time zone.Gets the year stored by the GlideDateTime object, expressed in the current user's time zone.Returns the year stored by the GlideDateTime object, expressed in the UTC time zone.Determines if an object's date is set.Determines if the object's time uses a daylight saving offsetDetermines if a value is a valid date and time.Sets the day of the month to a specified value.Sets the day of the month to a specified value in the current user's time zone.Sets the day of the month to a specified value in the UTC time zone.Sets a date and time value using the current user's display format and time zone.Sets a date and time value using the current user's time zone and the specified date and time format.Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.Sets a date using a specified style and format according to the current user's locale.Sets a date and time using a specified style, language, and format according to the current user's locale.Sets the date and time of the current object using an existing GlideDateTime object.Sets the date and time.Sets the month stored by the GlideDateTime object to a specified value using the Java Virtual Machine time zone.Sets the month stored by the GlideDateTime object to a specified value using the current user's time zone.Sets the month stored by the GlideDateTime object to a specified value using the UTC time zone.Sets the date and time to the number of milliseconds since January 1, 1970 00:00:00 GMT.Sets the time zone of the GlideDateTime object to be the specified time zone.Sets the date and time of the GlideDateTime object.Sets a date and time value using the UTC time zone and the specified date and time format.Sets the year stored by the GlideDateTime object to a specified value using the Java Virtual Machine time zone.Sets the year stored by the GlideDateTime object to a specified value using the current user's time zone.Sets the year stored by the GlideDateTime object to a specified value using the UTC time zone.Subtracts a specified amount of time.Subtracts a specified number of milliseconds from the GlideDateTime object.Returns the duration difference between two specified GlideDateTime objects.Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, and the system time zone, UTC by default.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 45
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDateTime- Global

The GlideDateTime class provides methods for performing operations on GlideDateTime objects.

Use the GlideDateTime methods to perform date-time operations, such as instantiating a GlideDateTime object, performing date-time calculations, formatting a date-time, or converting between date-time formats.

## Modify a glide\_date\_time field

When working with database columns of type glide\_date\_time in GlideDateTime methods, you must first convert the field value into a `GlideDateTime` object before performing date and time calculations. A `glide_date_time` field is represented as a GlideElement; calling Glide Element - getGlideObject\(\) returns a `GlideDateTime` object that supports date manipulation methods such as `addMonthsUTC()`. See [GlideElement - getGlideObject\(\)](../../GlideElement_global/concept/c_GlideElementAPI.md#) for more information.

For guidance on date time input strings with a list of common format conflicts, refer to [Date and time format guidelines](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDateTime - GlideDateTime\(\)

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

## GlideDateTime - GlideDateTime\(String dateTime\)

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
|dateTime|String|UTC date and time to set in the GlideDateTime object.|

This example shows how to instantiate a GlideDateTime object using a string.

```
var gdt = new GlideDateTime("2023-01-01 12:00:00");
gs.info(gdt);
```

Output:

```
2023-01-01 12:00:00
```

## GlideDateTime - GlideDateTime\(GlideDateTime gdt\)

Instantiates a new GlideDateTime object set to the time of a specified GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|gdt|GlideDateTime|Object used to set the time of the new object.|

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

## GlideDateTime - add\(Number milliseconds\)

Adds a specified number of milliseconds to the GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|The number of milliseconds to add|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getNumericValue());
gdt.add(10);
gs.print(gdt.getNumericValue());
```

Output:

```
1314777600000
1314777600010
```

### Scoped equivalent

To use the add\(\) method in a scoped application, use the corresponding scoped method: [add\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - add\(GlideTime time\)

Adds a GlideTime object to the current GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|time|[GlideTime](../../glideTimeScoped/concept/c_GlideTimeScopedAPI.md#)|GlideTime object whose time value to add to the specified GlideDateTime object.|

|Type|Description|
|----|-----------|
|void| |

This example shows how to add 20 seconds to the time set in the gdt GlideDateTime object.

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
var gtime1 = new GlideTime();
gtime1.setValue("00:00:20");
gdt.add(gtime1);
gs.print(gdt.toString());
```

Output:

```
2011-08-31 08:00:20
```

### Scoped equivalent

To use the add\(\) method in a scoped application, use the corresponding scoped method: [add\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addDays\(Number days\)

Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.

This method isn’t available in scoped applications. You can alternatively use addDaysLocalTime\(\) or addDaysUTC\(\) in scoped applications.

|Name|Type|Description|
|----|----|-----------|
|days|Number|The number of days to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addDays(-1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-30
```

## GlideDateTime - addDaysLocalTime\(Number days\)

Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.

The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|days|Number|The number of days to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addDaysLocalTime(-1);
gs.print(gdt.getLocalDate());
```

Output:

```
2011-08-30
```

### Scoped equivalent

To use the addDaysLocalTime\(\) method in a scoped application, use the corresponding scoped method: [addDaysLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addDaysUTC\(Number days\)

Adds a specified number of days to the current GlideDateTime object. A negative parameter subtracts days.

The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts days using the UTC date and time values.

|Name|Type|Description|
|----|----|-----------|
|days|Number|The number of days to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addDaysUTC(-1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-30
```

### Scoped equivalent

To use the addDaysUTC\(\) method in a scoped application, use the corresponding scoped method: [addDaysUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addSeconds\(Number seconds\)

Adds a specified number of seconds to the GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|seconds|Number|The number of seconds to add|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-12-07 08:00:00");
gdt.addSeconds(1000);
gs.print(gdt.getValue());
```

Output:

```
2011-12-07 08:16:40
```

### Scoped equivalent

To use the addSeconds\(\) method in a scoped application, use the corresponding scoped method: [addSeconds\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addWeeks\(Number weeks\)

Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.

Use addWeeksLocalTime\(\) and addWeeksUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|weeks|Number|The number of weeks to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addWeeks(-1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-24
```

## GlideDateTime - addWeeksLocalTime\(Number weeks\)

Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.

The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|weeks|Number|The number of weeks to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addWeeksLocalTime(-1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-24
```

### Scoped equivalent

To use the addWeeksLocalTime\(\) method in a scoped application, use the corresponding scoped method: [addWeeksLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addWeeksUTC\(Number weeks\)

Adds a specified number of weeks to the current GlideDateTime object. A negative parameter subtracts weeks.

The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts weeks using the UTC date and time values.

|Name|Type|Description|
|----|----|-----------|
|weeks|Number|The number of weeks to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addWeeksUTC(-1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-24
```

### Scoped equivalent

To use the addWeeksUTC\(\) method in a scoped application, use the corresponding scoped method: [addWeeksUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addMonths\(Number months\)

Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.

Use addMonthsLocalTime\(\) or addMonthsUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|months|Number|The number of months to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addMonths(2);
gs.print(gdt.getDate());
```

Output:

```
2011-10-31
```

## GlideDateTime - addMonthsLocalTime\(Number months\)

Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.

The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|months|Number|The number of months to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addMonthsLocalTime(2);
gs.print(gdt.getDate());
```

Output:

```
2011-10-31
```

### Scoped equivalent

To use the addMonthsLocalTime\(\) method in a scoped application, use the corresponding scoped method: [addMonthsLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addMonthsUTC\(Number months\)

Adds a specified number of months to the current GlideDateTime object. A negative parameter subtracts months.

The method determines the UTC date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts months using the UTC date and time values.

When working with database columns of type glide\_date\_time, you must first convert the field value into a `GlideDateTime` object before performing date and time calculations. A `glide_date_time` field is represented as a GlideElement. Calling Glide Element - getGlideObject\(\) returns a `GlideDateTime` object that supports date manipulation methods. See [GlideElement - getGlideObject\(\)](../../GlideElement_global/concept/c_GlideElementAPI.md#) for more information.

|Name|Type|Description|
|----|----|-----------|
|months|Number|The number of months to add. Use a negative number to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gdt.addMonthsUTC(2);
gs.print(gdt.getDate());
```

Output:

```
2011-10-31
```

The following example shows how to read a DateTime field from a record, add months using UTC time, and write the updated value back to the field.

```
// Add 3 months (UTC) to a glide_date_time field on the current record
var monthsToAdd = 3;

// Convert the glide_date_time field (GlideElement) to a GlideDateTime object
var gdt = current.u_renewal_date.getGlideObject();

// Add months using UTC time
gdt.addMonthsUTC(monthsToAdd);

// Store the updated value back to the field using the internal (UTC) format
current.u_renewal_date.setValue(gdt.getValue());
```

### Scoped equivalent

To use the addMonthsUTC\(\) method in a scoped application, use the corresponding scoped method: [addMonthsUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addYears\(Number years\)

Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.

Use addYearsLocalTime\(\) or addYearsUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|years|Number|The number of years to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2010-08-31 08:00:00");
gdt.addYears(1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-31
```

## GlideDateTime - addYearsLocalTime\(Number years\)

Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.

The method determines the local date and time equivalent to the value stored by the GlideDateTime object, then adds or subtracts years using the local date and time values.

|Name|Type|Description|
|----|----|-----------|
|years|Number|The number of years to add. To subtract use a negative value.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2010-08-31 08:00:00");
gdt.addYearsLocalTime(1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-31
```

### Scoped equivalent

To use the AddYearsLocalTime\(\) method in a scoped application, use the corresponding scoped method: [AddYearsLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - addYearsUTC\(Number years\)

Adds a specified number of years to the current GlideDateTime object. A negative parameter subtracts years.

The date and time value stored by GlideDateTime object is interpreted as being in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|years|Number|The number of years to add. Use a negative value to subtract.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2010-08-31 08:00:00");
gdt.addYearsUTC(1);
gs.print(gdt.getDate());
```

Output:

```
2011-08-31
```

### Scoped equivalent

To use the addYearsUTC\(\) method in a scoped application, use the corresponding scoped method: [addYearsUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - compareTo\(Object dateTime\)

Compares two date and time objects to determine whether one occurs before the other or if they are equivalent.

|Name|Type|Description|
|----|----|-----------|
|dateTime|Object|Date time in a GlideDateTime object|

<table id="table_tc3_rbd_nt" class="returns"><thead><tr><th>

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

### Scoped equivalent

To use the compareTo\(\) method in a scoped application, use the corresponding scoped method: [compareTo\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - equals\(Object GDT\)

Compares an object with an existing value for equality.

|Name|Type|Description|
|----|----|-----------|
|GDT|Object|The object to compare. Can be a GlideDateTIme object or a valid date time string.|

|Type|Description|
|----|-----------|
|Boolean|True if they are equal, false otherwise.|

```
var gdt = new GlideDateTime("2011-08-31 00:00:00");
gs.print(gdt.equals("2011-09-30 00:12:01"));
```

Output:

```
 false
```

### Scoped equivalent

To use the equals\(\) method in a scoped application, use the corresponding scoped method: [equals\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDate\(\)

Returns the date stored by the GlideDateTime object. Expressed in the format yyyy-MM-dd and in the system time zone, UTC by default.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_njv_xq2_nt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date in the system time zone.Format: yyyy-MM-dd, and in the system time zone, UTC by default.

</td></tr></tbody>
</table>```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getDate());
```

Output:

```
2011-08-31
```

### Scoped equivalent

To use the getDate\(\) method in a scoped application, use the corresponding scoped method: [getDate\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDayOfMonth\(\)

Gets the current day of the month in the UTC time zone.

Deprecated. Use getDayOfMonthLocalTime\(\) and getDayOfMonthUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the UTC time zone, from 1 to 31.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00");
gs.print(gdt.getDayOfMonth());
```

Output:

```
2
```

## GlideDateTime - getDayOfMonthLocalTime\(\)

Gets the day of the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the user's time zone, from 1 to 31.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00");
gs.print(gdt.getDayOfMonthLocalTime());
```

Output:

```
2
```

### Scoped equivalent

To use the getDayOfMonthLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getDayOfMonthLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDayOfMonthUTC\(\)

Gets the day of the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the UTC time zone, from 1 to 31.|

```
var gdt = new GlideDateTime("2011-12-02 12:00:00");
gs.print(gdt.getDayOfMonthUTC());
```

Output:

```
2
```

### Scoped equivalent

To use the getDayOfMonthUTC\(\) method in a scoped application, use the corresponding scoped method: [getDayOfMonthUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDayOfWeek\(\)

Retrieves the day of the week stored by the GlideDateTime object, expressed in the user's time zone.

Use getDayOfWeekLocalTime\(\) and getDayOfWeekUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the week value - Monday = 1, ... Sunday = 7.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");
gs.print(gdt.getDayOfWeek());
```

Output:

```
4
```

## GlideDateTime - getDayOfWeekLocalTime\(\)

Gets the day of the week stored by the GlideDateTime object, expressed in the user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the week value - Monday = 1, ... Sunday = 7|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");
gs.print(gdt.getDayOfWeekLocalTime());
```

Output:

```
4
```

### Scoped equivalent

To use the getDayOfWeekLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getDayOfWeekLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDayOfWeekUTC\(\)

Gets the day of the week stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the week value - Monday = 1, ... Sunday = 7|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");
gs.print(gdt.getDayOfWeekUTC());
```

Output:

```
4
```

### Scoped equivalent

To use the getDayOfWeekUTC\(\) method in a scoped application, use the corresponding scoped method: [getDayOfWeekUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDaysInMonth\(\)

Gets the number of days in the month stored by the GlideDateTime object, expressed in the Java Virtual Machine time zone.

Use getDaysInMonthLocalTime\(\) and getDaysInMonthUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of days in the current month in the Java Virtual Machine time zone.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getDaysInMonth());
```

Output:

```
31
```

## GlideDateTime - getDaysInMonthLocalTime\(\)

Gets the number of days in the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of days in the current month in the user's time zone.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getDaysInMonthLocalTime());
```

Output:

```
31
```

### Scoped equivalent

To use the getDaysInMonthLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getDaysInMonthLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDaysInMonthUTC\(\)

Gets the number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of days in the month stored by the GlideDateTime object, expressed in the UTC time zone.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getDaysInMonthUTC());
```

Output:

```
31
```

### Scoped equivalent

To use the getDaysInMonthUTC\(\) method in a scoped application, use the corresponding scoped method: [getDaysInMonthUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDisplayValue\(\)

Gets the date and time value in the current user's display format and time zone.

**Note:** Referring to the GlideDateTime object directly returns the date and time value in the GMT time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Date and time in the user's format and time zone. Keep in mind when designing business rules or script includes that this method may return values in different formats for different users.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getDisplayValue());
```

Output:

```
2011-08-31 01:00:00
```

### Scoped equivalent

To use the getDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [getDisplayValue\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDisplayValueInternal\(\)

Returns the display value in the internal format, yyyy-MM-dd HH:mm:ss. This method is useful for date/time fields, but not for date fields.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pcw_t1d_nt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

The date and time values for the GlideDateTime object.Format: yyyy-MM-dd HH:mm:ss in the caller's time zone.

</td></tr></tbody>
</table>```
// The passed in date and time is converted to the caller's time zone.
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getDisplayValueInternal());
```

Output:

```
2011-08-31 01:00:00
```

### Scoped equivalent

To use the getDisplayValueInternal\(\) method in a scoped application, use the corresponding scoped method: [getDisplayValueInternal\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getDisplayValueLang\(String style\)

Returns a date and time value in the current user's locale according to the specified date style.

<table id="id_zqf_hvw_dwb" class="parameters"><thead><tr><th>

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

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|A string representation of the date in the style specified and in the appropriate format for the locale of the current user.|

The following example returns the date and time of the user's locale in all date styles.

```
var gdt = new GlideDateTime(); // This will fetch the current date


gs.info('date: ' + gdt.getDisplayValue());

gs.info('date: ' + gdt.getDisplayValueLang("full"));
gs.info('date: ' + gdt.getDisplayValueLang("long"));
gs.info('date: ' + gdt.getDisplayValueLang("medium"));
gs.info('date: ' + gdt.getDisplayValueLang("short"));
```

Output:

```
date: 2023-01-18 06:49:02
date: Wednesday, January 18, 2023 06:49:02
date: January 18, 2023 06:49:02
date: Jan 18, 2023 06:49:02
date: 1/18/23 06:49:02
```

## GlideDateTime - getDisplayValueLang\(String style, String language\)

Returns a date and time value in the current user's locale according to a specified language and date style.

<table id="id_dfb_4vw_dwb" class="parameters"><thead><tr><th>

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

## GlideDateTime - getDSTOffset\(\)

Gets the amount of time that daylight saving time is offset.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Amount of time, in milliseconds, that daylight saving is offset. Returns 0 if there is no offset or if the time is not during daylight saving time.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getDSTOffset());
```

Output:

```
3600000
```

### Scoped equivalent

To use the getDSTOffset\(\) method in a scoped application, use the corresponding scoped method: [getDSTOffset\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getErrorMsg\(\)

Gets the current error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The error message|

```
var gdt = new GlideDateTime("2011-aa-31 aa:00:00"); //bad
gs.print(gdt.isValid()); //false
gs.print(gdt.getErrorMsg()); //reason
```

Output:

```
false
Could not parse DateTime: 2011-aa-31 aa:00:00
```

### Scoped equivalent

To use the getErrorMsg\(\) method in a scoped application, use the corresponding scoped method: [getErrorMsg\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getInternalFormattedLocalTime\(\)

Returns the object's time in the local time zone and in the internal format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The object's time in the local time zone and the internal format.|

This example displays the time in the system time format of the user's timezone.

```
var gdt = new GlideDateTime('2022-10-08 01:00:00');
gs.info(gdt.getDisplayValue());
gs.info(gdt.getInternalFormattedLocalTime());
```

Output:

```
2022-10-07 06:00:00 PM
18:00:00
```

### Scoped equivalent

To use the getInternalFormattedLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getInternalFormattedLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getInternalMidnight\(Number dayOfTheWeek\)

Returns a date and time object set to midnight of a specified day using UTC.

|Name|Type|Description|
|----|----|-----------|
|dayOfTheWeek|Number|The day of the week for which to return the date/time object.|

|Type|Description|
|----|-----------|
|GlideDateTime|A GlideDateTime object set to midnight.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getInternalMidnight(2));
```

Output:

```
2011-08-30 00:00:01
```

## GlideDateTime - getLocalDate\(\)

Gets the date stored by the GlideDateTime object, expressed in the standard format, yyyy-MM-dd, and the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDate|The date in the user's time zone.|

This example displays the time in the user's time format in the user's timezone.

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getLocalDate());
```

Output:

```
2011-08-31
```

### Scoped equivalent

To use the getLocalDate\(\) method in a scoped application, use the corresponding scoped method: [getLocalDate\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getLocalTime\(\)

Gets the time in the user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideTime|The time in the user's time zone.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getLocalTime());
```

Output:

```
1970-01-01 01:00:00
```

### Scoped equivalent

To use the getLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getMonth\(\)

Retrieves the month stored by the GlideDateTime object, expressed in Java Virtual Machine time zone.

Use getMonthLocalTime\(\) and getMonthUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month, Jan=1, Dec=12.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getMonth());
```

Output:

```
12
```

## GlideDateTime - getMonthLocalTime\(\)

Gets the month stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month, Jan=1, Dec=12.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getMonthLocalTime());
```

Output:

```
12
```

### Scoped equivalent

To use the getMonthLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getMonthLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getMonthUTC\(\)

Gets the month stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month, Jan=1, Dec=12.|

```
var gdt = new GlideDateTime(); //December
gs.print(gdt.getMonthUTC());
```

Output:

```
12
```

### Scoped equivalent

To use the getMonthUTC\(\) method in a scoped application, use the corresponding scoped method: [getMonthUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getNumericValue\(\)

Gets the number of milliseconds since January 1, 1970, 00:00:00 GMT.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of milliseconds since January 1, 1970, 00:00:00 GMT.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getNumericValue());
```

Output:

```
1314777600000
```

## GlideDateTime - getSpanTime\(Number dayOfWeek\)

Retrieves the amount of time elapsed since the midnight of a specified day to the current time.

|Name|Type|Description|
|----|----|-----------|
|dayOfWeek|Number|Day of week value from 1 to 7. 1 = Monday, 7=Sunday.|

|Type|Description|
|----|-----------|
|GlideTime|The amount of time elapsed since midnight of the specified day. To display the result in user-friendly terms, set the value to GlideDuration.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00"); //Wednesday
var dur = new GlideDuration();
 
var span = gdt.getSpanTime(1); //how much time since Monday 00:00:00
dur.setValue(span);
gs.print(dur.getDisplayValue());
```

Output:

```
2 Days 8 Hours
```

## GlideDateTime - getTime\(\)

Gets the Unix duration stamp.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideTime|The Unix duration stamp in system format based on GMT time.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getTime());
```

Output:

```
1970-01-01 08:00:00
```

### Scoped equivalent

To use the getTime\(\) method in a scoped application, use the corresponding scoped method: [getTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getTZOffset\(\)

Gets the time zone offset in milliseconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of milliseconds of the time zone offset|

```
var gdt = new GlideDateTime();
gdt.getLocalTime(); // PST local time
gs.print(gdt.getTZOffset());
```

Output:

```
-28800000
```

### Scoped equivalent

To use the getTZOffset\(\) method in a scoped application, use the corresponding scoped method: [getTZOffset\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getUserFormattedLocalTime\(\)

Returns the object's time in local time zone in the user's format.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The object's time in local time and the user's format.|

The following code example shows how to call this method.

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

### Scoped equivalent

To use the getUserFormattedLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getUserFormattedLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getUserTimeZone\(\)

Retrieves the time zone for the current user session.

This method is equivalent to `gs.getSession().getTimeZone()`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|TimeZone|TimeZone object for the current user.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.getUserTimeZone());
```

Output:

```
sun.util.calendar.ZoneInfo[id="America/Los_Angeles",offset=-28800000,dstSavings=3600000,useDaylight=true,transitions=185,
lastRule=java.util.SimpleTimeZone[id=America/Los_Angeles,offset=-28800000,dstSavings=3600000,useDaylight=true,startYear=0,startMode=3,
startMonth=2,startDay=8,startDayOfWeek=1,startTime=7200000,startTimeMode=0,endMode=3,endMonth=10,endDay=1,endDayOfWeek=1,
endTime=7200000,endTimeMode=0]]
```

## GlideDateTime - getUTCMidnight\(Number dayOfTheWeek\)

Retrieves a GlideDateTime object with the time set to midnight using the UTC time zone.

This method sets the date of the new GlideDateTime object as the specified day of the week within the week of the original GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|dayOfTheWeek|Number|The day of the week, from 1 to 7. Monday=1, Sunday=7. Do not enter 0 in this parameter.|

|Type|Description|
|----|-----------|
|GlideDateTime|A new GlideDateTime object, set to midnight.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00"); // Wednesday, 3rd day of the week.
gs.print(gdt.getUTCMidnight(5)); //Friday, 5th day of the week.
```

Output:

```
2011-09-02 00:00:00
```

## GlideDateTime - getValue\(\)

Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_psc_gbd_nt" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date and time in the internal format and system time zone.Format: yyyy-MM-dd HH:mm:ss in the UTC time zone.

</td></tr></tbody>
</table>```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.info(gdt.getValue());
```

Output:

```
2011-08-31 08:00:00
```

### Scoped equivalent

To use the getValue\(\) method in a scoped application, use the corresponding scoped method: [getValue\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getWeekOfYearLocalTime\(\)

Gets the number of the week stored by the GlideDateTime object, expressed in the current user's time zone.

All weeks begin on Sunday. The first week of the year is the week that contains at least one day of the new year. The week beginning Sunday 2015-12-27 is considered the first week of 2016 as that week contains January 1 and 2.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of the current week. The highest week number in a year is either 52 or 53.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");
gs.print(gdt.getWeekOfYearUTC());
```

Output:

```
49
```

### Scoped equivalent

To use the getWeekOfYearLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getWeekOfYearLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getWeekOfYearUTC\(\)

Gets the number of the week stored by the GlideDateTime object, expressed in the UTC time zone.

All weeks begin on Sunday. The first week of the year is the week that contains at least one day of the new year. The week beginning Sunday 2015-12-27 is considered the first week of 2016 as that week contains January 1 and 2.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The number of the current week in UTC time. The highest week number in a year is either 52 or 53.|

```
var gdt = new GlideDateTime("2011-12-01 12:00:00");
gs.print(gdt.getWeekOfYearUTC());
```

Output:

```
49
```

### Scoped equivalent

To use the getWeekOfYearUTC\(\) method in a scoped application, use the corresponding scoped method: [getWeekOfYearUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getYear\(\)

Retrieves the year stored by the GlideDateTime object, expressed in the Java Virtual Machine time zone.

Use getYearLocalTime\(\) and getYearUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The 4-digit year value in the Java Virtual Machine time zone.|

```
var gdt = new GlideDateTime(); //2011
gs.print(gdt.getYear());
```

Output:

```
2011
```

## GlideDateTime - getYearLocalTime\(\)

Gets the year stored by the GlideDateTime object, expressed in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The 4-digit year value in the user's time zone.|

```
var gdt = new GlideDateTime(); //2011
gs.print(gdt.getYearLocalTime());
```

Output:

```
2011
```

### Scoped equivalent

To use the getYearLocalTime\(\) method in a scoped application, use the corresponding scoped method: [getYearLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - getYearUTC\(\)

Returns the year stored by the GlideDateTime object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|number|Four-digit year value in the UTC time zone.|

```
var gdt = new GlideDateTime(); //2011
gs.info(gdt.getYearUTC());
```

Output:

```
2011
```

### Scoped equivalent

To use the getYearUTC\(\) method in a scoped application, use the corresponding scoped method: [getYearUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - hasDate\(\)

Determines if an object's date is set.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the object's date is set, false otherwise.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.hasDate());
```

Output:

```
true
```

### Scoped equivalent

To use the hasDate\(\) method in a scoped application, use the corresponding scoped method: [hasDate\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - isDST\(\)

Determines if the object's time uses a daylight saving offset

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the time is daylight saving time, false otherwise.|

```
var gdt = new GlideDateTime("2011-08-31 00:00:00");
gs.print(gdt.isDST()); //true
```

Output:

```
true
```

### Scoped equivalent

To use the isDST\(\) method in a scoped application, use the corresponding scoped method: [isDST\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - isValid\(\)

Determines if a value is a valid date and time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if value is valid, false otherwise.|

```
var gdt = new GlideDateTime("2011-aa-31 aa:00:00"); 
gs.print(gdt.isValid()); //true
gs.print(gdt.getErrorMsg()); //reason
```

Output

```
Invalid date time: '2011-aa-31 aa:00:00', ignored
```

### Scoped equivalent

To use the isValid\(\) method in a scoped application, use the corresponding scoped method: [isValid\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDayOfMonth\(Number day\)

Sets the day of the month to a specified value.

Use setDayOfMonthLocalTime\(day\) and setDayOfMonthUTC\(day\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|day|Number|Day of the month, from 1 to 31.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setDayOfMonth(9);
gs.print(gdt.getDayOfMonth());
```

Output:

```
9
```

## GlideDateTime - setDayOfMonthLocalTime\(Number day\)

Sets the day of the month to a specified value in the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|day|Number|The day of month to change to, from 1 to 31. If this value is greater than the maximum number of days in the month, the value is set to the last day of the month.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setDayOfMonthLocalTime(9);
gs.print(gdt.getDayOfMonthLocalTime());
```

Output:

```
9
```

### Scoped equivalent

To use the setDayOfMonthLocalTime\(\) method in a scoped application, use the corresponding scoped method: [setDayOfMonthLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDayOfMonthUTC\(Number day\)

Sets the day of the month to a specified value in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|day|Number|The day of month to change to, from 1 to 31. If this value is greater than the maximum number of days in the month, the value is set to the last day of the month.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setDayOfMonthUTC(9);
gs.print(gdt.getDayOfMonthUTC());
```

Output:

```
9
```

### Scoped equivalent

To use the setDayOfMonthUTC\(\) method in a scoped application, use the corresponding scoped method: [setDayOfMonthUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDisplayValue\(String asDisplayed\)

Sets a date and time value using the current user's display format and time zone.

|Name|Type|Description|
|----|----|-----------|
|asDisplayed|String|The date and time in the current user's display format and time zone. The parameter must be formatted using the current user's preferred display format, such as MM-dd-yyyy HH:mm:ss. To assign the current date and time to a variable in a workflow script, use `<variable>.setDisplayValue(gs.nowDateTime);`.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-02-02 12:00:00");
gdt.setDisplayValue("2011-01-01 12:00:00");
gs.print(gdt.getValue());
```

Output:

```
2011-01-01 20:00:00
```

### Scoped equivalent

To use the setDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [setDisplayValue\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDisplayValue\(String dateTime, String format\)

Sets a date and time value using the current user's time zone and the specified date and time format.

This method throws a runtime exception if the date and time format used in the dateTime parameter does not match the format parameter. You can retrieve the error message by calling getErrorMsg\(\) on the GlideDateTime object after the exception is caught.

|Name|Type|Description|
|----|----|-----------|
|dateTime|String|The date and time in the current user's time zone.|
|format|String|The format to use to parse the dateTime parameter.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-02-02 12:00:00");
gdt.setDisplayValue("20-5-2011 12:00:00", "dd-MM-yyyy HH:mm:ss");
gs.print(gdt.getValue());
```

Output:

```
2011-05-20 19:00:00
```

### Scoped equivalent

To use the setDisplayValue\(\) method in a scoped application, use the corresponding scoped method: [setDisplayValue\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDisplayValueInternal\(String dateTime\)

Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|dateTime|String|The date and time in internal format|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-02-02 12:00:00");
gdt.setDisplayValueInternal("2011-01-01 12:00:00");
gs.print(gdt.getValue());
```

Output:

```
2011-01-01 20:00:00
```

### Scoped equivalent

To use the setDisplayValueInternal\(\) method in a scoped application, use the corresponding scoped method: [setDisplayValueInternal\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setDisplayValueInternalWithAlternates\(String dateTime\)

Sets a date and time value using the internal format \(yyyy-MM-dd HH:mm:ss\) and the current user's time zone.

This method attempts to parse incomplete date and time values.

|Name|Type|Description|
|----|----|-----------|
|dateTime|String|The date and time in internal format.|

|Type|Description|
|----|-----------|
|void| |

## GlideDateTime - setDisplayValueLang\(String dateTime, String style\)

Sets a date using a specified style and format according to the current user's locale.

<table id="id_jjl_xvw_dwb" class="parameters"><thead><tr><th>

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

## GlideDateTime - setDisplayValueLang\(String dateTime, String style, String language\)

Sets a date and time using a specified style, language, and format according to the current user's locale.

<table id="id_zks_2ww_dwb" class="parameters"><thead><tr><th>

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

## GlideDateTime - setGlideDateTime\(GlideDateTime gDT\)

Sets the date and time of the current object using an existing GlideDateTime object.

This method is equivalent to instantiating a new object with a GlideDateTime parameter.

|Name|Type|Description|
|----|----|-----------|
|gDT|GlideDateTime|A GlideDateTime object|

|Type|Description|
|----|-----------|
|void| |

```
var dt1 = new GlideDateTime("2011-01-01 12:00:00");
var dt2 = new GlideDateTime("2011-02-02 08:00:00");
dt1.setGlideDateTime(dt2);
gs.print(dt1.getValue());
```

Output:

```
2011-02-02 08:00:00
```

### Scoped equivalent

To use the setGlideDateTime\(\) method in a scoped application, use the corresponding scoped method: [setGlideDateTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setInitialValue\(String dateTime\)

Sets the date and time.

This method is equivalent to setValue\(Object\).

|Name|Type|Description|
|----|----|-----------|
|dateTime|String|The date and time to use. Accepts either a string in the GMT time zone in the internal format, or a GlideDateTime object.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setInitialValue("2011-01-01 12:00:00");
gs.print(gdt.getValue());
```

Output:

```
2011-01-01 12:00:00
```

## GlideDateTime - setMonth\(Number month\)

Sets the month stored by the GlideDateTime object to a specified value using the Java Virtual Machine time zone.

Use setMonthLocalTime\(\) or setMonthUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|month|Number|The month to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setMonth(1);
gs.print(gdt.getMonth());
```

Output:

```
1
```

## GlideDateTime - setMonthLocalTime\(Number month\)

Sets the month stored by the GlideDateTime object to a specified value using the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|month|Number|The month to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setMonthLocalTime(1);
gs.print(gdt.getMonthLocalTime());
```

Output:

```
1
```

### Scoped equivalent

To use the setMonthLocalTime\(\) method in a scoped application, use the corresponding scoped method: [setMonthLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setMonthUTC\(Number month\)

Sets the month stored by the GlideDateTime object to a specified value using the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|month|Number|The month to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setMonthUTC(1);
gs.print(gdt.getMonthUTC());
```

Output:

```
1
```

### Scoped equivalent

To use the setMonthUTC\(\) method in a scoped application, use the corresponding scoped method: [setMonthUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setNumericValue\(Number milliseconds\)

Sets the date and time to the number of milliseconds since January 1, 1970 00:00:00 GMT.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|Number of milliseconds|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setNumericValue(1314777600000);
gs.print(gdt.getValue());
```

Output:

```
2011-08-31 08:00:00
```

## GlideDateTime - setTZ\(TimeZone timeZone\)

Sets the time zone of the GlideDateTime object to be the specified time zone.

|Name|Type|Description|
|----|----|-----------|
|timeZone|TimeZone|A time zone object|

|Type|Description|
|----|-----------|
|void| |

```
var tz = gs.getSession().getTimeZone();
var gdt = new GlideDateTime(); 
gdt.setTZ(tz);
```

## GlideDateTime - setValue\(Object dateTime\)

Sets the date and time of the GlideDateTime object.

This method is equivalent to setInitialValue\(\).

<table id="table_yfh_fpc_nt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dateTime

</td><td>

Object

</td><td>

The date and time to use. This parameter may be one of several types. -   A string in the UTC time zone and the internal format of yyyy-MM-dd HH:mm:ss: Sets the value of the object to the specified date and time. Using the method this way is equivalent to instantiating a new GlideDateTime object using the GlideDateTime\(value\) constructor. If the date and time format used does not match the internal format, the method attempts to set the date and time using other available formats. Resolving the date and time this way can lead to inaccurate data due to ambiguity in the day and month values. When using a non-standard date and time format, use setValueUTC\(dateTime, format\) instead.
-   A GlideDateTime object: Sets the value of the object to the date and time stored by the GlideDateTime passed in the parameter. Using the method this way is equivalent to instantiating a new GlideDateTime object using the GlideDateTime\(g\) constructor.
-   A Java Date object: Sets the value of the object using the value stored by the Java Date object. Using the method this way is equivalent to passing the value returned by the Java Date object getTime\(\) to the GlideDateTime setNumericValue\(\) method. This method does not accept JavaScript Date objects.
-   A JavaScript Number: Sets the value of the object using the Number value as milliseconds past January 1, 1970 00:00:00 UTC. Using the method this way is equivalent to the setNumericValue\(milliseconds\) method.
-   A Java Integer or Long: Sets the value of the object using the Integer or Long value as milliseconds past January 1, 1970 00:00:00 UTC. Using the method this way is equivalent to the setNumericValue\(milliseconds\) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Set the date and time using a string in yyyy-MM-dd HH:mm:ss format.

```
var gdt = new GlideDateTime("2011-01-01 12:00:00");
gdt.setValue("2011-02-02 08:00:00");
gs.print(gdt.getValue());
```

Output:

```
2011-02-02 08:00:00
```

Set the date and time using an existing GlideDateTime object.

```
var gdtSource = new GlideDateTime("2017-05-23 11:37:41");
var gdtDest = new GlideDateTime();
gdtDest.setValue(gdtSource);
gs.print(gdtDest.getValue());
```

Output:

```
2017-05-23 11:37:41
```

Set the date and time using a number indicating milliseconds past January 1, 1970 00:00:00 UTC.

```
var gdt = new GlideDateTime("2011-01-01 12:00:00");
gdt.setValue(1617634522375);
gs.print(gdt.getValue());
```

Output:

```
2021-04-05 14:55:22
```

### Scoped equivalent

To use the setValue\(\) method in a scoped application, use the corresponding scoped method: [setValue\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setValueUTC\(String dateTime, String format\)

Sets a date and time value using the UTC time zone and the specified date and time format.

This method throws a runtime exception if the date and time format used in the dateTime parameter does not match the format parameter. You can retrieve the error message by calling getErrorMsg\(\) on the GlideDateTime object after the exception is caught.

|Name|Type|Description|
|----|----|-----------|
|dateTime|String|The date and time to use.|
|format|String|The format to use.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-01-01 12:00:00");
gdt.setValueUTC("15-02-2011 08:00:00", "dd-MM-yyyy HH:mm:ss");
gs.print(gdt.getValue());
```

Output:

```
2011-02-15 08:00:00
```

### Scoped equivalent

To use the setValueUTC\(\) method in a scoped application, use the corresponding scoped method: [setValueUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setYear\(Number year\)

Sets the year stored by the GlideDateTime object to a specified value using the Java Virtual Machine time zone.

Use setYearLocalTime\(\) or setYearUTC\(\) instead of this method.

|Name|Type|Description|
|----|----|-----------|
|year|Number|The year to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setYear(2013);
gs.print(gdt.getYear());
```

Output:

```
2013
```

## GlideDateTime - setYearLocalTime\(Number year\)

Sets the year stored by the GlideDateTime object to a specified value using the current user's time zone.

|Name|Type|Description|
|----|----|-----------|
|year|Number|The year to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setYearLocalTime(2013);
gs.print(gdt.getYearLocalTime());
```

Output:

```
2013
```

### Scoped equivalent

To use the setYearLocalTime\(\) method in a scoped application, use the corresponding scoped method: [setYearLocalTime\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - setYearUTC\(Number year\)

Sets the year stored by the GlideDateTime object to a specified value using the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|year|Number|The year to change to.|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime();
gdt.setYearUTC(2013);
gs.print(gdt.getYearUTC());
```

Output:

```
2013
```

### Scoped equivalent

To use the setYearUTC\(\) method in a scoped application, use the corresponding scoped method: [setYearUTC\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - subtract\(GlideTime time\)

Subtracts a specified amount of time.

|Name|Type|Description|
|----|----|-----------|
|time|GlideTime|The time to subtract|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
var gtime1 = new GlideTime();
gtime1.setValue("00:00:20");
gdt.subtract(gtime1);
gs.print(gdt.getTime());
```

Output:

```
1970-01-01 07:59:40
```

### Scoped equivalent

To use the subtract\(\) method in a scoped application, use the corresponding scoped method: [subtract\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - subtract\(Number milliseconds\)

Subtracts a specified number of milliseconds from the GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|milliseconds|Number|The number of milliseconds to subtract|

|Type|Description|
|----|-----------|
|void| |

```
var gdt = new GlideDateTime("2011-12-07 08:00:00");
gdt.subtract(1000);
gs.print(gdt.getValue());
```

Output:

```
2011-12-07 07:59:59
```

### Scoped equivalent

To use the subtract\(\) method in a scoped application, use the corresponding scoped method: [subtract\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - subtract\(GlideDateTime start, GlideDateTime end\)

Returns the duration difference between two specified GlideDateTime objects.

|Name|Type|Description|
|----|----|-----------|
|start|GlideDateTime|Start date object.|
|end|GlideDateTime|End date object.|

|Type|Description|
|----|-----------|
|GlideDuration|Duration difference between the two specified dates.|

```
var gdt1 = new GlideDateTime("2011-08-28 09:00:00");
var gdt2 = new GlideDateTime("2011-08-31 08:00:00");
 
var dur = GlideDateTime.subtract(gdt1, gdt2); // Difference between gdt1 and gdt2
gs.info(dur.getDisplayValue());
```

Output:

```
2 Days 23 Hours
```

### Scoped equivalent

To use the subtract\(\) method in a scoped application, use the corresponding scoped method: [subtract\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

## GlideDateTime - toString\(\)

Returns the date and time value stored by the GlideDateTime object in the internal format, yyyy-MM-dd HH:mm:ss, and the system time zone, UTC by default.

This method is equivalent to getValue\(\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|The date and time stored by the GlideDateTime object in the system time zone and format.|

```
var gdt = new GlideDateTime("2011-08-31 08:00:00");
gs.print(gdt.toString());
```

Output:

```
2011-08-31 08:00:00
```

### Scoped equivalent

To use the toString\(\) method in a scoped application, use the corresponding scoped method: [toString\(\)](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

