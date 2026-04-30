---
title: Password Reset global properties
description: You can configure the Password Reset global properties.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset global properties

You can configure the Password Reset global properties.

<table id="table_wln_rl1_rq"><thead><tr><th>

Property Label

</th><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Password Reset Global Properties

</td></tr><tr><td>

Email template for enrollment reminder emails

</td><td>

password\_reset.enroll \_reminder.email\_template

</td><td>

The instance can send email reminders to users who are not yet enrolled in the Password Reset process.

Template to use for the email messages that remind users to enroll for the password reset process. See [Send email to remind users to enroll for Password Reset](../task/config-pwd-reset-enroll-reminder.md).

</td></tr><tr><td>

Workflow polling frequency

</td><td>

password\_reset.wf.refresh\_rate

</td><td>

Time period in milliseconds between checks on status of the Password Reset workflow.

-   Type: integer
-   Default value: 500

</td></tr><tr><td>

Workflow expiration

</td><td>

password\_reset.wf.timeout

</td><td>

Maximum wait time in milliseconds for the workflow to complete. The workflow is triggered during the password reset request when the user clicks **Submit**.-   Type: integer
-   Default value: 90000

</td></tr><tr><td>

Disable CAPTCHA validation functionality

</td><td>

password\_reset.captcha.ignore

</td><td>

Enables or disables CAPTCHA functionality.-   Type: true\|false
-   Default value: false

 The Password Reset application uses Google re-CAPTCHA as the default CAPTCHA service. To use the base system CAPTCHA, change the **password\_reset.captcha.google.enabled** system property to **false**.

 See [Configure Google reCAPTCHA](../task/t_ConfigureGoogleRecaptcha.md)

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset Request Properties

</td></tr><tr><td>

Number of unsuccessful attempts allowed to resetting/changing password

</td><td>

password\_reset.request.max\_attempt

</td><td>

Number of password reset attempts a user is allowed before they are locked out for a period determined by the value in **max\_attempt\_window**.-   Type: integer
-   Default value: 3 \(attempts\)

</td></tr><tr><td>

Number of minutes a user needs to wait for resetting/changing password after exceeding the maximum allowed unsuccessful attempts

</td><td>

password\_reset.request.max\_attempt\_window

</td><td>

Time period that users are blocked or prevented from changing their passwords after trying the maximum number of times.-   Type: integer
-   Default value: 1440 \(minutes\)

</td></tr><tr><td>

Number of minutes a user needs to wait to reset/change password after the last successful reset/change

</td><td>

password\_reset.request.success\_window

</td><td>

Time period that a user must wait after successfully resetting the password to reset the password again.-   Type: integer
-   Default value: 1440 \(minutes\)

</td></tr><tr><td>

Number of minutes a user needs to wait to start a reset request after the last successful unlock account.

</td><td>

password\_reset.request.unlock\_window

</td><td>

Time period that a user must wait after a successful unlock operation before starting a new request.-   Type: integer
-   Default value: 1440 \(minutes\)

</td></tr><tr><td>

Number of minutes before a password reset request expires

</td><td>

password\_reset.request.expiry

</td><td>

Time period during which a user must perform the Password Reset process.-   Type: integer
-   Default value: 10 \(minutes\)

</td></tr><tr><td>

Number of hours before the password reset one time token validity expires

</td><td>

glide.pwd\_reset.onetime.token.validity

</td><td>

Time period during which a user must perform the Password Reset process using the email link.-   Type: integer
-   Default value: 12 \(hours\)

 **Note:** The setting for the `glide.pwd_reset.onetime.token.validity` property takes precedence over the setting for `password_reset.request.expiry` when the **Email Password Reset URL** check box on the process record is selected.

</td></tr><tr><td>

Maximum number of times that a user can receive "Reset Password" link via email, in a span of 24 hours. The upper limit is 5.

</td><td>

password\_reset.request.max\_email

</td><td>

Maximum number of times a user can receive emails containing a link for resetting a password in a duration of 24 hours. For example, when you set the maximum number to 3, users would receive 3 emails in the duration of 24 hours. The maximum number you can set is 5.

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset Security Question Properties

</td></tr><tr><td>

Number of security questions required during the password reset request

</td><td>

password\_reset.qa.num\_reset

</td><td>

Number of security questions that are displayed on the Verify page while a user is attempting to reset the password. The user must answer all questions correctly to verify identity. The questions are selected at random and are presented in random order.

-   Type: integer
-   Default value: 3 \(questions\)
-   Possible values: Integers that are less than the number specified for the **Number of security questions required during enrollment** property \(the num\_enroll parameter\).

 **Note:** You can override this property setting for a Password Reset process by configuring the **num\_reset** parameter. See [Specify the number of required security questions](../task/t_SecurityQuestionTypeVerif.md).

</td></tr><tr><td>

Number of security questions required during enrollment

</td><td>

password\_reset.qa.num\_enroll

</td><td>

Number of questions that a user must provide answers to while enrolling for the Password Reset process.

-   Type: integer
-   Default value: 5
-   Possible values: Integers that are greater than or equal to the number specified for the **Number of security questions required during enrollment** property \(the num\_reset parameter\).

 **Note:**

-   While attempting to verify identity, if a user answers a question incorrectly, the application refreshes with a random set of the specified questions in random order. You should, therefore, require more questions than specified for the **Number of security questions required during enrollment** property \(the num\_reset parameter\).
-   You can override this property setting for a Password Reset process by configuring the **num\_enroll** parameter. See [Specify the number of required security questions](../task/t_SecurityQuestionTypeVerif.md).

</td></tr><tr><td>

Minimum length requirement for security answers

</td><td>

password\_reset.qa.ans\_min\_len

</td><td>

Minimum number of alphanumeric characters that the user must enter in the answer text box for any security question.Default value: 3 characters

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset SMS Code Properties

</td></tr><tr><td>

Maximum number of SMS codes sent for verification per day

</td><td>

password\_reset.sms.max\_per\_day

</td><td>

Maximum number of SMS codes that are sent to a user within one 24-hour period. The 24-hour period begins when a user clicks **Send Code**.

-   Type: integer
-   Default value: 10 \(per day\)

 **Note:** You can override this SMS code property by adding the **max\_per\_day** parameter in the SMS code verification.

</td></tr><tr><td>

Number of minutes before the user can attempt to send another SMS code for verification

</td><td>

password\_reset.sms.pause\_window

</td><td>

Time that must pass before another SMS code can be sent to a user.

-   Type: integer
-   Default value: 2 \(minutes\)

 **Note:** You can override this SMS code property by adding the **pause\_window** parameter in the SMS code verification.

</td></tr><tr><td>

Number of digits in the SMS code sent to the user

</td><td>

password\_reset.sms.default\_complexity

</td><td>

Number of characters required for a user to reset their password.

-   Type: integer
-   Default value: 4 \(digits\)

 You can override this SMS code property by adding the **complexity** parameter in the SMS code verification.

</td></tr><tr><td>

Number of minutes before the SMS code expires

</td><td>

password\_reset.sms.expiry

</td><td>

Time, in minutes, until the SMS code sent to the user expires.

-   Type: integer
-   Default value: 5 \(minutes\)

 **Note:** You can override this SMS code property by the **expiry** parameter in the SMS code verification.

</td></tr><tr><td>

Use Notify for SMS code notification for enrollment and verification

</td><td>

password\_reset.sms.use\_notify

</td><td>

Support for SMS channel used for notifying users for password reset enrollment and verification. If selected, the users would receive notifications through Notify.-   Type: Yes\|No
-   Default value: Yes

**Note:** To use Notify, you must activate the Notify plugin \(com.snc.notify\).

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset Soft PIN Properties

</td></tr><tr><td>

Enable Soft PIN expiration

</td><td>

password\_reset.softpin.expiration\_enabled

</td><td>

Enables or turns off Soft PIN expiration for users.

 -   Type: Yes\|No
-   Default value: Yes

 Use this property when you want to let users know that their Soft PIN is expiring. You can enable sending reminders for Soft PIN expiration.

 If the users are resetting Soft PIN using the Virtual Agent,they view the corresponding messages with the number of days when the Soft PIN is going to expire.

</td></tr><tr><td>

The number of days after which the Soft PIN expires

</td><td>

password\_reset.softpin.expiration\_day

</td><td>

Number of days after which the Soft PIN expires. For example, if you set the number to 90, the Soft PIN will expire after 90 days are completed. The minimum limit is 30 days.

 Default value: 90

</td></tr><tr><td>

Enable Soft PIN expiration reminder

</td><td>

password\_reset.softpin.expiration\_reminder\_enabled

</td><td>

Enables or turns off the Soft PIN expiration reminders. If selected, the users will not get any email notifications stating that their Soft PIN is expiring.

 -   Type: Yes\|No
-   Default value: Yes

</td></tr><tr><td>

The time at which the Soft PIN expiration reminder is sent. Format: HH:MM

</td><td>

password\_reset.softpin.expiration\_reminder\_time

</td><td>

The time at which you want the users to receive the reminders.

 You must enter the value in the HH:MM format.

 Default value is 00:00 at system time zone.

</td></tr><tr><td>

The number of days that specify when to send a reminder before the Soft PIN expires

</td><td>

password\_reset.softpin.expiration\_reminder\_warn\_days

</td><td>

Number of days that specify when to send a reminder before the Soft PIN expires. For example, if you set the value to 5, users would get the reminder 5 days before their Soft PIN expires.

 Default value: 10

</td></tr><tr><td>

The number that sets a history limit on reusing previously used Soft PINs for the enrollment. Use any value from 1 to 30

</td><td>

password\_reset.softpin.history\_limit

</td><td>

Number of previous Soft PINs which can’t be reused for the enrollment. For example,if you set the number to 3, the users won't be able to use the same Soft PIN that's used in the previous 3 Soft PINs.

 You must use the number between 1 and 30.

 Default value: 5

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset Monitoring and Reporting Properties

</td></tr><tr><td>

Time interval, in minutes, for counting blocked users

</td><td>

password\_reset.activity\_monitor.incident\_window

</td><td>

Time window to count the number of blocked users.-   Type: integer
-   Default value: 60 \(minutes\)

</td></tr><tr><td>

Number of blocked users, in the defined time interval, that triggers a system log event

</td><td>

password\_reset.activity\_monitor.incident\_threshold

</td><td>

Number of blocked \(or locked\) users, within the specified time window, that triggers a system log event.-   Type: integer
-   Default value: 10 \(blocked users\)

</td></tr><tr><td class="sub-head" colspan="3">

Password Reset Style Sheet

</td></tr><tr><td>

Style sheet to apply to end-user pages during the password reset process.

</td><td>

password\_reset.stylesheet

</td><td>

Name of a custom CSS style sheet in the Style Sheet \[content\_css\] table. You can use the default style sheet as a template for the custom style sheet. You cannot add element definitions to the style sheet.-   Type: string
-   Default value: **css\_pwd\_reset\_default**

</td></tr></tbody>
</table>**Note:** Several components in the Self Service Password Reset \(`com.snc.password_reset`\) plugin and the Password Reset \(`com.glideapp.password_reset`\) plugin control the password reset flow. The following properties affect Password Reset, but do not appear on the **Password Reset** &gt; **Properties** page:

You can add the `glide.pwd_reset.onetime.token.validity` property to the System Properties \[sys\_properties\] table to specify the number of hours that the Password Reset token should be valid. Default: 12.

**Note:** The setting for the `glide.pwd_reset.onetime.token.validity` property takes precedence over the setting for `password_reset.request.expiry` when the **Email Password Reset URL** checkbox on the process record is selected.

Properties accessible from the System Properties \[sys\_properties\] table:

-   For Password Reset on mobile devices, you can specify the URL that the user is taken to when user taps the **Forgot password?** button. See the `glide.security.password_reset.uri` property in [High Security Settings](https://www.servicenow.com/docs/access?context=c_HighSecuritySettings&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) . Default: **/$pwd\_reset.do?sysparm\_url=ss\_default**
-   If `glide.security.forgot_password.display.link` is set to **true**, displays the **Forgot Password?** link on the login page.

**Related topics**  


[Configuring Password Reset properties](../task/t_SetPwdResetProps.md)

