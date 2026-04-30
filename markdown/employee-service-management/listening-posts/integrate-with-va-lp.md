---
title: Integrating Listening Posts integration with Virtual Agent
description: Enable an employee to complete a pulse survey from other communication channels such as Virtual Agent, Slack, Microsoft Teams, and chat web client in Employee Center.
locale: en-US
release: yokohama
product: Listening Posts
classification: listening-posts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Listening Posts integrations, Listening Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Integrating Listening Posts integration with Virtual Agent

Enable an employee to complete a pulse survey from other communication channels such as Virtual Agent, Slack, Microsoft Teams, and chat web client in Employee Center.

Listening Posts integrates with Virtual Agent to deliver pulse survey as an actionable notification on Virtual Agent. This integration with Virtual Agent allows integrating with other communication applications, such as Slack and Microsoft Teams.

For sending survey notifications on Virtual Agent, the **Virtual Agent notifications** option must be enabled while pulse survey is created in Listening Posts. When the pulse survey is published, an actionable survey notification is automatically sent to all pulse survey users on Virtual Agent. The actionable survey notification is also displayed in a chat web client in Employee Center.

For sending survey notifications on Slack and Microsoft Teams, notifications must be enabled on Slack and Microsoft Teams. For more details, see [Virtual Agent integration with messaging apps](https://www.servicenow.com/docs/access?context=va-integration-messaging-apps&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

For sending notifications via an SMS, a delivery channel must be set up in **Pulse survey notification content SMS** in the Virtual Agent Notification Messaging. For more details, see [Set up the Conversational SMS Integration with Twilio](https://www.servicenow.com/docs/access?context=configure-twilio-adapter&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

**Note:** When a survey creator enables the **Send Virtual agent notifications** option, then all the enabled integrations such as Microsoft Teams, Slack, and SMS are used and the pulse survey is pushed to those channels. If a survey recipient takes the survey on one channel, then the survey becomes inaccessible on the remaining channels.

**Parent Topic:**[Listening Posts integrations](listening-posts-integrations.md)

**Related topics**  


[Integrating Listening Posts with User Experience Analytics](lp-apps.md)

[Integrating Listening Posts with Journey designer](integrating-li-jny.md)

