---
title: SMS Code Verification type for Password Reset
description: Using the Simple Message Service \(SMS\) Code Verification type, a user can verify identity with the help of any SMS-enabled device, like a cell phone that accepts text messages. When a user requests password reset, the system sends a numerical code to the device and the user then enters the code on the Password Reset Verification page.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Password Reset verifications, Configure your Password Reset process, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# SMS Code Verification type for Password Reset

Using the Simple Message Service \(SMS\) Code Verification type, a user can verify identity with the help of any SMS-enabled device, like a cell phone that accepts text messages. When a user requests password reset, the system sends a numerical code to the device and the user then enters the code on the Password Reset Verification page.

You can change the default behavior of an SMS code verification using either of the following methods:

-   Set parameter values, as shown in the table.
-   Update property settings for the Password Reset application.

**Note:** The system allows only one instance of each SMS code parameter.

<table id="table_qdh_s5b_pp"><thead><tr><th>

Parameter name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

expiry

</td><td>

Number of minutes the verification code is valid.**Data Type**: integer \(any positive integer\)

 **Default Value**: 5

</td></tr><tr><td>

complexity

</td><td>

Number of digits in the numerical verification code.**Data Type**: integer \(any positive integer\)

 **Default Value**: 6

</td></tr><tr><td>

pause\_window

</td><td>

Number of minutes before the user can request another SMS code for verification.**Data Type**: integer \(any positive integer\)

 **Default Value**: 2

</td></tr><tr><td>

max\_per\_day

</td><td>

Maximum number of codes sent for verification in one day.**Data Type**: integer \(any positive integer\)

 **Default Value**: 10

</td></tr></tbody>
</table>## User experience

For information on how users enroll for SMS verification, see [Enroll for the Password Reset program using SMS codes](../task/t_EnrollUsingSMS.md).

-   **[Use Notify to send SMS codes for enrollment and verification](../task/t_NotifyForSMSVerification.md)**  
You can configure the Password Reset application to send SMS codes for enrollment and verification using the ServiceNow Notify application \(via the Twilio SMS Messaging system\). Notify is tightly integrated with the workflow engine and business rules and delivers a highly configurable and trusted way to deliver SMS messages.

**Parent Topic:**[Password Reset verifications](c_PWRVerifications.md)

