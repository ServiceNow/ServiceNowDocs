---
title: Set up Conversational Integration with WhatsApp \(powered by Twilio\)
description: Set up the Conversational Integration with WhatsApp \(powered by Twilio\) application so that you can engage requesters in bot conversations. Integrating with ServiceNow Virtual Agent enables you to interact on WhatsApp chat with a Virtual Agent or Live Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Conversational Integration with WhatsApp \(powered by Twilio\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up Conversational Integration with WhatsApp \(powered by Twilio\)

Set up the Conversational Integration with WhatsApp \(powered by Twilio\) application so that you can engage requesters in bot conversations. Integrating with ServiceNow Virtual Agent enables you to interact on WhatsApp chat with a Virtual Agent or Live Agent.

## Before you begin

Before you begin, do the following:

-   Get ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Twilio spoke
    -   Conversational Integration with WhatsApp \(powered by Twilio\)
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Install the following applications on your ServiceNow instance:
    -   Integration Hub
    -   Twilio spoke
    -   Conversational Integration with WhatsApp \(powered by Twilio\)
-   [Connect your Twilio Number to your WhatsApp Business Profile](https://www.twilio.com/docs/sms/whatsapp/tutorial/connect-number-business-profile).
-   [Set up Twilio spoke](https://www.servicenow.com/docs/access?context=setup-twilio&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

Role required: external\_app\_install\_admin or va\_admin

## Procedure

1.  Connect your company's Twilio account with your ServiceNow instance.

    1.  Log in to your [Twilio Console](https://www.twilio.com/console).

    2.  From the Project Info pane of the Console Dashboard page, note down the authentication token.

        You will later use this token to authenticate the Twilio account on your ServiceNow instance. For more information, see the [Twilio documentation](https://www.twilio.com/docs).

    3.  To specify the webhook URL, in the Twilio console, navigate to **Programmable Messaging** &gt; **Senders** &gt; **WhatsApp Senders**.

        To enable your Twilio account to send messages to your ServiceNow instance, enter the webhook URL in the following format: `https://<instance-name>.service-now.com/api/sn_va_whatsapp_twi/message`.

    4.  Click your WhatsApp-enabled Twilio phone number.

    5.  In the **A MESSAGE COMES IN** field of the Configure WhatsApp Number dialog box, enter the webhook URL of your ServiceNow instance and click **Configure**.

2.  To authenticate incoming hash messages from the Twilio account, create a Hash Message Verification record that stores the Twilio authentication token.

    1.  In the navigation filter of your ServiceNow instance, enter `hash_message_verification.list`.

    2.  In the Hash Message Verifications list, click **New**.

    3.  On the form, fill in the fields.

<table id="table_rw5_syy_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in the Hash Message Verification \[hash\_message\_verification\] table that stores the authentication token that is associated with your company's WhatsApp-enabled Twilio phone number. For example, `TwilioWhatsappTestAppAuthToken`.

</td></tr><tr><td>

Description

</td><td>

Description of the record. For example, `Twilio Whatsapp Testing application Auth Token`.

</td></tr><tr><td>

Secret

</td><td>

Twilio authentication token that is associated with your company's WhatsApp-enabled Twilio phone number.

</td></tr></tbody>
</table>    4.  Take note of the name of the Hash Message Verification record.

    5.  Click **Submit**.

3.  Associate inbound message records with a Message Auth record.

    1.  In the navigation filter of your ServiceNow instance, enter `message_auth.list` and click **New**.

    2.  On the form, fill in the fields.

<table id="table_nb4_vvr_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in the Message Auth \[message auth\] table. For example, `VA Twilio WhatsApp Test App Message Auth`.

</td></tr><tr><td>

Provider

</td><td>

Provider of the auth token. Enter `Twilio`.

</td></tr><tr><td>

Group name

</td><td>

Name of the group that you created.

</td></tr><tr><td>

Service Portal

</td><td>

Customer service portal that you created.

</td></tr><tr><td>

Outbound service token

</td><td>

A unique token used by the ServiceNow AI Platform to authenticate and authorize access to an external service or API. The token is a credential that allows the ServiceNow AI Platform to securely interact with other systems. This token is generated by the external service and provided to the ServiceNow AI Platform so that the platform can make requests and access resources.

</td></tr><tr><td>

Inbound message verification

</td><td>

Name of the Hash Message Verification record that you created for the inbound hash messages in [step 2](messg-whatsapp-setup.md#wa-hash).

</td></tr><tr><td>

Outbound message verification

</td><td>

Name of the Hash Message Verification record that you created for the inbound hash messages in [step 2](messg-whatsapp-setup.md#wa-hash).**Note:** The values for the **Inbound message verification** and **Inbound message verification** fields are the same.

</td></tr></tbody>
</table>    3.  Click **Submit**.

4.  Associate the Message Auth record with the WhatsApp-enabled Twilio phone number.

    1.  In the navigation filter of your ServiceNow instance, enter `sys_cs_provider.list`.

    2.  In the Provider Channels list, click **Twilio** from the **Name** column corresponding to the **WhatsApp** channel.

        If the **Twilio** entry is not present, enter `sys_cs_provider_application.list` in the navigation filter to create the list.

    3.  In the Provider Channel Identity related list, click **New**.

    4.  On the form, fill in the fields.

<table id="table_f34_25r_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the entity that users are contacting, such as IT Service Desk.

</td></tr><tr><td>

Inbound ID

</td><td>

Twilio phone number that users are contacting.

**Note:** Be sure to include the '+' symbol and the country code in front of the phone number. For example: +18185559485.

</td></tr><tr><td>

Message auth

</td><td>

Message auth that you created in [step 3](messg-whatsapp-setup.md#wa-auth-record).

</td></tr></tbody>
</table>    5.  Click **Submit**.


