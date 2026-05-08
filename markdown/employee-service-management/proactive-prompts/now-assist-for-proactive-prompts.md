---
title: Now Assist with Proactive Prompts
description: Your employees and managers can use conversational actions to see their pending HR tasks and how much remaining time off they have by using the Now Assist with the Proactive Prompts integration.
locale: en-US
release: australia
product: Proactive Prompts
classification: proactive-prompts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Proactive Prompts, HR Service Delivery, Employee Service Management]
---

# Now Assist with Proactive Prompts

Your employees and managers can use conversational actions to see their pending HR tasks and how much remaining time off they have by using the Now Assist with the Proactive Prompts integration.

The Proactive Prompts with the Now Assist integration uses large language models \(Now LLM Service\) to create a natural-language conversational experience that can improve the success of your prompts.

**Note:** Proactive Prompts support Now LLM Service actions for a more intelligent and flexible conversational experience.

A signal is the configuration for instructions about when to send them, what to send, whom to send them to, where to send them, and related actions to generate and deliver them. You can define whom to send the signal to, how often, and on what channels. The following two signal configurations are available so that your employees and managers can experience the Now LLM Service capabilities in Proactive Prompts:

-   Approvals pending: Displays a prompt to the employee on their pending HR tasks for approval. The corresponding action for this signal configuration is **Show Approvals**.
-   High PTO balance: Displays a prompt to the employee if more than 80 percent of their leaves are remaining. The corresponding action for this signal configuration is **Request PTO**.

The **Show Approvals** and **Request PTO** actions aren't available by default to add to the signal configuration as they’re inactive. Follow these steps to activate these actions:

-   Create and publish the Now LLM Service topics. For information on creating a Virtual Agent topic, see Creating a Virtual Agent topic. For information on publishing a Virtual Agent topic, see Publish a Virtual Agent topic
-   Create signal actions forProactive Prompts. For information about configuring signal actions for Proactive Prompts, see [Configure signal actions for Proactive Prompts](../task/proactive-prompts-signal-actions.md).
-   Select the actions in the signal channel configuration. For information on configuring the delivery channels in Proactive Prompts, see [Configure delivery channels in Proactive Prompts](../task/proactive-prompts-config-channels.md).

    **Note:** You can select both NLU and Now LLM Service actions in the **Virtual agent actions** field.


A single signal configuration caters to both NLU and Now LLM Service prompts and actions. The prompt is delivered to the portals depending on their Virtual Agent configuration. For example, if the portal has Now Assist configured, Now LLM Service prompts and actions are delivered. If the portal has NLU configured, NLU prompts and actions are delivered from the same signal configuration. For more information on the signal configuration, see [Create a signal in Proactive Prompts](../task/proactive-prompts-signal-create.md).

