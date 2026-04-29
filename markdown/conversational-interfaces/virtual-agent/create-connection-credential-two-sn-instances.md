---
title: Create a connection and credential in Virtual Agent Bot Interconnect
description: To use ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, configure the connection and credential records in the Bot Interconnect \(primary\) instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Create a connection and credential in Virtual Agent Bot Interconnect

To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, configure the connection and credential records in the Bot Interconnect \(primary\) instance.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Click the **Bot Interconnect VA API Integration** record to open it.

3.  In the Connections related list, click **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name, such as `SNow Secondary Bot`.|
    |Credential|Leave this blank for now.|
    |Connection alias|Use the default value.|
    |Connection URL|Enter the URL for Virtual Agent API on your secondary instance. For example, enter `https://secondary-instance-name.service-now.com/api/sn_va_as_service/bot/integration`.|

5.  Click **Submit**.

6.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

7.  On the Credentials page, click **New**.

8.  Click either **Bot Interconnect Hash Token Credential** or **Bot Interconnect Static Token Credential** as the type.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique name for the credential. For example, `SNowSecondaryBotToken`.|
    |Static token|
    |Header|Enter `Token`.|
    |Static Token|Enter a password.|
    |Hash token|
    |Header|Enter `x-b2b-signature`.|
    |Algorithm|Select **HmacSHA1**.|
    |Hash Secret|Enter the hash secret.|
    |Authorization Algorithm|Select the algorithm to use. For example, **Secondary Bot Hash Token Auth**.|

10. Click **Submit**.

11. Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

12. Click the **Bot Interconnect VA API Integration** record to open it.

13. In the Connections related list, open the new connection record you created in an earlier step.

14. In the **Credential** field, enter the name of the record that contains the static token or hash token.

    For example, `SNowSecondaryBotToken`.

    ![ServiceNow Secondary Bot HTTPS connection view. Credential and Connection URL fields are highlighted as newly created credential record and VA API installation on the secondary bot instance.](../images/api-secondary-bot-connection-credential.png "Connection and credential record in the ServiceNow Bot Interconnect instance")

15. Click **Update**.


-   **[Create a connection and credential in Virtual Agent Bot Interconnect](create-connection-credential-two-sn-instances-uploading-attachments.md)**  
Create a connection and credential in Virtual Agent Bot Interconnect \(primary instance\) to enable uploading of attachments in the secondary bot.

**Parent Topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-sn-secondary-bot-with-sn-primary.md)

**Previous topic:**[Enable asynchronous mode on the secondary ServiceNow Virtual Agent instance](enable-async-mode-secondary-sn-bot.md)

**Next topic:**[Create a connection and credential in Virtual Agent Bot Interconnect](create-connection-credential-two-sn-instances-uploading-attachments.md)

