---
title: Time worked
description: The Task \[task\] table provides a time-tracking field called Time worked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_TimeWorked.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task fields for measuring work time, Default date and time fields, Date and Date/Time fields, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Time worked

The Task \[task\] table provides a time-tracking field called **Time worked**.

\[Omitted image "TimeTimeworked.png"\] Alt text:

This field measures how long a record has been viewed to track work time on a ticket. Any table that extends Task can use this field. To add the field, configure the form.

As the record is viewed, the timer counts upward. To pause the timer, click the stop icon \(\[Omitted image "TimerStop.png"\] Alt text: Stop icon\).

To resume the timer, click the start icon \(\[Omitted image "TimerStart.png"\] Alt text: Start icon\).

When you save a task, the amount of new time in the timer is used to generate a record on the Time Worked \[task\_time\_worked\] table. You can view this table as a related list on the task form.

By default, the time in the **Time worked** field is a cumulative value stored in the task record. If you modify a Time Worked record, the changes are not reflected in the task timer.

You can set the property **com.snc.time\_worked.update\_task\_timer** to enable updating of the task timer value, based on changes to the Time worked records. You do this using the **Update task timer** business rule.

You can also enable the dictionary attribute **time\_worked\_alert** so that updates to the time worked field make the form dirty. By default the attribute is set to false.

**Parent Topic:**[Task fields for measuring work time](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/c_TaskFieldsForMeasuringWorkTime.md)

