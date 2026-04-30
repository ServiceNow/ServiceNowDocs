---
title: GlideDate - Global
description: The GlideDate class provides methods for performing operations on GlideDate objects, such as instantiating GlideDate objects or working with GlideDate fields.Creates a GlideDate object with the current date time.Gets the date in the specified date format.Gets the day of the month stored by the GlideDate object, expressed in the UTC time zone.Gets the date and time field value in the UTC time zone.Gets the date in the internal format \(yyyy-MM-dd\) and current user's timezone.Returns the date value in the user's locale according to a specified date style.Returns the date value in the user's locale and language according to a specified date style.Gets the month stored by the GlideDate object, expressed in the UTC time zone.Gets the year stored by the GlideDate object, expressed in the UTC time zone.Parses a date to the locale associated with the passed language and country codes.Sets a date value using the current user's display format and time zone.Sets a date using a specified style and format according to the current user's locale.Sets a date using a specified style, language, and format according to the current user's locale.Sets the date of the current GlideDate object in internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDate- Global

The GlideDate class provides methods for performing operations on GlideDate objects, such as instantiating GlideDate objects or working with GlideDate fields.

For guidance on date time input strings with a list of common format conflicts, refer to [Date and time format guidelines](../../../../../script/glide-server-apis/topic/p_GlideServerAPIs.md#).

See also [GlideDateTime - Global](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDate - GlideDate\(\)

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

## GlideDate - getByFormat\(String format\)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getByFormat\(String format\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - getDayOfMonthNoTZ\(\)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getMonthNoTZ\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - getDisplayValue\(\)

Gets the date and time field value in the UTC time zone.

See also: [getDisplayValueInternal\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getDisplayValue\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - getDisplayValueInternal\(\)

Gets the date in the internal format \(yyyy-MM-dd\) and current user's timezone.

See also [getDisplayValue\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getDisplayValueInternal\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - getDisplayValueLang\(String style\)

Returns the date value in the user's locale according to a specified date style.

<table id="id_bvt_cvr_dwb" class="parameters"><thead><tr><th>

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

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|A string representation of the date in the style specified and in the appropriate format for the locale of the current user.|

The following example returns the date of the user's locale in all styles.

```
var gd = new GlideDate(); // This will fetch the current date


gs.info('date: ' + gd.getDisplayValue());

gs.info('date: ' + gd.getDisplayValueLang("full"));
gs.info('date: ' + gd.getDisplayValueLang("long"));
gs.info('date: ' + gd.getDisplayValueLang("medium"));
gs.info('date: ' + gd.getDisplayValueLang("short"));
```

Output:

```
date: 2023-01-18
Wednesday, January 18, 2023
date: January 18, 2023
date: Jan 18, 2023
date: 1/18/23
```

## GlideDate - getDisplayValueLang\(String style, String language\)

Returns the date value in the user's locale and language according to a specified date style.

<table id="id_ox5_fwr_dwb" class="parameters"><thead><tr><th>

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

## GlideDate - getMonthNoTZ\(\)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getMonthNoTZ\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - getYearNoTZ\(\)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - getYearNoTZ\(\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - parseDate\(String date, String language, String country\)

Parses a date to the locale associated with the passed language and country codes.

**Note:** This method fails and throws an exception if the regional date format isn't followed.

<table id="table_ynx_dsb_fbc" class="parameters"><thead><tr><th>

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

Date formatted in regional syntax. Formats:

-   Alphanumeric dates: You can specify months as either three characters such as Jan, Feb, or Mar, or fully spell out the month's name. Years must be four digits and days must be two digits. For example: `"31 Jan 2020"` or `"31 January 2020"`
-   Numeric dates: Days and months must be two digits. Four digits are highly preferred for years, though the method does support a two-digit year with less accuracy and a higher chance of parse failure. You must also use the regional date separator. These separators affect the parse based on the passed in **language** and **country** values. For example: "12/31/2020" for US locale and "31.12.20" for Estonia locale.

</td></tr><tr><td>

language

</td><td>

String

</td><td>

ISO-639 two-character language code.

</td></tr><tr><td>

country

</td><td>

String

</td><td>

ISO-3166 two-character country code.

</td></tr></tbody>
</table><table id="table_znx_dsb_fbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Parsed GlideDate object that you can use in calculations or insert in a record. This method throws an exception if the date failed to parse. An exception happens when the date format doesn't match the specified locale format \(passed **language** and **country** parameters\).

</td></tr></tbody>
</table>The following code example parses a date and adds four weeks to that date.

```
var date = GlideDate.parseDate("31 Dec 2020", "en", "GB");
date.addWeeksLocalTime(4);
gs.info("Project is due 4 weeks after start date, on " + date.getDisplayValue());
```

Output:

```
Project is due 4 weeks after start date, on 2021-01-28
```

## GlideDate - setDisplayValue\(String asDisplayed\)

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - setDisplayValue\(String asDisplayed\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

## GlideDate - setDisplayValueLang\(String date, String style\)

Sets a date using a specified style and format according to the current user's locale.

<table id="id_hyd_vwr_dwb" class="parameters"><thead><tr><th>

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

## GlideDate - setDisplayValueLang\(String date, String style, String language\)

Sets a date using a specified style, language, and format according to the current user's locale.

<table id="id_udx_nxr_dwb" class="parameters"><thead><tr><th>

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

## GlideDate- setValue\(String o\)

Sets the date of the current GlideDate object in internal format \(yyyy-MM-dd\) and the system time zone \(UTC by default\).

If invalid data is provided to this method, the previous value is kept.

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

### Scoped equivalent

To use this method in a scoped application, use the corresponding scoped method: [Scoped GlideDate - setValue\(String o\)](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#).

