---
title: Configure the required strength for passwords
description: The password that a user defines must meet certain requirements — for example, it must contain at least 12 characters, it must include a numeral, and so on. You can configure the requirements as needed for your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/password-reset/config-pwd-strength-rqmts.html
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the required strength for passwords

The password that a user defines must meet certain requirements — for example, it must contain at least 12 characters, it must include a numeral, and so on. You can configure the requirements as needed for your organization.

## Before you begin

Role required: password\_reset\_admin

## About this task

The base system includes example credential stores with various password requirements. You can modify password requirements and provide users with hints for creating a password. The default requirements are:

-   At least eight characters
-   At least one uppercase and one lower case letter
-   At least one numeral

**Note:** In addition to configuring password strength requirements, you can configure several other settings for the credential store, as described in [Configure the connection to a credential store for the Password Reset processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateACredentialStore.md).

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Credential Stores**.

2.  Select the credential store in the list and then configure the following settings:

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Password rule hint

</td><td>

Specify the text that appears on the password reset page to help the user to create a password that meets all requirements. The **Password rule** script enforces the requirements.**Note:** The Password Reset Windows Application supports newline characters in the hint. Other formatting is not supported \(bold, underline, hyperlink, and so on\).

</td></tr><tr><td>

Password rule

</td><td>

Specify the client script that validates the new password that the user enters. The script is invoked when the user enters a new password and clicks **Password Reset**. You can use the script to enforce password strength/complexity requirements.

</td></tr><tr><td>

Enable Password Strength

</td><td>

Select the check box to:-   Display the text box for the **Strength rule** script so you can update the script.
-   Display the graphical **Password Strength** bar to the user while the user changes or resets the password.
 **Note:** The Password Reset Windows Application does not support Password Strength.

</td></tr><tr><td>

Strength rule

</td><td>

This text box appears only if you select **Enable Password Strength**.Specify the client script that calculates the strength/complexity of the password that the user enters. The script is invoked when the user begins to enter a new password during the reset process.

Default settings:-   Selected for local ServiceNow credential stores
-   Not selected for other credential stores
 **Note:**

-   To guide the user during the reset process, the system displays a graphical bar labeled **Password Strength** under the **New password** field.

\[Omitted image "password-strength.png"\] Alt text: Password strength indicator

-   The Password Reset Windows Application does not support Password Strength.


</td></tr></tbody>
</table>3.  Click **Submit**.

    You should test the connection to a credential store after you configure a new credential store or when users experience problems that might involve the connection.

4.  Navigate to **Password Reset** &gt; **Credential Stores** and then open the credential store.

5.  In the header bar, click **Save and Test Connection**.

    A progress page displays the result of the test.


**Parent Topic:**[Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md)

**Related topics**  


[Calculating the security score for password reset process]()

[Configure password expiration reminder]()

[Credential stores for Password Reset]()

[Password Reset verifications]()

[Configure your Password Reset process to auto-enroll users]()

[Enable users to enroll for Password Reset]()

[Configure Password Reset properties]()

[Send email to remind users to enroll for Password Reset]()

[Specify lockout for failed login attempts]()

[Configure Google reCAPTCHA for the password reset process]()

