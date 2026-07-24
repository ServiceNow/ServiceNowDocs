---
title: Configure your Password Reset process to auto-enroll users
description: To simplify management, many organizations auto-enroll users in the Password Reset program. Every base-system verification type enables you to specify automatic enrollment for your process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/configure-auto-enroll-for-pwd-reset.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure your Password Reset process to auto-enroll users

To simplify management, many organizations auto-enroll users in the Password Reset program. Every base-system verification type enables you to specify automatic enrollment for your process.

## Before you begin

Role required: password\_reset\_admin

## About this task

To enable automatic enrollment, you configure settings for the verification type that your Password Reset process is based on.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Extensions** &gt; **Verification Types**.

2.  Click the verification type for the verification that your Password Reset process uses.

    The verification type for each base-system verification is identified in [Password Reset verifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/c_PWRVerifications.md).

3.  On the **Verification Types** page, specify the following settings:

<table id="table_p5w_mgz_h1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enrollment check

</td><td>

Script that determines whether a user is enrolled for verification. **Note:** For automatic enrollment to work, the **Enrollment check** script must return true. This may require additional setup by the admin to ensure that the preconditions are met. For example, for the **SMS Code** verification type, records must be populated in particular tables.

 If no script is specified when **Automatic Enrollment** is selected, a default script is provided.

</td></tr><tr><td>

Automatic enrollment

</td><td>

Select the check box to auto-enroll users. **Note:** If **Automatic enrollment** is not selected, then you must provide an enrollment UI macro and enrollment processor script as described in [Create a custom Password Reset verification type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/create-verification-type.md).

</td></tr></tbody>
</table>4.  Repeat the procedure for all verifications that your Password Reset process uses.


**Parent Topic:**[Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process]()

[Configure password expiration reminder]()

[Credential stores for Password Reset]()

[Password Reset verifications]()

[Enable users to enroll for Password Reset]()

[Configure Password Reset properties]()

[Send email to remind users to enroll for Password Reset]()

[Configure the required strength for passwords]()

[Specify lockout for failed login attempts]()

[Configure Google reCAPTCHA for the password reset process]()

