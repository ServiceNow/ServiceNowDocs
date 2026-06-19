---
title: Time zone for email notifications
description: A system property controls the time zone that the instance uses for the date and time stamp of a message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-platform-administration/c\_SpecifyingTheTimeZone.html
release: australia
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Time zone for email notifications

A system property controls the time zone that the instance uses for the date and time stamp of a message.

The date and time stamp of a notification uses the system time zone, not the time zone of any recipient. The email property `glide.email.append.timezone` controls whether to append the time zone. If true, the system time zone of the instance is appended to any Date/Time fields in outbound email messages \(for example, 2018-07-02 04:01:14 PST\).

**Parent Topic:**[Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_CreateANotification.md)

