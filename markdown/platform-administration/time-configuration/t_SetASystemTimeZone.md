---
title: Set a system time zone
description: Set your system time zone with a system property.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set a system time zone

Set your system time zone with a system property.

## Before you begin

Role required: admin

## About this task

The ServiceNow AI Platform stores time values in Universal Coordinated Time. Times appear globally based on the [system time zone](t_SetASystemTimeZone.md) \(glide.sys.default.tz\), or if specified, based on [user settings](../../users-and-groups/task/t_CreateAUser.md).

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System**.

2.  Locate the property **System timezone for all users unless overridden in the user's record** \[glide.sys.default.tz\].

    By default, the field is empty. If you have not defined a time zone for this property, America/Los Angeles is the default.

    For more information on setting the default time, see [Configure Next Experience language and region preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-language-preferences.md).

3.  Add a time zone in the format Country/City or using the name of a time zone \(for example, GMT\) and select **Save**.

    For available values, see [Time zone representation](https://support.servicenow.com/kb_view.do?sysparm_article=KB0594661).

    The new system time zone automatically cascades to all users who don’t already have a specified time zone. If a user selects a different time zone, or if the administrator selects a different time zone for them, the selected time zone is assigned to the user. The system time zone isn’t used.


**Parent Topic:**[Using time configuration](../using-time-configuration.md)

