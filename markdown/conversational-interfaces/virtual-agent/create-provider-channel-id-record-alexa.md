---
title: Create a provider channel identity record for Alexa
description: Create a provider channel identity record to connect to your Alexa account.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Conversational Integration with Alexa, Configure Conversational Integration with Alexa, Conversational Integration with Alexa, Conversational IVR with Amazon Connect, Virtual Agent integration with Voice channels, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Create a provider channel identity record for Alexa

Create a provider channel identity record to connect to your Alexa account.

## Before you begin

Role required: va\_admin or admin

## Procedure

1.  In the navigation filter of your ServiceNow instance, enter `sys_cs_provider_application.list`.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_etf_jfy_jqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your provider.

</td></tr><tr><td>

Provider

</td><td>

Provider channel that you created.Select **VA Alexa Adapter Provider** as the provider channel.

 **Note:** The provider is available with the installation of the Conversational Integration with Alexa plugin \(sn\_va\_alexa\).

</td></tr><tr><td>

Default portal

</td><td>

Default portal used in the mapping.

</td></tr><tr><td>

Short description

</td><td>

Short description for your channel identifier.For security reasons, the Virtual Agent checks that the URLs for attachments in conversations are from trusted domains specified here. If the URL is not from a trusted domain, the Virtual Agent does not upload the attachment.

 If an attachment upload fails because Virtual Agent did not trust the domain, Virtual Agent does not inform the end user about the attachment upload failure.

</td></tr><tr><td>

Message auth

</td><td>

Message authentication for the channel identifier.Choose a message authentication type from the following options:

-   ServiceNow Virtual Agent Alexa App - Static
-   ServiceNow Virtual Agent Alexa App - Hash


</td></tr><tr><td>

Inbound ID

</td><td>

Identifier for your bot.In this field, provide your Alexa Skill ID that you copied from the Amazon developer console.

 For example: `amzn1.ask.skill.XXXXXXX-XXXX-XXXX-XXXX-XXXXXXX`.

</td></tr></tbody>
</table>4.  Click **Submit**.


