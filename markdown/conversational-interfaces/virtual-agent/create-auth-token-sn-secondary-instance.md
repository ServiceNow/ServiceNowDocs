---
title: Create an auth token in the ServiceNow secondary instance
description: To use ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, create an authentication token in the secondary instance.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, Using Virtual Agent Bot Interconnect in your configuration, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create an auth token in the ServiceNow secondary instance

To use ServiceNow® Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect, create an authentication token in the secondary instance.

## Before you begin

[Create a connection and credential in Virtual Agent Bot Interconnect](create-connection-credential-two-sn-instances.md).

Role required: admin

## About this task

Ensure that the type of authentication \(Static or Hash\) and token or hash secret in the secondary instance is the same as the type and token or hash secret in the Bot Interconnect instance.

## Procedure

1.  Navigate to **All**, and then enter `token_verification.list` in the filter.

2.  On the Token Verifications page, click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name for the authentication token, such as `SNSecondaryBotToken`.|
    |Token|The static token or hash secret you provided in the Bot Interconnect \(primary\) instance.|

4.  Click **Submit**.

5.  Navigate to **All**, and then enter `message_auth.list` in the filter.

6.  On the Message Auth page, click **New**.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the message authentication, such as `SNtoSNAuthtoken`.|
    |Provider|Name of the provider, such as `ServiceNowProvider`.|
    |Group name|Name used to classify the provider.|
    |Service Portal|Set this field to link users on Virtual Agent integrations such as Slack and Microsoft Teams to a service portal login page. If the field is empty, Virtual Agent redirects the users to the instance login page.|
    |Inbound message verification|The name of the authentication token you created in the secondary instance. For example, `SNSecondaryBotToken`.|
    |Outbound message creation|The name of the authentication token you created in the secondary instance. For example, `SNSecondaryBotToken`.|
    |Outbound service token|The name of the authentication token you created in the secondary instance. For example, `SNSecondaryBotToken`.|

8.  Click **Submit**.

9.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the filter.

10. Open the VA Bot to Bot Provider Application record.

11. In the **Message auth** field, select the name of the message authentication record you created.

    For example, select **SNtoSNAuthtoken**.

12. Click **Update**.


**Parent Topic:**[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](../concept/using-sn-secondary-bot-with-sn-primary.md)

**Previous topic:**[Create a connection and credential in Virtual Agent Bot Interconnect](create-connection-credential-two-sn-instances-uploading-attachments.md)

**Next topic:**[Create a Virtual Agent Bot Interconnect shell topic to call Virtual Agent secondary topics](create-va-topic-sn-primary-secondary-config.md)

