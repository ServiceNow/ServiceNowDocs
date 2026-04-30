---
title: Exploring Virtual Agent
description: The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations with an out-of-the-box system that help your users quickly obtain information, make decisions, and perform common work tasks with Virtual Agent.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-11-14"
reading_time_minutes: 6
keywords: [Virtual Agent, Exploring, Now Assist, LLM, NLU, Natural Language Understanding, Large language model]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Exploring Virtual Agent

The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations with an out-of-the-box system that help your users quickly obtain information, make decisions, and perform common work tasks with Virtual Agent.

## Overview of Virtual Agent

Virtual Agent helps solve ordinary issues and delivers results for common requests, leaving your agents and technicians free to focus on more complex user issues. You can change the look and feel of the chat experience to suit each audience for your business, including running your chatbot in a variety of common or custom messaging channels. Monitor your bot's success with the Conversational Analytics dashboard.

When you add Now Assist in Virtual Agent skills, your developers have access to large language model \(LLM\) topic discovery. The Now Assist topics skill includes LLM controls that make topic authoring easier so that you can deliver self-service solutions more quickly.

![Virtual Agent increases deflection and improves self-service in a customizable environment. With Now Assist in Virtual Agent, development time is faster and uses generative AI LLM topic discovery.](../images/va-landing-page-overview.png)

## Pre-built Virtual Agent topics

Pre-built Virtual Agent topics are available from the ServiceNow Store. These topics are designed to handle common issues that can occur and are customized for ServiceNow workflows. Available plugins include the following:

-   [ITSM Virtual Agent conversations](https://www.servicenow.com/docs/access?context=itsm-virtual-agent&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [Customer Service Virtual Agent conversations](https://www.servicenow.com/docs/access?context=activate-virtual-agent-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [HR Service Delivery Virtual Agent conversations](https://www.servicenow.com/docs/access?context=hr-virtual-agent-conversations&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)

## Virtual Agent and Virtual Agent Lite

The Virtual Agent platform is available as a professional subscription or in a limited version \(Virtual Agent Lite\) that is automatically included with the ServiceNow AI Platform®.

Virtual Agent Professional provides all the core functionality for creating and deploying Virtual Agent conversations. Virtual Agent includes the following features, which are automatically installed with the Glide Virtual Agent plugin \(com.glide.cs.chatbot\):

-   Virtual Agent Designer \(supports Natural Language Understanding \(NLU\) in Virtual Agent conversations\)
-   Virtual Agent chat widget
-   Virtual Agent notifications
-   Conversational custom chat integration framework
-   Conversational Interfaces console for admin configuration
-   Topic Recommendations \(ServiceNow Store app\)
-   Conversational Analytics \(ServiceNow Store app\)

Virtual Agent Lite provides a limited \(trial\) version of Virtual Agent for ITSM standard customers. For more information, see [Virtual Agent Lite](va-lite.md).

## Virtual Agent benefits

<table id="table_ogy_wpy_1bc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Use a conversation designer to build and test conversations without scripting or advanced skills. Drag and drop elements on the graphical canvas to see the entire flow. Go further with branching, looping, and scripting.

</td><td>

[Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Use LLM topic discovery instead of Natural Language Understanding \(NLU\) or keywords to create more conversational experiences. Now Assist in Virtual Agent uses LLMs and generative AI skills to improve deflection rates and reduce the amount of time-consuming work that NLU topic discovery requires.

</td><td>

[Now Assist in Virtual Agent](../../now-assist-in-va/concept/now-assist-in-va-landing.md)

 [LLM topic discovery in Virtual Agent](va-llm.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Create custom chat experiences for users from where they run Virtual Agent.

</td><td>

[Configuring Now Assist in Virtual Agent](../../now-assist-in-va/task/configure-now-assist-va.md)

 [Branding your chat client](../../conversational-interfaces/concept/branding-chat-client.md)

 [Setting up chat experiences for Virtual Agent users](va-conversation-settings.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Seamlessly transfer the entire conversation history and context to the right human agent so they can quickly address any escalations and resolve user issues.

</td><td>

[Using Virtual Agent with a live agent](using-va-agent-chat.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Connect to where your employees and customers already are—in web portals, Now® Mobile apps, and collaboration tools like Slack, Microsoft Teams, Facebook Messenger consumer app, Workplace from Facebook enterprise messaging app, and any other popular chat or messaging app.

</td><td>

[Integrating Virtual Agent with other channels](integrate-virtual-agent.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Analyze the performance of Virtual Agent through preconfigured dashboards.

</td><td>

[Analyzing Virtual Agent performance](analyzing-virtual-agent-performance.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Deliver real-time alerts and status updates to employees, including actionable notifications and SMS notifications. Deliver notifications via all supported channels, including web, Slack, Workplace, and SMS. You can quickly collect feedback for critical decisions and resolve requests faster.

</td><td>

[Configuring Virtual Agent notifications](configuring-va-notifications.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Serve your international Virtual Agent users, regardless of their language and locale.

</td><td>

[Localization options for Virtual Agent](multi-language-options-va.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Integrate with other ServiceNow AI Platform applications, such as AI Search. Use Workflow Studio to add automated workflows to conversation topics, and access many third-party services using Integration Hub spokes.

</td><td>

[Improving the user experience with AI Search](va-ai-search.md)

 [Integrating Virtual Agent with Workflow Studio workflows](va-flow-designer-integration.md)

 [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

The Virtual Agent API enables developers, advanced users, and admins to use Virtual Agent as a standalone or secondary bot in your chat environment. Use Virtual Agent Bot Interconnect as the primary bot in a diverse chat environment.

</td><td>

[Using Virtual Agent API](virtual-agent-api.md)

 [Using Virtual Agent Bot Interconnect in your configuration](using-sn-va-primary-bot-api.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr></tbody>
</table>**Note:** For developer training, go to the [Developer's Portal](https://developer.servicenow.com/dev.do) \(login required\). Navigate to **Learn** &gt; **Courses** &gt; **Virtual Agent**.

