---
title: Date and Date/Time fields
description: Records in the ServiceNow AI Platform store date and time values in several different types of fields. These values are stored as integer numbers, in milliseconds, and appear in the appropriate date or date/time format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/r\_UseDateAndTimeFields.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
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

For the full listing of field types, see [Introduction to Fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/c_IntroductionToFields.md).

-   **[Global date and time field format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_FormatDateAndTimeFields.md)**  
You define default date and time formats globally using system properties.
-   **[Configure the date picker for the list editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/t_ConfigureDatePickerForListEditor.md)**  
A system property enables you to choose between two date picker configurations for the list editor.
-   **[Default date and time fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_DefaultDateAndTimeFields.md)**  
Certain time fields are provided by default to store particular date and time fields.
-   **[Export date and time formats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_ExportDateAndTimeInformation.md)**  
Because some export formats are intended for human consumption and others for database usage, various methods are used to provide date and time field information in different formats.

**Parent Topic:**[Exploring time configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/exploring-time-configuration.md)

