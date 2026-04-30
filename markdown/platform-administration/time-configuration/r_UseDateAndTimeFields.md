---
title: Date and Date/Time fields
description: Records in the ServiceNow AI Platform store date and time values in several different types of fields. These values are stored as integer numbers, in milliseconds, and appear in the appropriate date or date/time format.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Date and Date/Time fields

Records in the ServiceNow AI Platform store date and time values in several different types of fields. These values are stored as integer numbers, in milliseconds, and appear in the appropriate date or date/time format.

## Date and Date/Time field types

The ServiceNow AI Platform stores date and date/time information in records using the following field types:

|Field type|Dictionary XML type|MySQL DB type|
|----------|-------------------|-------------|
|Date|**glide\_date**|DATE|
|Date/Time|**glide\_date\_time**|DATETIME|
|Time|**glide\_time**|DATETIME|
|Duration|**glide\_duration**|DATETIME|
|Due date|**due\_date**|DATETIME|

For the full listing of field types, see [Introduction to Fields](../../reference-pages/concept/c_IntroductionToFields.md).

-   **[Global date and time field format](r_FormatDateAndTimeFields.md)**  
You define default date and time formats globally using system properties.
-   **[Configure the date picker for the list editor](../task/t_ConfigureDatePickerForListEditor.md)**  
A system property enables you to choose between two date picker configurations for the list editor.
-   **[Default date and time fields](../concept/c_DefaultDateAndTimeFields.md)**  
Certain time fields are provided by default to store particular date and time fields.
-   **[Export date and time formats](../concept/c_ExportDateAndTimeInformation.md)**  
Because some export formats are intended for human consumption and others for database usage, various methods are used to provide date and time field information in different formats.

**Parent Topic:**[Exploring time configuration](../exploring-time-configuration.md)

