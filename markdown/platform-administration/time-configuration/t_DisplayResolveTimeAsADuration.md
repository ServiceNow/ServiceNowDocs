---
title: Display resolve time as a duration
description: You can display the resolve time as a human-readable duration rather than an integer representing a duration in seconds.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resolve time, Task fields for measuring work time, Default date and time fields, Date and Date/Time fields, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display resolve time as a duration

You can display the resolve time as a human-readable duration rather than an integer representing a duration in seconds.

## Procedure

1.  From the Incident or Request form, right-click the form header and click **Configure** &gt; **Table**.

2.  From the **Columns** embedded list, click **Resolve time**.

3.  From the **Attributes** related list, click **New**.

4.  Enter these values.

    |Field|Value|
    |-----|-----|
    |Attribute|Format|
    |Dictionary entry|Resolve time|
    |Value|glide\_duration|

5.  Click **Submit**.

    The resolve time appears in forms and lists as a duration, expressed in days, hours, and minutes.

    **Note:** This attribute does not change the field data format, which remains an integer representing a duration in seconds. In reports and data exports, it still appears as the actual number of seconds, rather than as a duration.


**Parent Topic:**[Resolve time](../concept/c_ResolveTime.md)

