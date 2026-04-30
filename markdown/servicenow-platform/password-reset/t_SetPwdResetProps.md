---
title: Configuring Password Reset properties
description: You can specify properties that configure the Password Reset experience for end users.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring Password Reset properties

You can specify properties that configure the Password Reset experience for end users.

## Before you begin

Role required: password\_reset\_admin

## About this task

While there are no range limits for the values you can enter for properties, consider using only positive integer values starting at 1. When you determine the limit for the upper range of a property, consider the task that the user is performing.

For example, you would not want to allow 100 attempts for users to verify their identity. A more common value is 3 attempts. Similarly, you may not want to force users who are completing the enrollment process to spend time selecting and answering 30 security questions. The more commonly used number of security questions is between 5 and 7.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Properties**.

    For information about the Password Reset properties, see [Password Reset global properties](../reference/password-reset-global-properties.md).

2.  Update settings as needed and then click **Save**.


**Parent Topic:**[Configure your Password Reset process](t_CreateAPasswordResetProcess.md)

**Related topics**  


[Configure password expiration reminder](password-reset-expiration-setup.md)

[Credential stores for Password Reset](../concept/c_CredentialStores.md)

[Password Reset verifications](../concept/c_PWRVerifications.md)

[Configure your Password Reset process to auto-enroll users](../../security/task/configure-auto-enroll-for-pwd-reset.md)

[Enable users to enroll for Password Reset](../../security/task/configure-user-enroll-for-pwd-reset.md)

[Send email to remind users to enroll for Password Reset](config-pwd-reset-enroll-reminder.md)

[Configure the required strength for passwords](config-pwd-strength-rqmts.md)

[Specify lockout for failed login attempts](../../security/task/t_LockoutForFailedLogins.md)

[Configure Google reCAPTCHA for the password reset process](t_ConfigureGoogleRecaptcha.md)

