---
title: Global date and time field format
description: You define default date and time formats globally using system properties.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Date and Date/Time fields, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Global date and time field format

You define default date and time formats globally using system properties.

## Date format

The **glide.sys.date\_format** property defines the date format. An administrator can modify the property by navigating to **System Properties** &gt; **System**. The default format is: yyyy-MM-dd.

**Note:** A user can override the global date or time format with a personal preference.

Modifying the **glide.sys.date\_format** property changes the date or time format globally. When modifying the standard date format, also verify the format using a [Validate date and time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ValidateDateAndTime.md) script. You can use the same pattern strings as the [java.text.SimpleDateFormat](https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html) class, with the following exception:

-   You cannot append the 'z' character to include the time zone when adding it to a script.
-   If the resulting time zone is not three characters, an Invalid Date appears error appears when you validate the script, because the Date/Time Validation Script \(sys\_script\_validator\) fails. This failure occurs even though the script debugger shows that the content of the value meets the requirement of 'g\_user\_date\_time\_format'.

**MM** is months, while **mm** indicates minutes. The format string consists of the following abbreviations.

|Field|Full form|Short form|
|-----|---------|----------|
|Year|yyyy \(4 digits\)|yy \(2 digits\), y \(2 or 4 digits\)|
|Month|MMM \(name or abbr.\)|MM \(2 digits\), M \(1 or 2 digits\)|
|Day of Month|dd \(2 digits\)|d \(1 or 2 digits\)|

**Note:** It is recommended that you use a `yyyy` format-based date. For example, use `MM-dd-yyyy`, `yyyy-MM-dd`, or `dd-MM-yyyy`.

-   If your system date format is set to use the `yy` year format, the system considers dates 20 years later or 80 years earlier from the current date as a date in the past or future leading to an unexpected behavior.
-   For example, if you set the year as `51` for 2051, the system considers the year as 1951. Similarly, if you set the year as `37` for 1937, the system considers the year as 2037.

## Time format

An administrator can modify the **glide.sys.time\_format** property by navigating to **System Properties** &gt; **System**. Modifying the property changes the date or time format globally. When modifying the standard time format, also verify the format using a [Validate date and time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ValidateDateAndTime.md) script. You can use the same pattern strings as the [java.text.SimpleDateFormat](https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html) class, with the following exception: Appending 'z' to include the time zone is not supported.

The format string consists of the following abbreviations.

|Field|Full form|Short form|
|-----|---------|----------|
|Hour \(1-12\)|hh \(2 digits\)|h \(1 or 2 digits\)|
|Hour \(0-23\)|HH \(2 digits\)|H \(1 or 2 digits\)|
|Minute|mm \(2 digits\)|m \(1 or 2 digits\)|
|Second|ss \(2 digits\)|s \(1 or 2 digits\)|

Add the character `a` to the end of the time format string to indicate AM or PM. This option shows AM or PM whether you are using 12-hour time \(hh\) or 24-hour time \(HH\).

The default format is: HH:mm:ss.

**Note:** A user can override the global date or time format with a personal preference.

**Related topics**  


[Schedule entry fields](r_ScheduleEntryFields.md)

