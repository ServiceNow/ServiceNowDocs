---
title: GlideDate - Scoped
description: The scoped GlideDate class provides methods for performing operations on GlideDate objects, such as instantiating GlideDate objects or working with GlideDate fields.Creates a GlideDate object with the current date time.Gets the date in the specified date format.Gets the day of the month stored by the GlideDate object, expressed in the UTC time zone.Gets the date and time field value in the UTC time zone.Returns the date using the current user's timezone and a specified format.Gets the date in the internal format \(yyyy-MM-dd\) and current user's timezone.Returns the date value in the user's locale according to a specified language and date style.Gets the month stored by the GlideDate object, expressed in the UTC time zone.Gets the date in the internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).Gets the year stored by the GlideDate object, expressed in the UTC time zone.Sets a date value using the current user's display format and time zone.Sets the date using a specified format.Sets a date using a specified style and format according to the current user's locale.Sets a date using a specified style, language, and format according to the current user's locale.Sets the date of the current GlideDate object in internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).Gets the duration difference between two GlideDate values.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDate- Scoped

The scoped GlideDate class provides methods for performing operations on GlideDate objects, such as instantiating GlideDate objects or working with GlideDate fields.

For guidance on date time input strings with a list of common format conflicts, refer to [Date and time format guidelines](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

See also [GlideDateTime - Scoped](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideDate - GlideDate\(\)

Creates a GlideDate object with the current date time.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
//Today's date is April 21, 2021
var gd = new GlideDate();
gs.info(gd.getValue());
```

Output:

```
2021-04-21
```

## Scoped GlideDate - getByFormat\(String format\)

Gets the date in the specified date format.

|Name|Type|Description|
|----|----|-----------|
|format|String|Desired date format using Java [SimpleDateFormat](https://docs.oracle.com/javase/10/docs/api/java/text/SimpleDateFormat.html). For example, `"dd-MM-yyyy"` to get the day, month, and year, or `"EEEE"` to get the day of the week.|

|Type|Description|
|----|-----------|
|String|Date value for the GlideDate object in the specified format.|

```
var gd = new GlideDate(); 
gd.setValue('2021-04-21');
gs.info(gd.getByFormat("dd-MM-yyyy"));
```

Output:

```
21-04-2021
```

## Scoped GlideDate - getDayOfMonthNoTZ\(\)

Gets the day of the month stored by the GlideDate object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The day of the month in the UTC time zone, from 1 to 31.|

```
//Today's date is 2016-05-13 
var gd =new GlideDate();
gs.info(gd.getDayOfMonthNoTZ());
```

Output:

```
13
```

## Scoped GlideDate - getDisplayValue\(\)

Gets the date and time field value in the UTC time zone.

See also: [getDisplayValueInternal\(\)](c_GlideDateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|String|Date value for the GlideDate object in the UTC time zone.|

```
var gd = new GlideDate(); 
gd.setValue('2025-04-21');
gs.info(gd.getDisplayValue());
```

Output:

```
2025-04-21
```

## Scoped GlideDate - getDisplayValueEx\(String style\)

Returns the date using the current user's timezone and a specified format.

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

Format to use for the date.Valid values \(case insensitive\):

-   `short`: M/D/YY or D/M/YY depending on the current user's language. For example, 1/27/26 or 27/1/26.
-   `medium`: Includes abbreviated month, day, and year. For example, Jan 27, 2026.
-   `long`: Includes month, day, and year. For example, January 27, 2026.
-   `full`: Includes day of the week, month, day, and year. For example, Tuesday, January 27, 2026.

The date is returned in the current user's language. The language determines the order of month and day in the date.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|The date in the specified format.|

This example returns the date using the current user's timezone and each formatting option.

```
var gd = new GlideDate();
gs.info(gd.getDisplayValueEx("short"));
gs.info(gd.getDisplayValueEx("medium"));
gs.info(gd.getDisplayValueEx("long"));
gs.info(gd.getDisplayValueEx("full"));
```

Output:

```
1/27/26  //short
Jan 27, 2026  //medium
January 27, 2026  //long
Tuesday, January 27, 2026  //full
```

## Scoped GlideDate - getDisplayValueInternal\(\)

Gets the date in the internal format \(yyyy-MM-dd\) and current user's timezone.

See also [Scoped GlideDate - getDisplayValueInternal\(\)](c_GlideDateScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|none| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Date value for the GlideDate object in the current user's time zone. Format: yyyy-MM-dd

</td></tr></tbody>
</table>```
var gd = new GlideDate(); 
gs.info(gd.getDisplayValueInternal());
```

Output:

```
2021-04-21
```

## Scoped GlideDate - getDisplayValueLang\(String style, String language\)

Returns the date value in the user's locale according to a specified language and date style.

<table id="id_a2q_p5w_dwb" class="parameters"><thead><tr><th>

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

Date format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API defaults to `medium`. Accepted values are not case sensitive.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

Returns the date according to a specified language value. Accepts language tags that conform with the BCP-47 standard. For example, `fr` for French or `en-UK` for British English. For a full list of accepted values, see [BCP 47 Language Code List](https://appmakers.dev/bcp-47-language-codes-list/).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Date in the style and language specified according to the locale of the current user.|

The following example returns the date of the user's locale in various languages and styles.

```
var gd = new GlideDate(); // This will fetch the current date


gs.info('date: ' + gd.getDisplayValue());

gs.info('date: ' + gd.getDisplayValueLang("full", "fr"));
gs.info('date: ' + gd.getDisplayValueLang("long", "en-GB"));
gs.info('date: ' + gd.getDisplayValueLang("medium", "de"));
gs.info('date: ' + gd.getDisplayValueLang("short", "es-MX"));
```

Output:

```

date: 2023-01-18
date: mercredi 18 janvier 2023
date: 18 January 2023
date: 18.01.2023
date: 18/01/23
```

## Scoped GlideDate - getMonthNoTZ\(\)

Gets the month stored by the GlideDate object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the month from 1 to 12.|

```
//Today's date is 2016-05-13
var gd =new GlideDate();
gs.info(gd.getMonthNoTZ());
```

Output:

```
5
```

## Scoped GlideDate - getValue\(\)

Gets the date in the internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).

|Name|Type|Description|
|----|----|-----------|
|none| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The date value for the GlideDate object in the system time zone. Format: yyyy-MM-dd

</td></tr></tbody>
</table>```
var gd = new GlideDate();
gd.setValue('2021-04-21');
gs.info(gd.getValue());
```

Output:

```
2021-04-21
```

## Scoped GlideDate - getYearNoTZ\(\)

Gets the year stored by the GlideDate object, expressed in the UTC time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The numerical value of the year.|

```
//Today's date is 2016-05-13
var gd =new GlideDate();
gs.info(gd.getYearNoTZ());
```

Output:

```
2016
```

## Scoped GlideDate - setDisplayValue\(String asDisplayed\)

Sets a date value using the current user's display format and time zone.

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

Date in the current user's display format and time zone. Format: Must be formatted using the current user's preferred display format, such as yyyy-MM-dd.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var gd = new GlideDate();
gd.setDisplayValue("2011-01-01");
gs.info(gd.getValue());
```

Output:

```
2011-01-01
```

## Scoped GlideDate - setDisplayValueEx\(String date, String style\)

Sets the date using a specified format.

<table id="table_zb5_3kc_b3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

date

</td><td>

String

</td><td>

Value to set for the date. The [getDisplayValueEx\(\)](c_GlideDateScopedAPI.md#) method returns dates in a valid format, or dates can be formatted as shown below.

-   M/D/YY or D/M/YY depending on the current user's language. For example, 1/27/26 or 27/1/26.
-   Abbreviated month, day, and year. For example, Jan 27, 2026.
-   Month, day, and year. For example, January 27, 2026.
-   Day of the week, month, day, and year. For example, Tuesday, January 27, 2026.

The current user's language determines the accepted order of month and day in the date. For example, if the current user's language is English `3/21/26` and `March 21, 2026` are valid values while `21/3/26` and ``21 March, 2026`` are not.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Format to use for the date.You must use the same format as the provided **date** value.

Valid values \(case insensitive\):

-   `short`: M/D/YY or D/M/YY depending on the current user's language. For example, 1/27/26 or 27/1/26.
-   `medium`: Abbreviated month, day, and year. For example, Jan 27, 2026.
-   `long`: Month, day, and year. For example, January 27, 2026.
-   `full`: Day of the week, month, day, and year. For example, Tuesday, January 27, 2026.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example sets the date using a specified format.

```
gd = new GlideDate();
gd.setDisplayValueEx("Jan 28, 2026", "medium");
gs.info(gd.getDisplayValueEx("full"));
```

Output:

```
Wednesday, January 28, 2026
```

## Scoped GlideDate - setDisplayValueLang\(String date, String style\)

Sets a date using a specified style and format according to the current user's locale.

<table id="id_m14_55w_dwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

date

</td><td>

String

</td><td>

Date value for the GlideDate object in the current user's time zone. Valid values are any date and time output from the getDisplayValueLang\(\) function.For instance, using output from the getDisplayValueLang\(String style, String language\) example earlier in this topic, **October 25, 2022** or **25.10.2022** are accepted values.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Date format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API defaults to `medium`. Accepted values are not case sensitive.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

The following example shows how you can set the current date of the user's locale to 'full' style using setDisplayValueLang\(\).

```
glideDate.setDisplayValueLang("2/3/2023", "short");


gs.info('date: ' + glideDate.getDisplayValue());
gs.info('date: ' + glideDate.getDisplayValueLang("full"));
```

Output:

```
date: 2023-02-03
date: Friday, February 3, 2023
```

## Scoped GlideDate - setDisplayValueLang\(String date, String style, String language\)

Sets a date using a specified style, language, and format according to the current user's locale.

<table id="id_kns_w5w_dwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

date

</td><td>

String

</td><td>

Date value for the GlideDate object in the current user's time zone. Valid values are any date and time output from the getDisplayValueLang\(\) function.For instance, using output from the getDisplayValueLang\(String style, String language\) example earlier in this topic, **October 25, 2022** or **25.10.2022** are accepted values.

</td></tr><tr><td>

style

</td><td>

String

</td><td>

Date format. Valid values:

-   full: returns the date in the format of &lt;weekday, month, day, and year&gt; according to the user's locale \(for example, Monday, October 24, 2022\).
-   long: returns the date in the format of &lt;month, day, and year&gt; according to the user's locale \(for example, October 24, 2022\).
-   medium: similar to **long** but returns the date with an abbreviated month \(for example, Oct 24, 2022\).
-   short: returns the date in the format of MM/DD/YY or DD/MM/YY according to the user's locale \(for example, 10/24/2022 or 24/10/2022\).

 If any other value is passed the API defaults to `medium`. Accepted values are not case sensitive.

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
var glideDateFR = new GlideDate(); 

glideDateUS.setDisplayValueLang("2/3/202", "short", "en-US" );
glideDateFR.setDisplayValueLang("2/3/2023", "short", "fr-FR" );

gs.info('en-US date: ' + glideDateUS.getDisplayValue());
gs.info('en-US date: ' + glideDateUS.getDisplayValueLang("full"));

gs.info('fr-FR date: ' + glideDateFR.getDisplayValue());
gs.info('fr-FR date: ' + glideDateFR.getDisplayValueLang("full"));
```

Output:

```
en-US date: 2023-02-03
en-US date: Friday, February 3, 2023
fr-FR date: 2023-03-02
fr-FR date: Thursday, March 2, 2023
```

## Scoped GlideDate - setValue\(String o\)

Sets the date of the current GlideDate object in internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).

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

Date and time to set in the current GlideDate object.Format: yyyy-MM-dd

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
var gd = new GlideDate(); 
gd.setValue('2015-01-01');
gs.info(gd.getValue());
```

Output:

```
2015-01-01
```

## Scoped GlideDate - subtract\(GlideDate start, GlideDate end\)

Gets the duration difference between two GlideDate values.

|Name|Type|Description|
|----|----|-----------|
|start|GlideDate|The start value.|
|end|GlideDate|The end value.|

|Type|Description|
|----|-----------|
|GlideDuration|The duration between the two values.|

```
var sgd1 = new GlideDate(); 
sgd1.setDisplayValue('2014-07-18'); 
var sgd2 = new GlideDate(); 
sgd2.setDisplayValue('2014-07-19'); 
 
var duration = GlideDate.subtract(sgd1, sgd2); 
gs.info(duration.getDisplayValue());
```

Output:

```
1 Day
```

