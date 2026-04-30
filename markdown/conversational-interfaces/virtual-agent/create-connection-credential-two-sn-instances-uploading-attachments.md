---
title: Create a connection and credential in Virtual Agent Bot Interconnect
description: Create a connection and credential in Virtual Agent Bot Interconnect \(primary instance\) to enable uploading of attachments in the secondary bot.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a connection and credential in Virtual Agent Bot Interconnect, Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create a connection and credential in Virtual Agent Bot Interconnect

Create a connection and credential in Virtual Agent Bot Interconnect \(primary instance\) to enable uploading of attachments in the secondary bot.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click the **Bot Interconnect VA API Attachment** record to open it.

3.  In the Connections related list, click **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name, such as `SNowSecondaryBotAttachment`.|
    |Credential|Leave this blank for now.|
    |Connection alias|Use the default value.|
    |Connection URL|Enter the URL of your secondary instance. For example, enter `https://secondary-instance-name.service-now.com/`.|

5.  Click **Submit**.

6.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

7.  On the Credentials page, click **New**.

8.  Click either **Basic Auth Credentials** or **OAuth 2.0 Credentials** as the type.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the credential. For example, `SNowSecondaryBotAttachmentToken`.|
    |Basic Auth Credentials|
    |Username|Enter the username you want to send as basic authentication credential..|
    |Password|Enter the password you want to send as basic authentication credential.|
    |OAuth 2.0 Credentials|
    |OAuth Entity Profile|In the OAuth profile field, select the OAuth 2.0 profile that specifies the credentials you want to send.|

10. Click **Submit**.

11. Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

12. Click the **Bot Interconnect VA API Attachment** record to open it.

13. In the Connections related list, open the new connection record you created in an earlier step.

14. In the **Credential** field, enter the name of the record that contains the static token or hash token.

    For example, `SNowSecondaryBotAttachmentToken`.

    ![ServiceNow Secondary Bot HTTPS connection view. Credential and Connection URL fields are highlighted as newly created credential record and VA API installation on the secondary bot instance.](../images/api-secondary-bot-attachment-connection-credential.png "Connection and credential record in the ServiceNow Bot Interconnect instance")

15. Click **Update**.


**Parent Topic:**[Create a connection and credential in Virtual Agent Bot Interconnect](create-connection-credential-two-sn-instances.md)

