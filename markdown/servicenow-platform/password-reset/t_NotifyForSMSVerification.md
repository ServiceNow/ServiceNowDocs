---
title: Use Notify to send SMS codes for enrollment and verification
description: You can configure the Password Reset application to send SMS codes for enrollment and verification using the ServiceNow Notify application \(via the Twilio SMS Messaging system\). Notify is tightly integrated with the workflow engine and business rules and delivers a highly configurable and trusted way to deliver SMS messages.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SMS Code Verification type for Password Reset, Password Reset verifications, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use Notify to send SMS codes for enrollment and verification

You can configure the Password Reset application to send SMS codes for enrollment and verification using the ServiceNow Notify application \(via the Twilio SMS Messaging system\). Notify is tightly integrated with the workflow engine and business rules and delivers a highly configurable and trusted way to deliver SMS messages.

## Before you begin

Role required: password\_reset\_admin

## About this task

Notify requires a separate contract with Twilio.

## Procedure

1.  Enroll for a Twilio account and telephone number at [https://www.twilio.com/](https://www.twilio.com/)

2.  Activate the **Notify** plugin.

3.  Associate the Twilio account with Notify.


## Result

No other configuration is required. Users who request password change or password reset receive SMS codes through Notify.

**Parent Topic:**[SMS Code Verification type for Password Reset](../concept/c_SMSCodeTypeVerifications.md)

**Related topics**  


[Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

