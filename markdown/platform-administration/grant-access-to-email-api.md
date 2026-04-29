---
title: Grant access to the Email API
description: To grant non-admin users access to the Email API, administrators must create an access control and assign a special role.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Grant access to the Email API

To grant non-admin users access to the Email API, administrators must create an access control and assign a special role.

## Before you begin

Role required: admin

## About this task

For additional details, see [Email API](https://www.servicenow.com/docs/access?context=email-api&version=australia&pubname=australia-api-reference&ft:locale=en-US) .

## Procedure

1.  Elevate privileges to security\_admin.

2.  Navigate to **System Security** &gt; **Access Control \(ACL\)**.

3.  Click **New**.

4.  Create an access control for the Email \[sys\_email\] table.

    |Field|Value|
    |-----|-----|
    |Type|record|
    |Operation|create|
    |Admin overrides|Selected|
    |Name|sys\_email|
    |Requires role|email\_api\_send|

5.  Assign the email\_api\_send role to the non-admin user.

6.  Verify the non-admin user either has read access to all records in the notification target table or has read access to a specific record in the table.

    For example, to work with incident notifications the non-admin user needs access to the Incident table. You can provide record access by:

    -   Granting the user an appropriate role, such as the itil role.
    -   Selecting a specific incident that was opened on behalf of the user.

