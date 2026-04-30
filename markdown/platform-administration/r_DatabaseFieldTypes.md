---
title: Database field type
description: Several field types are available in the system.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field administration, Forms, fields, and lists, Configure core features, Administer]
---

# Database field type

Several field types are available in the system.

This table shows field types and corresponding MySQL database types. Typically, it isn't necessary to perform any actions at the database level. To learn about changing a field type, see [System dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md).

|Field types|Options|Dictionary XML type|MySQL DB type|
|-----------|-------|-------------------|-------------|
|String|small|string|VARCHAR\(40\)|
|String|medium|string|VARCHAR\(100\)|
|String|large|string|MEDIUMTEXT|
|String|extralarge|string|MEDIUMTEXT|
|Decimal| |decimal|Decimal \(15,2\) older instances may have \(12,2\)|
|Integer| |integer|Integer|
|True-False| |boolean|TINYINT\(1\)|
|Date| |glide\_date|DATE|
|Date-Time| |glide\_date\_time|DATETIME|
|Time| |glide\_time|DATETIME|
|Duration| |glide\_duration|DATETIME|
|Choice| |string|VARCHAR\(40\)|
|Suggestion| |string|VARCHAR\(40\)|
|Journal| |journal|MEDIUMTEXT|
|Reference|&lt;reference table&gt;|reference|VARCHAR\(32\)|
|List| |glide\_list|MEDIUMTEXT|
|Url| |url|MEDIUMTEXT|
|Image| |user\_image|VARCHAR\(40\)|
|Due-Date| |due\_date|DATETIME|

**Note:** An example of option types is as follows:

-   A string field defined in the platform with a max length of 40 characters → VARCHAR\(40\).
-   A string field defined in the platform with a max length of x, where x = 41-255 characters, inclusive → VARCHAR\(x\) \[examples: String 42 is VARCHAR\(42\) and String 211 is VARCHAR\(211\)\].
-   A string field defined in the platform with a max length of 256 and upwards → MEDIUMTEXT.

