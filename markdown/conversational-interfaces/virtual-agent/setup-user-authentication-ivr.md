---
title: Configure user authentication for Conversational IVR
description: You must configure the authentication level for how the end-user can be authenticated to be the logged-in ServiceNow user using Voice.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure Conversational IVR with Amazon Connect, Integrating Virtual Agent with Conversational IVR, Integrating Virtual Agent with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Configure user authentication for Conversational IVR

You must configure the authentication level for how the end-user can be authenticated to be the logged-in ServiceNow user using Voice.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings** &gt; **Virtual Agent**.

2.  On the Virtual Agent Settings page, navigate to the Configure your interactive voice response \(IVR\) section and click **Configure IVR** under Configure pre-built adapter.

3.  On the Configure interactive voice response page, select **VA Amazon Connect Adapter Provider** from the Select IVR service provider drop-down.

4.  Under Provider Channel Identities, select the identity provider that you want to edit the user authentication for.

5.  On the Amazon Connect information form, in the Configure user authentication tile, click **Configure authentication**.

6.  On the User authentication method setup form, swipe the **Enable authentication** toggle switch to the right.

    **Note:** Ensure that the application scope of your ServiceNow instance is set to the Conversational IVR with Amazon Connect application before editing the User authentication method setup form.

7.  Select the **Authentication style**.

    -   **Phone**: Customer's phone number.

        **Note:** Only requires the incoming phone number to match the record in \[sys\_user\] profile **Business Phone** field, in order for user to log in.

    -   **Phone + Soft PIN**: Customer's phone number requiring a pre-configured Soft PIN to authenticate.

        **Note:** Requires not only the phone number to match, but also for end user to identify user's personal Soft PIN registered with the customer’s ServiceNow record.

    -   **Phone + Soft PIN + MFA**: Customer's phone number, requiring a Soft PIN and adds an extra layer of security with MFA \(Multi-factor Authentication\).

        **Note:** Requires the phone number to match and also for end user to identify user's personal Soft Pin registered with the customer’s ServiceNow record, in addition to have the end user authenticate using MFA.

    To set up your end users with Soft PIN or MFA, see [Configure your Password Reset process to auto-enroll users](https://www.servicenow.com/docs/access?context=configure-auto-enroll-for-pwd-reset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

8.  Provide the authentication details as per the selected authentication style.

    -   **Verification question**: Add a verification question of your choice.

        **Note:** This option is only available for Phone + Soft PIN.

    -   **Verification PIN length**: Set up the length of your Soft PIN.

        **Note:** This option is only available for Phone + Soft PIN.

    -   **One-time password length**: Set up the length of the one-time password

        **Note:** This option is only available for Phone + Soft PIN and Phone + Soft PIN + MFA.

    -   **one-time-password expiration time**: Set up the expiration time for the password.

        **Note:** This option is only available for Phone + Soft PIN and Phone + Soft PIN + MFA.

    Changing the values or messages updates the record on the Password Reset verification record. For more information, see [Configure your Password Reset process to auto-enroll users](https://www.servicenow.com/docs/access?context=configure-auto-enroll-for-pwd-reset&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

9.  Click **Save**.


