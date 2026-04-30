---
title: Specify the number of required security questions
description: When designing a Security Questions verification for Password Reset, you can specify the number of questions to display when users enroll. You can also specify the number to display when a user is verifying identity while resetting the password.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Password Reset verifications, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Specify the number of required security questions

When designing a Security Questions verification for Password Reset, you can specify the number of questions to display when users enroll. You can also specify the number to display when a user is verifying identity while resetting the password.

## Before you begin

Role required: password\_reset\_admin

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Verifications** and then open a verification that uses the **Security Questions Verification Type**.

2.  Configure the parameters in the **Password Reset Verification Parameters** related list.

<table id="table_ttd_pvb_pp"><thead><tr><th>

Parameter Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

num\_enroll

</td><td>

Number of questions that a user must provide answers to while enrolling for the Password Reset process.

 The value that you specify here overrides the setting of the **Number of security questions required during enrollment** property. See [Configure Password Reset properties](t_SetPwdResetProps.md).

 **Data Type**: Positive integer that does not exceed the number of questions in the security questions list \(**Password Reset** &gt; **Security Questions**\).

 **Default Value**: 5

</td></tr><tr><td>

num\_reset

</td><td>

Number of security questions that are displayed on the Verify page while a user is attempting to reset the password. The user must answer all questions correctly to verify identity. The questions are selected at random and are presented in random order.The value that you specify here overrides the setting of the **Number of security questions required during the password reset request** property. See [Configure Password Reset properties](t_SetPwdResetProps.md).

 **Data Type**: Positive integer that does not exceed the value of the num\_enroll parameter

 **Default Value**: 3

</td></tr></tbody>
</table>3.  Click **Update**.


**Parent Topic:**[Password Reset verifications](../concept/c_PWRVerifications.md)

**Related topics**  


[Add a custom question to the Security Questions verification](t_CreateQAVerificationQs.md)

