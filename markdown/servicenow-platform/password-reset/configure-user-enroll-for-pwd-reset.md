---
title: Enable users to enroll for Password Reset
description: To enable users to enroll for the Password Reset program, you specify a UI macro that takes the user through the enrollment process and a script that processes the enrollment data that the user entered. The base system includes a functioning macro and script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/configure-user-enroll-for-pwd-reset.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable users to enroll for Password Reset

To enable users to enroll for the Password Reset program, you specify a UI macro that takes the user through the enrollment process and a script that processes the enrollment data that the user entered. The base system includes a functioning macro and script.

## Before you begin

Role required: password\_reset\_admin

## About this task

To enable users to enroll, you configure settings for the verification type that your Password Reset process is based on.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Verification Types**.

2.  Click the verification type for the verification that your Password Reset process uses.

    The verification type for each base-system verification is identified in [Password Reset verifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/c_PWRVerifications.md).

3.  On the **Verification Types** page, specify the following settings:

    |Field|Description|
    |-----|-----------|
    |Automatic enrollment|Clear the check box to disable automatic enrollment.|
    |Enrollment UI|Enrollment UI macro that takes the user through the enrollment process.|
    |Enrollment processor|Enrollment processor script that processes enrollment data.|

4.  Repeat the procedure for all verifications that your Password Reset process uses.


## Enabling user enrollment

This example verification type uses the pwd\_enroll\_sms\_ui enrollment UI macro and the PwdEnrollSMSProcessor enrollment processor script.

\[Omitted image "VerificationTypeExample.png"\] Alt text: Verification type

A verification type must also define a verification UI macro and a corresponding verification processor script. The example uses the pwd\_verify\_sms\_uiverification UI macro and the PwdVerifySMSProcessor verification processor script.

\[Omitted image "VerificationTypeSMSUIMacro.png"\] Alt text: UI macro

\[Omitted image "VerificationTypeSMSProcessor.png"\] Alt text: Verification processor

**Parent Topic:**[Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process]()

[Configure password expiration reminder]()

[Credential stores for Password Reset]()

[Password Reset verifications]()

[Configure your Password Reset process to auto-enroll users]()

[Configure Password Reset properties]()

[Send email to remind users to enroll for Password Reset]()

[Configure the required strength for passwords]()

[Specify lockout for failed login attempts]()

[Configure Google reCAPTCHA for the password reset process]()

