---
title: Set up the Conversational SMS Integration with Twilio
description: Integrate Twilio with Virtual Agent so that you can engage in SMS bot conversations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Conversational SMS Integration with Twilio, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up the Conversational SMS Integration with Twilio

Integrate Twilio with Virtual Agent so that you can engage in SMS bot conversations.

## Before you begin

Before you can set up the Conversational SMS Integration with Twilio, complete the following tasks:

1.  Ensure that you have valid ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Twilio spoke
    -   Conversational SMS Service Channel
    -   Conversational SMS Integration with Twilio
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

2.  Install the following applications on your instance:
    -   Integration Hub
    -   Twilio spoke
    -   Conversational SMS Service Channel
    -   Conversational SMS Integration with Twilio
3.  [Set up Twilio spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-twilio.md)
4.  Ensure that the Conversational Custom Chat Integration plugin \(com.glide.cs.custom.adapter\) is active on your instance.

Role required: external\_app\_install\_admin or va\_admin

## Procedure

1.  Create a Hash Message Verification record.

    1.  In the navigation filter, enter `hash_message_verification.list` and click **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the auth token, such as TwilioSMSTestAppAuthToken.|
        |Description|Description of the auth token, such as "Twilio SMS Testing application Auth Token."|
        |Secret|Auth token that is associated with your Twilio phone number.|

    3.  Click **Submit**.

2.  Create a Message Auth record.

    1.  In the navigation filter, enter `message_auth.list` and click **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the message auth, such as VA Twilio SMS Test App Message Auth.|
        |Provider|Provider of the auth token. Enter `Twilio`.|
        |Group name|Name of the recipient group. Leave this field blank.|
        |Service Portal|Service Portal that is associated with the message auth. Leave this field blank.|
        |Inbound message verification|Hash message token that you created.|
        |Outbound message verification|Hash message token that you created.|
        |Outbound service token|Authorized outbound service token. Leave this field blank.|

    3.  Click **Submit**.

3.  Create a Messaging Provider Application record.

    1.  Navigate to **Conversational Interfaces** &gt; **SMS integration with Twilio** and click **New**.

    2.  On the form, fill in the fields.

<table id="table_f34_25r_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the entity that users are contacting, such as IT Service Desk.

</td></tr><tr><td>

Phone Number

</td><td>

Twilio phone number that users are contacting.**Note:** Be sure to include the '+' symbol and the country code in front of the phone number. For example: +18185559485.

</td></tr><tr><td>

Message auth

</td><td>

Message auth that you created.

</td></tr></tbody>
</table>    3.  Click **Submit**.

4.  In the Twilio Console, for the phone number that you specified in Step [3](configure-twilio-adapter.md#mess-prov-app), update the SMS incoming web-hook.

    To update the web-hook, navigate to the phone number in your Twilio console: **Phone Numbers** &gt; **Manager** &gt; **Active numbers**. Click on the phone number and enter the following address in the Messaging web-hook field:

    ```
    https://<instance-name>.service-now.com/api/sn_va_sms_twilio/message
    ```


## What to do next

After you set up the Conversational SMS Integration with Twilio, you can create SMS conversation topics in Virtual Agent Designer. For more information on using the tool, see [Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md).

**Parent Topic:**[Configuring Conversational SMS Integration with Twilio](../concept/configure-va-sms-twilio-app.md)

**Related topics**  


[Install Conversational SMS Integration with Twilio](install-sms-twilio.md)

[Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_InstallApplications.md)

[Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md)

