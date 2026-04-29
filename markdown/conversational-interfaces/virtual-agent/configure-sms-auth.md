---
title: Configure SMS authentication
description: Authenticate all users using Conversational SMS Integration with Twilio with Soft PIN \(SN\) and Google authenticators as the 2-factor authentication mechanisms for account linking.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Conversational SMS Integration with Twilio, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure SMS authentication

Authenticate all users using Conversational SMS Integration with Twilio with Soft PIN \(SN\) and Google authenticators as the 2-factor authentication mechanisms for account linking.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  On your ServiceNow instance, enter `sys_cs_provider.list` and open **VA SMS Twilio Adapter Provider** record.

2.  In the VA SMS Twilio Adapter Provider record, select the **Allow account linking** check box.

    Selecting the **Allow account linking** check box populates the **Link account action** and **Account linking type** options.

3.  Select **Verification question and MFA** from the **Allow account linking** drop-down.

    When **Verification question and MFA** is selected, the **Automatic link action** field populates with the **sn\_va\_sms\_twilio.va\_sms\_auto\_link\_account** value.

    With **Verification question and MFA** selected, the end user is asked to enter the Soft Pin along with an MFA \(Multi-factor Authentication\) OTP \(One Time Password\) and Google authenticator is the default MFA method for SMS Twilio for enhanced security.

    If there is an invalid input/failure, you can continue the conversation as a guest user. ​Upon success, the session is elevated to the authenticated user session.

    Also, you can also look up the automatic link flow action from the Workflow Studio.

4.  Navigate to the **Define the identity and messages for this connection** section on the SMS Twilio provider channel record and click the **Provider Properties** tab to configure the following mandatory MFA Provider Properties.

    -   **verification\_question\_id**: Default sys\_id for SoftPIN verification. The default value can be customized.
    -   **two\_factor\_methods**: By default, Google authenticator is the two factor method if **Verification question and MFA** is selected.

        **google\_autheticator** or **sms** are the supported values.

        **Note:** If this property value is updated, then the **mfa\_question\_id** property value must be updated to the sys\_id of the corresponding verification Id.

    -   **mfa\_question\_id**: Corresponds to the two-factor method. The value is the default sys\_id for the google authenticator verification type.

        **Note:** If you set the value of two\_factor\_methods property to **sms**, then you must update the sys\_id of this property to SMS verification type.

        To get the SMS verification type sys\_id, navigate to **Verification Types** and copy the **SMS Code Verification Type** sys\_id record.

5.  To use account linking in SMS Twilio, navigate to the User \[sys\_user\] table by entering `sys_user.list`, pick a user, and update the user's mobile phone number with a valid incoming mobile phone number.

    After the incoming phone number is authenticated, the system authenticates the user and links the phone number to the respective User \[sys\_user\] ID.

6.  To Enroll the Soft PIN, perform the following steps:

    Setting up your Soft PIN enables you to use this PIN for identifying yourself when you try to have a conversation via SMS.

    1.  Impersonate the user that you picked in the Step 5 and navigate to **Password Reset** &gt; **Enroll**.

    2.  In the Password Reset Enrollment record, under the Soft PIN Verification tab, enter the Soft Pin in the **Enter the Soft PIN** field.

    3.  Under the **Authenticator App Verification** tab, click **Generate a new QR code** to generate the QR code for your Google authenticator if you have downloaded one.

    4.  Click **Submit**.

    When authentication is enabled for SMS, even when an actionable notification is triggered for the user in SMS conversation, user is expected to enter the Soft PIN and MFA to execute the action. For example, when an incident is updated, an actionable notification is triggered on the SMS app and you are asked to input your authentication code \(Soft PIN or MFA code\).


-   **[Rate limiting policy for SMS Authentication](../concept/sms-authentication.md)**  
Rate limiting policy locks out a user when an invalid or incorrect Soft PIN is entered consecutively for 3 times in a span of 24 hours.

**Parent Topic:**[Configuring Conversational SMS Integration with Twilio](../concept/configure-va-sms-twilio-app.md)

