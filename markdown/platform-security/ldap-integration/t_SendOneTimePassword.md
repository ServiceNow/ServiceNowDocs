---
title: Send a one-time password when the LDAP server is down
description: An LDAP property is available to send a one-time password to a user if the user is unable to log in because the LDAP server is down. You can also configure another property to control how long the password is valid.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LDAP integration troubleshooting, LDAP integration, Authentication, Access Management]
---

# Send a one-time password when the LDAP server is down

An LDAP property is available to send a one-time password to a user if the user is unable to log in because the LDAP server is down. You can also configure another property to control how long the password is valid.

## Before you begin

Role required: admin

To receive a one-time password, the user must have notifications enabled on their user profile. The notification is an email message only. SMS messages are not supported.

## About this task

Both properties are enabled by default. The default value for property that controls password validity is 10 minutes.

## Procedure

1.  Open the list of system properties by entering `sys_properties.list` in the filter of the application navigator.

2.  Find the **glide.ldap.onetime.password.enabled** property.

3.  Set the property to `true`.

4.  To change the password validity time for a user, set the following property to an integer number of minutes: **glide.authenticate.onetime.password.validity**.


