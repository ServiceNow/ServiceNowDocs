---
title: Export date and time formats
description: Because some export formats are intended for human consumption and others for database usage, various methods are used to provide date and time field information in different formats.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Date and Date/Time fields, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Export date and time formats

Because some export formats are intended for human consumption and others for database usage, various methods are used to provide date and time field information in different formats.

## Excel

Date, Date-Time, and Time fields are all exported as their display values, and appear in a custom format, instead of the system date format. However, duration fields, export as the value stored in the database, which is an integer value of seconds.

**Note:** If the date and time format is `hh:mm:ss` in the **glide.sys.date\_format** System Properties setting, and you export time values to Excel, they appear in 24-hour military time.

To display the exported values in standard 12-hour am/pm time formats, select the `1:30PM time` format in **Format Cells** &gt; **Time** in Excel.

## XML

All Date and Time fields export as the value stored in the database.

## PDF

All Date and Time fields \(including Duration\) export as their display value.

## CSV

All Date and Time fields export as the value stored in the database.

**Parent Topic:**[Date and Date/Time fields](../reference/r_UseDateAndTimeFields.md)

