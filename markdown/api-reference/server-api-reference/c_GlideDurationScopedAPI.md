---
title: GlideDuration - Scoped
description: The GlideDuration class provides methods for working with spans of time known as durations.Instantiates a GlideDuration object.Instantiates a GlideDuration object by cloning the values of the passed in GlideDuration object.Instantiates a GlideDuration object with the specified duration in milliseconds.Instantiates a GlideDuration object with the specified duration display value.Adds the duration of the specified GlideDuration object to the current GlideDuration object.Returns the duration value in the specified format.Returns the number of days.Returns the display value of the duration in number of days, hours, and minutes.Returns the duration value in "d HH:mm:ss" format.Returns the rounded number of days. If the time part is more than 12 hours, the return value is rounded up. Otherwise, it is rounded down.Returns the internal date/time value of the current GlideDuration object.Sets the duration display value.Sets the internal date/time value of the GlideDuration object.Subtracts the duration of the specified GlideDuration object to the current GlideDuration object.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDuration- Scoped

The GlideDuration class provides methods for working with spans of time known as durations.

GlideDuration objects store the duration as the number of days and time from January 1, 1970, 00:00:00. As a result, the setValue\(\) and getValue\(\) methods use the scoped GlideDateTime object for parameters and return values.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDuration - GlideDuration\(\)

Instantiates a GlideDuration object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideDuration - GlideDuration\(GlideDuration another\)

Instantiates a GlideDuration object by cloning the values of the passed in GlideDuration object.

|Name|Type|Description|
|----|----|-----------|
|another|GlideDuration|GlideDuration object.|

```
var duration = new GlideDuration('3 12:00:00');
var duration2 = new GlideDuration(duration);
gs.info(duration2.getDisplayValue());
```

Output:

```
3 Days 12 Hours
```

## GlideDuration - GlideDuration\(Number milliseconds\)

Instantiates a GlideDuration object with the specified duration in milliseconds.

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

Duration value.Unit: Milliseconds

</td></tr></tbody>
</table>```
var dur = new GlideDuration(60000);
gs.info(dur.getDurationValue());
```

Output:

```
00:01:00
```

## GlideDuration - GlideDuration\(String displayValue\)

Instantiates a GlideDuration object with the specified duration display value.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

displayValue

</td><td>

String

</td><td>

Duration value.Format: d HH:mm:ss where "d" is number of days.

</td></tr></tbody>
</table>```
var duration = new GlideDuration('3 12:00:00');
var duration2 = new GlideDuration('3:00:00');
var answer = duration.add(duration2);
gs.info(answer.getDisplayValue());
```

Output:

```
3 Days 15 Hours
```

## GlideDuration - add\(GlideDuration duration\)

Adds the duration of the specified GlideDuration object to the current GlideDuration object.

|Name|Type|Description|
|----|----|-----------|
|duration|GlideDuration|GlideDuration object that contains the duration value to add to the current GlideDuration object.|

|Type|Description|
|----|-----------|
|GlideDuration|New GlideDuration object whose duration is the sum of the durations of the two GlideDuration objects.|

```
var duration = new GlideDuration('3 12:00:00');
var duration2 = new GlideDuration('3:00:00');
var answer = duration.add(duration2);
gs.info(answer.getDisplayValue());
```

Output:

```
3 Days 15 Hours
```

## GlideDuration - getByFormat\(String format\)

Returns the duration value in the specified format.

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

Duration format.Format: [Global date and time field format](https://www.servicenow.com/docs/access?context=r_FormatDateAndTimeFields&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Current duration in the specified format.|

```
var dur = new GlideDuration('3 22:00:00');
gs.info(dur.getByFormat('HH:mm'));
```

Output

```
22:00
```

## GlideDuration - getDayPart\(\)

Returns the number of days.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Number of days in the duration.|

```
var dur = new GlideDuration('3 12:00:00');
gs.info(dur.getDayPart());
```

Output:

```
3
```

## Scoped GlideDuration - getDisplayValue\(\)

Returns the display value of the duration in number of days, hours, and minutes.

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

Number of days, hours, and minutes, such as 2 Days 10 Hours 36 Minutes.Format: Display value: "n" Days "n" Hours "n" Minutes

</td></tr></tbody>
</table>```
var dur = new GlideDuration('3 12:00:00');
gs.info(dur.getDisplayValue());
```

Output:

```
3 Days 12 Hours
```

## GlideDuration - getDurationValue\(\)

Returns the duration value in "d HH:mm:ss" format.

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

Duration value. Format: d HH:mm:ss where "d" is number of days.

</td></tr></tbody>
</table>```
var dur = new GlideDuration(60000);
gs.info(dur.getDurationValue());
```

Output:

```
00:01:00
```

## GlideDuration - getRoundedDayPart\(\)

Returns the rounded number of days. If the time part is more than 12 hours, the return value is rounded up. Otherwise, it is rounded down.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Day value of the display value rounded.|

```
var dur = new GlideDuration('3 14:00:00');
gs.info(dur.getRoundedDayPart());
```

Output:

```
4
```

## GlideDuration - getValue\(\)

Returns the internal date/time value of the current GlideDuration object.

GlideDuration objects store the duration as a date and time from January 1, 1970, 00:00:00.

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

Current duration within the GlideDuration object.Format: YYYY-MM-DD HH:mm:ss

</td></tr></tbody>
</table>```
var dur = new GlideDuration('3 12:00:00');
gs.info(dur.getValue());
```

Output:

```
1970-01-04 12:00:00
```

## GlideDuration - setDisplayValue\(String asDisplayed\)

Sets the duration display value.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

asDisplayed

</td><td>

String

</td><td>

Display duration value to set.Format: d HH:mm:ss where "d" is number of days

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var dur = new GlideDuration(); 
dur.setDisplayValue('3 08:00:00');
gs.info(dur.getDisplayValue());
```

Output:

```
3 Days 8 Hours
```

## GlideDuration - setValue\(Object o\)

Sets the internal date/time value of the GlideDuration object.

The method sets the duration value to the difference of the passed in date/time the base date/time value of January 1, 1970, 00:00:00. The passed in date/time object \(string\) is parsed into a GlideDateTime object.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

o

</td><td>

Object

</td><td>

Date and time to use as the endpoint for the calculated duration time. Format: YYYY-MM-DD HH:mm:ss

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var dur = new GlideDuration();
dur.setValue('1970-01-05 08:00:00'); // sets internal DateTime value. The String is parsed into a GlideDateTime object.
gs.info(dur.getDisplayValue());
```

Output:

```
4 Days 8 Hours
```

## GlideDuration - subtract\(GlideDuration duration\)

Subtracts the duration of the specified GlideDuration object to the current GlideDuration object.

|Name|Type|Description|
|----|----|-----------|
|duration|GlideDuration|GlideDuration object that contains the duration value to subtract from the current GlideDuration object.|

|Type|Description|
|----|-----------|
|GlideDuration|New GlideDuration object whose duration contains the result of the subtraction of the duration of the two GlideDuration objects.|

```
var duration = new GlideDuration('3 12:00:00');
var duration2 = new GlideDuration('3:00:00');
var answer = duration.subtract(duration2);
gs.info(answer.getDisplayValue());
```

Output:

```
3 Days 9 Hours
```

