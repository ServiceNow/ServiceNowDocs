---
title: Message logs for individual emails
description: The email log entries for an individual notification email are accessible as a related list in the email record. The Error string field in the email record can provide additional information.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email FAQs and troubleshooting, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Message logs for individual emails

The email log entries for an individual notification email are accessible as a related list in the email record. The **Error string** field in the email record can provide additional information.

Every email record contains an **Email Log** related list. This list shows the Email Log Entry \[syslog\_email\] records. For troubleshooting purposes, the most useful fields are probably **Level** and **Message**.

To diagnose problems with outbound emails, also examine the **Error string** field in the email record. However, not every receiving email server sends back an error string.

**Note:** The Email Log Entry record is available for only 7 days after the email record is created.

## Inbound actions on received emails

Check these logs as the first step to diagnose issues with inbound actions. The logs show which inbound action did or did not apply and for what reason.

**Note:** If an inbound action did not update any field on the target record, the log indicates that the inbound action was skipped.

## Reasons for including or excluding recipients

For outbound notifications, the email system log provides reasons that recipients were included or excluded.

Each log entry corresponds to a reason for inclusion or exclusion. For example, all users who were excluded because they are inactive appear in a single log entry.

A series of system properties can be used to fine-tune the information to be logged. Two properties, glide.notification.recipient.include\_logging and glide.notification.recipient.exclude\_logging, control all recipient inclusion and exclusion logging. Several other [properties](../../reference-pages/reference/r_AdditionalProperties.md) allow you to tailor the information reported in the logs to meet your needs. All of the properties are enabled by default.

**Parent Topic:**[Email FAQs and troubleshooting notification emails](../concept/troubleshooting-notification-emails.md)

