---
title: Time zones
description: All times are stored in Coordinated Universal Time \(UTC\) and appear globally based on the system time zone. However, times appear to users in their local time zone, according to their user preference settings.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Time zones

All times are stored in Coordinated Universal Time \(UTC\) and appear globally based on the system time zone. However, times appear to users in their local time zone, according to their user preference settings.

## Time zone representation

Time zones that have the Country/City format are primary time zone IDs. Other time zone IDs are links to the primary time zone.

-   For example, US/Pacific is a link to the America/Los\_Angeles time zone. Both America/Los\_Angeles and US/Pacific represent Pacific Standard Time with the same zone offset and Daylight Savings Time \(DST\) schedule.
-   Other than the representation, there is no impact on date and time functionality.

In the absence of a default time zone for the user or the system, JVM reads default time zone information from the server.

-   Depending on how the server is configured, it might return the Country/City or link, for example, US/Pacific or America/Los\_Angeles.
-   Administrators should configure their system with a default time zone `glide.sys.default.tz` to avoid system dependencies. For more information, see [Time zone representation](https://support.servicenow.com/kb_view.do?sysparm_article=KB0594661).

## Daylight Saving Time

In general, if you specify a time zone based on location \(for example, **America/Los Angeles**\), the system automatically adjusts for daylight saving time.

-   If you specify a time zone based on the time zone name \(for example, **GMT**\), which is discouraged, it does not typically adjust for daylight saving time. There are however exceptions to these guidelines.
-   For more detailed information on how daylight saving time is handled in Java, see [https://www.iana.org/time-zones](https://www.iana.org/time-zones) and [https://en.wikipedia.org/wiki/Tz\_database](https://en.wikipedia.org/wiki/Tz_database).

## User preferences

Once the System Time Zone is defined, users can also select their own time zone from their user form, accessed through **Self-Service** &gt; **My Profile**.

**Note:**

The System default appears as **System \(\[name of the default time zone\]\)**. For example, if the System time zone is **America/Los\_Angeles**, the user sees **System \(America/Los Angeles\)**.

## Java time zone class

The ServiceNow AI Platform supports all Java time zone class time zones. To view a listing of these time zones:

1.  In the **Type filter text** field, enter `sys_user.list`.
2.  Open one of the user records in the listing.
3.  Right-click the **time zone** field and select **Show Choices**.

    The resulting list is a complete listing of available time zone IDs.


## Time zones in email notifications

The date and time stamp of a notification uses the **system time zone** and not the time zone of any recipient.

**Note:**

The **glide.email.append.timezone** property in **System Properties** &gt; **Email** controls whether to append the time zone. If set to true, the system time zone of the instance is appended to any dates or date/times in outbound email messages \(for example, 2010-07-02 04:01:14 PST\).

## Time zones in service level agreements

Service level agreements have different options for which time zone to use. To set a time-zone for SLAs, navigate to the SLA definition and locate the **Timezone source** field, and select an option.

Some special considerations:

-   If you select the time zone for the caller, unpredictable behavior can occur if the caller does not have a time zone defined.
-   If you select the time zone for the SLA definition, you must manual specify the time zone on the form for the SLA.

## Time zone in scripting

When you create scripting on the server, the script uses several GlideSystem date and time functions to obtain time values. For more information about specific methods and to learn the format in which each returns the requested time, see the [GlideSystem API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideSystemScopedAPI.md).

## Enhancements

DST enhancement requires that reports and queries observe Daylight Saving Time rules. Changes affect trend charts, line charts, and filters using the "trend on" operation.

## Time zone changer

The time zone changer is active by default. Users can change their time zone for the current session in the system settings \(the gear on the top right of the banner\). At the next login, the time zone setting reverts to the system default, or user profile setting for time zone.

**Parent Topic:**[Time configuration references](../reference-time-configuration.md)

**Related topics**  


[Set a system time zone](../task/t_SetASystemTimeZone.md)

[Change the time zone choice list](../task/t_ChangeTheTimeZoneChoiceList.md)

[Change a time zone in a scheduled report](../task/t_ChangeATimeZoneInASchedReport.md)

[Change a time zone in a scheduled data import](../task/t_ChangeTimeZoneInScheduledImport.md)

