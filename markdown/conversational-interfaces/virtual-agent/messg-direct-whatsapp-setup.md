---
title: Set up Conversational Integration with WhatsApp \(WhatsApp Cloud API\)
description: Set up the Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application so that you can engage requesters in bot conversations. Integrating with ServiceNowVirtual Agent enables you to interact on WhatsApp chat with a Virtual Agent or Live Agent.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Conversational Integration with WhatsApp \(WhatsApp Cloud API\), Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up Conversational Integration with WhatsApp \(WhatsApp Cloud API\)

Set up the Conversational Integration with WhatsApp \(WhatsApp Cloud API\) application so that you can engage requesters in bot conversations. Integrating with ServiceNowVirtual Agent enables you to interact on WhatsApp chat with a Virtual Agent or Live Agent.

## Before you begin

Before you begin, do the following:

-   Get ServiceNow entitlements for the following products and applications:

    -   Integration Hub
    -   Conversational Integration with WhatsApp \(WhatsApp Cloud API\)
    For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

-   Set up the following applications on your ServiceNow instance:
    -   Integration Hub
    -   Conversational Integration with WhatsApp \(WhatsApp Cloud API\)

Role required: external\_app\_install\_admin or va\_admin

## Procedure

1.  Set up required on the meta developer account and Facebook business account.

    1.  Create a Meta developer app by completing the prerequisites and step 1 in the [WhatsApp Cloud API Get Started](https://developers.facebook.com/documentation/business-messaging/whatsapp/get-started) guide.

    2.  Copy the App Secret:

        -   On the Meta application dashboard, navigate to **App Settings** &gt; **Basic**.
        -   Note the App Secret.

            You would later use this token to authenticate the WhatsApp account on your ServiceNow instance.

    3.  Copy the Phone number ID:

        -   Navigate to **WhatsApp** &gt; **API Setup**.
        -   From the Send and receive messages section, select your WhatsApp-enabled phone number from the **From dropdown** list.

            You would need this ID to configure the provider record in your ServiceNow instance.

    4.  Create a system user access token in Meta Business Manager.

    For more information on how to create a system user access token, see [Generating System User Access Tokens](https://developers.facebook.com/documentation/business-messaging/whatsapp/access-tokens#generating-system-user-access-tokens). Grant the required permissions while creating the access token and copy the access token.

    You would need this token to configure the Token Verification record in your ServiceNow instance.

2.  To receive messages from WhatsApp in your ServiceNow instance, verify and configure the webhook URL.

    1.  In the navigation filter, enter `sys_properties.list`.

    2.  Locate and open the **sn\_va\_whatsapp.webhook\_verify\_token** property.

    3.  In the Value field, enter a chosen password or secret.

    4.  Select **Save**.

    5.  In the Meta developer console, navigate to **WhatsApp** &gt; **Configuration** &gt; **WhatsApp Configuration**.

    6.  Under the webhook section, in the callback URL field, enter the URL in the format `https://<instance-name>.service-now.com/api/sn_va_whatsapp/va_whatsapp_adapter`.

    7.  In the Verify token field, enter the chosen password you configured in the ServiceNow instance in step \(c\).

    8.  Select **Verify and save**.

    9.  In the Webhook fields section, enable the **Subscribe** toggle switch to subscribe to messages.

3.  To authenticate incoming hash messages from the WhatsApp account, create a Hash Message Verification record that stores the authentication token.

    1.  In the navigation filter of your ServiceNow instance, enter `hash_message_verification.list`.

    2.  In the Hash Message Verifications list, select **New**.

    3.  On the form, fill in the fields.

<table id="table_rw5_syy_2mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in the Hash Message Verification \[hash\_message\_verification\] table that stores the authentication token that is associated with your company's WhatsApp business phone number. For example, `WhatsappTestAppInboundToken`.

</td></tr><tr><td>

Description

</td><td>

Description of the record. For example, `WhatsApp Testing application Auth Token`.

</td></tr><tr><td>

Secret

</td><td>

App secret for the application that was set up in the Meta Developer Console.

</td></tr></tbody>
</table>    4.  Make a note of the name of the Hash Message Verification record.

    5.  Select **Submit**.

4.  To send messages with the required authentication headers to the WhatsApp account, create a Token Verification record that stores the system user access token.

    1.  In the navigation filter of your ServiceNow instance, enter `token_verification.list`.

    2.  In the Token Verifications list, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the record in the Token Verification \[token\_verification\] table that stores the system user access token that is associated with your company's Meta business account. For example, `WhatsappTestAppOutboundToken`.|
        |Description|Description of the record. For example, WhatsApp Business Testing Application Outbound Token.|
        |Token|System user access token created in Meta Business Manager|

    4.  Make a note of the name of the Token Verification record.

    5.  Select **Submit**.

5.  Associate outbound message records with a Message Auth record.

    1.  In the navigation filter of your ServiceNow instance, enter `message_auth.list` and select **New**.

    2.  On the form, fill in the fields.

<table id="table_nb4_vvr_cmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record in the Message Auth \[message auth\] table. For example, `VA WhatsApp Test App Message Auth`.

</td></tr><tr><td>

Provider

</td><td>

Provider of the auth token. Enter `WhatsApp`.

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

A unique token used by the ServiceNow AI Platform to authenticate and authorize access to an external service or API. The token is a credential that enables the ServiceNow AI Platform to securely interact with other systems. This token is generated by the external service and provided to the ServiceNow AI Platform so that the platform can make requests and access resources.

</td></tr><tr><td>

Inbound message verification

</td><td>

Name of the Hash Message Verification record that you created for the inbound hash messages.

</td></tr><tr><td>

Outbound message verification

</td><td>

Name of the Token Message Verification record that you created for the inbound hash messages.**Note:** The values for the **Inbound message verification** and **Inbound message verification** fields are the same.

</td></tr></tbody>
</table>    3.  Select **Submit**.

6.  Associate the Message Auth record with the WhatsApp-enabled phone number.

    1.  In the navigation filter of your ServiceNow instance, enter `sys_cs_provider.list`.

    2.  In the Provider Channels list, select **VA Whatsapp Adapter Provider** from the **Name** column corresponding to the WhatsApp channel.

        If the WhatsApp entry isn’t present, enter `sys_cs_provider_application.list` in the navigation filter to create the list.

    3.  In the Provider Channel Identity related list, select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the entity that users are contacting, such as IT Service Desk.|
        |Inbound ID|Phone number ID corresponding to your WhatsApp-enabled phone number.|
        |Message auth|Message auth that you created.|

    5.  Select **Submit**.

7.  Configure the provider channel identity properties.

    1.  Select a provider channel identity that you created.

    2.  From the Provider Channel Identity Properties section, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the entity that users are contacting. Enter display\_phone\_number.|
        |Value|Enter the actual phone number corresponding to the Phone Number ID that you created.|
        |Description|Add a description for the provider channel.|

    4.  Select **Submit**.

8.  Enable the server to download media content sent by you.

    1.  In the navigation filter of your ServiceNow instance, enter `sys_cs_provider.list`.

    2.  In the Provider Channels list, select **VA Whatsapp Adapter Provider** from the Name column corresponding to the WhatsApp channel.

    3.  Enter `lookaside.fbsbx.com` in the trusted media domains field.

    4.  Select **Update**.


**Parent Topic:**[Configure Conversational Integration with WhatsApp \(WhatsApp Cloud API\)](messg-direct-whatsapp-configure.md)

