---
title: Set up your language preferences for your Virtual Agent integration with Microsoft Teams
description: Set language preferences so that Virtual Agent is in the same language as the user's preferred Microsoft Teams language.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure VA for Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Set up your language preferences for your Virtual Agent integration with Microsoft Teams

Set language preferences so that Virtual Agent is in the same language as the user's preferred Microsoft Teams language.

## Before you begin

Role required: admin

## About this task

You set the Microsoft Teams language preference in the Microsoft Teams client. The ServiceNow language is the language that is typically used in the ServiceNow instance. By default, a user's Microsoft Teams language preference takes precedence over the user preference language of the base system if both languages are different. For more information, see [Change Settings in Microsoft Teams](https://support.microsoft.com/en-gb/office/change-settings-in-microsoft-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7).

To ensure consistency, use the same language. If the user preference language in Microsoft Teams isn’t an available language in the ServiceNow instance, then the instance language is the default language.

## Procedure

1.  Change which language takes precedence by configuring the following system property for users: **sn\_va\_teams.use\_teams\_language**.

    |Setting|Description|
    |-------|-----------|
    |**True**|The language displayed in Virtual Agent honors the user's preferred language that is set in Microsoft Teams.|
    |**False**|The language displayed in Virtual Agent honors the user's preferred language that is set on the ServiceNow instance.|


**Parent Topic:**[Configure Virtual Agent for Microsoft Teams](configure-va-msteams-settings.md)

