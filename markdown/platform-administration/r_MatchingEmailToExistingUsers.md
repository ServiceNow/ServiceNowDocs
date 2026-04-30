---
title: Email user matching
description: When the instance receives an email message, the system searches for an existing user record with the same email address as the sender.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [References, Inbound email, Notifications, Configure core features, Administer]
---

# Email user matching

When the instance receives an email message, the system searches for an existing user record with the same email address as the sender.

|Value of email.from Variable|Matching User ID|Email Address|Name|
|----------------------------|----------------|-------------|----|
|michael.tossi@company.com|michael.tossi@company.com|michael.tossi@company.com|Michael Tossi|
|"Michael Tossi" &lt;michael.tossi@company.com&gt;|michael.tossi@company.com|michael.tossi@company.com|Michael Tossi|
|"Tossi, Michael" &lt;michael.tossi@company.com&gt;|michael.tossi@company.com|michael.tossi@company.com|Michael Tossi|
|"Tossi" &lt;mtossi@company.com&gt;|mtossi@company.com|mtossi@company.com|Tossi|

**Note:** This functionality requires that you activate the Email Automatic User Creation plugin.

Inbound Email Action scripts no longer support the `gs.createUser()` method. Use either the automatically-generated email variables or the `gs.GetUserID()` method instead.

**Parent Topic:**[References for Inbound email](../concept/references-inbound-email.md)

