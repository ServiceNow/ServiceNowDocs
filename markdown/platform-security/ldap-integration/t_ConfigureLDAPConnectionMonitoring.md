---
title: Configure LDAP connection monitoring
description: Change or disable LDAP connection monitoring and notifications.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [LDAP integration via MID Server, LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Configure LDAP connection monitoring

Change or disable LDAP connection monitoring and notifications.

## Before you begin

Role required: admin

## About this task

The instance automatically sends an email to users configured in the LDAP Admins group when an LDAP server connection fails. This uses the email notification, which is launched by the **LDAP Connection Test**scheduled job. This email notification is enabled by default.

**Note:** The instance does not send the email notification unless there is at least one member in the LDAP Admins group. Make sure to populate this group with the users you want to receive the email.

By default, the scheduled job tests the connection every 15 minutes. To change this interval or disable monitoring:

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Open **LDAP Connection Test**.

3.  Do one of the following:

    -   Change the interval in the **Repeat Interval** field.
    -   Disable monitoring by clearing the **Active** check box.

