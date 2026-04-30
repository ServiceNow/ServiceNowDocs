---
title: Customize Virtual Agent welcome messages in Microsoft Teams
description: Alter the default welcome message to send a custom greeting in Virtual Agent conversations integrated with Microsoft Teams.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-08-20"
reading_time_minutes: 1
keywords: [virtual, agent, chat, custom, welcome, message, conversational, interfaces, microsoft, teams, genAI]
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Customize Virtual Agent welcome messages in Microsoft Teams

Alter the default welcome message to send a custom greeting in Virtual Agent conversations integrated with Microsoft Teams.

## Before you begin

Role required: virtual\_agent\_admin or admin

Install the Microsoft Teamsplugin. For more information, see [Integrating Virtual Agent with Microsoft Teams](../concept/va-integ-msteams.md).

## About this task

The Provider Channel Identity \[sys\_cs\_provider\_application\_list\] table stores identities for various chat channels, including for Virtual Agent in Microsoft Teams. The Bot Messages tab previously used the **msteams\_welcome\_part1\_msg** and **msteams\_welcome\_part2\_msg** parameters for welcome messages. The new **default\_welcome\_message** parameter replaces both parameters with a single message parameter instead.

## Procedure

1.  Navigate to **All** &gt; **sys\_cs\_provider\_application.list**.

2.  Select the **Provider** entry `VA Teams adapter provider`.

3.  On the **Bot messages** tab, select **New**.

4.  On the form, fill out the following fields.

    |Property|Description|
    |--------|-----------|
    |Name|Enter `default_welcome_message`.|
    |Value|Enter your new welcome message. For example, `Welcome to Virtual Agent for Microsoft Teams!`|
    |Description|Enter a description for your message. For example, `New default welcome message.`|
    |Message type|Select **message** from the drop-down menu.|
    |Provider Channel Identity|This is the name of the Provider Channel Identity.|

5.  Select **submit**.


## Result

The Channel Identity for Virtual Agent Microsoft Teams has the new **default\_welcome\_message** parameter in the Bot Messages tab. The new welcome message displays each time you open a Virtual Agent conversation in Microsoft Teams.

**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

