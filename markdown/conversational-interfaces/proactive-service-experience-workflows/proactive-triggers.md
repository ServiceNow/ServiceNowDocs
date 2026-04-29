---
title: Exploring Proactive Triggers
description: Proactive Triggers is a ServiceNow Store application that is available to all Virtual Agent chat widget and Agent Chat customers by default. Proactive Triggers can increase adoption of Virtual Agent by proactively sending context-specific messages to end users.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Exploring Proactive Triggers

Proactive Triggers is a ServiceNow® Store application that is available to all Virtual Agent chat widget and Agent Chat customers by default. Proactive Triggers can increase adoption of Virtual Agent by proactively sending context-specific messages to end users.

## Proactive Triggers overview

The Proactive Triggers rich text pop-up messages provide users with actions according to real-time Proactive Triggers data. When end users engage with the Proactive Triggers message, the Virtual Agent opens. If there’s a Virtual Agent topic, associated with the action, the topic runs. If buttons are presented to end users \(a maximum of three\), they can select the most relevant button to run the associated Virtual Agent topic. Proactive Triggers can be used with LLM topics if Now Assist in Virtual Agent is set up. Proactive Triggers can also be used with Agent Chat to connect customers to a live agent in configurations without Virtual Agent. For more information about the Proactive Triggers process, see [How Proactive Triggers work](how-proactive-triggers-work.md).

Proactive Triggers admins use Proactive Triggers rules to define when, where, and how to engage with customers. Proactive Triggers actions define what the rule does, using several key fields. Admins customize these rules and actions based on when and how their customers are most likely in need of help. For example, customers may need help when ordering equipment, opening an incident/case, or viewing information in a Knowledge Base article. Proactive Triggers rules can be applied to any defined URL, including any portal URL, catalog item, or external site. Proactive Triggers rules can be applied to the Proactive Triggers API after the **Proactive Trigger on Search** business rule and related trigger type, rule, and action are enabled. For additional information and an example of the Proactive Triggers API script, see [ProactiveTriggerAPI - Scoped](https://www.servicenow.com/docs/access?context=ProactiveTriggerScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

## Proactive Triggers examples

The Proactive Triggers feature uses rules and related actions based on those rules to present messages to end users. These rules and actions are context-specific and are based on real-time data gathered as end users navigate across portal pages or through the Proactive Triggers API call.

By default, the Proactive Triggers feature includes these sample rules: Virtual Agent greeting and Chat welcome message when a live agent is available.

See the following table for information about action type examples. The images in the Example column are all of standard chat, but this feature works the same in enhanced chat.

**Note:** Depending on the plugins installed, you may only see one of these rules or you may see other rules as well.

<table id="table_hzy_gz2_bxb"><thead><tr><th>

Default sample rules

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Virtual Agent greeting

</td><td>

This rule gives a sample welcome message to end users on a portal page. This message introduces the Virtual Agent to both internal and external end users.

</td><td>

![Sample welcome message on portal.](../image/welcome-message-sample.png)

</td></tr><tr><td>

Chat welcome message when a live agent is available

</td><td>

This rule gives a sample welcome message to end users when the chat widget is configured for Live Agent only. This message introduces Agent Chat to end users.**Note:** This message appears only if you have the Advanced Work Assignment \(AWA\) plugin \(agent chat\) installed.

</td><td>

![Sample welcome message from a live agent.](../image/live-agent-sample-rule.png)

</td></tr></tbody>
</table>After a rule is created, the admin creates one or more actions that are triggered by the rule. Actions define the messages that end users see based on the rule and the next steps available for the end users to take. These messages are displayed differently depending on the selected action type.

See the following table for information about action type examples. The images in the Example column are all of standard chat, but this feature works the same in enhanced chat.

|Action type|Description|Example|
|-----------|-----------|-------|
|Message only|End users see an HTML pop-up message.|![Proactive Triggers message only.](../image/pt-message-only-action-type.png)|
|Message that launches a virtual agent topic|End users see an HTML pop-up message that directs them to an available Virtual Agent topic.|![Proactive Triggers message that launches a Virtual Agent topic.](../image/pt-message-launches-va-topic.png)|
|Message that launches a selection of virtual agent topics|End users see an HTML pop-up message with up to three suggested action buttons that direct them to a relevant Virtual Agent topic.|![Proactive Triggers message that launches a selection of virtual agent topics.](../image/pt-message-launches-multi-buttons-va-topics.png)|

You can customize the appearance of the Proactive Triggers message. For example, you can change the side bar color of the message. For more information about customization, see [Configure Agent Chat in a portal](https://www.servicenow.com/docs/access?context=configure-va-in-sp&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

