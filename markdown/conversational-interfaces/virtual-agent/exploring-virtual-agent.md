---
title: Exploring Virtual Agent
description: The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations with an out-of-the-box system that help your users quickly obtain information, make decisions, and perform common work tasks with Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/exploring-virtual-agent.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Virtual Agent, Exploring, Now Assist, LLM, NLU, Natural Language Understanding, Large language model]
breadcrumb: [Virtual Agent, Conversational Interfaces]
---

# Exploring Virtual Agent

The ServiceNow Virtual Agent platform provides user assistance through conversations within an intelligent messaging interface. Design and build automated conversations with an out-of-the-box system that help your users quickly obtain information, make decisions, and perform common work tasks with Virtual Agent.

## Overview of Virtual Agent

Virtual Agent helps solve ordinary issues and delivers results for common requests, leaving your agents and technicians free to focus on more complex user issues. You can change the look and feel of the chat experience to suit each audience for your business, including running your chatbot in a variety of common or custom messaging channels. Use the Assistant Designer Analytics tab to monitor your bot's success.

Your developers have access to large language model \(LLM\) topic discovery. Assistant Designer includes LLM controls that make topic authoring easier so that you can deliver self-service solutions more quickly.

\[Omitted image "mmasset0022339.svg"\] Alt text: Virtual Agent increases deflection and improves self-service in a customizable environment. With ServiceNow Otto for Virtual Agent, development time is faster and uses generative AI LLM topic discovery.

## AI agents in Virtual Agent

Virtual Agent supports AI agents. When a user asks a question in chat, the agent understands the query and can reason, plan, and execute using tools such as the following:

-   AI agents
-   Virtual Agent topics
-   Conversational actions and subflows
-   Catalogs
-   Knowledge articles
-   Generative AI skills

Virtual Agent supports multi-intent queries with AI agents if there are associated AI agents per user query.

## Prebuilt Virtual Agent topics

Prebuilt Virtual Agent topics are available from the ServiceNow Store. These topics are designed to handle common issues that can occur and are customized for ServiceNow workflows. Available plugins include the following:

-   [ITSM Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/itsm-virtual-agent.md)
-   [Customer Service Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/activate-virtual-agent-csm.md)
-   [HR Service Delivery Virtual Agent conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/hr-virtual-agent-conversations.md)

## Virtual Agent availability

The Virtual Agent platform is available as a professional subscription or in a limited version \(Virtual Agent Lite\) that is automatically included with the ServiceNow AI Platform®.

Virtual Agent Professional provides all the core functionality for creating and deploying Virtual Agent conversations. Virtual Agent includes the following features, which are automatically installed with the Glide Virtual Agent plugin \(com.glide.cs.chatbot\):

-   Virtual Agent chat widget
-   Virtual Agent notifications
-   Conversational custom chat integration framework
-   Conversational Interfaces console for admin configuration

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

[Virtual Agent Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Empower users to self-serve using LLM topic discovery. Options include AI agents, enhanced or premium chat with AI Search, conversational catalog skills, and more.

</td><td>

[Case and incident deflection in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/case-incident-deflection-virtual-agent.md)[LLM topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-llm.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Create custom chat experiences for Virtual Agent users.

</td><td>

[Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md)

 [Branding your chat client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/branding-chat-client.md)

 [Customizing a Virtual Agent chat experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-conversation-settings.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Seamlessly transfer the entire conversation history and context to the right human agent so they can quickly address any escalations and resolve user issues.

</td><td>

[Using Virtual Agent with a live agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/using-va-agent-chat.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Connect to where your employees and customers already are—in web portals, Now® Mobile apps, and collaboration tools like Slack and Microsoft Teams, and any other popular chat or messaging app.

</td><td>

[Integrating Virtual Agent with other channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/integrate-virtual-agent.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Analyze the performance of assistants in Assistant Designer.

</td><td>

[Analyzing assistants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/ai-engagement-analytics.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Deliver real-time alerts and status updates to employees, including actionable notifications and SMS notifications. Deliver notifications via all supported channels, including web, Slack, and SMS. You can quickly collect feedback for critical decisions and resolve requests faster.

</td><td>

[Configuring Virtual Agent notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configuring-va-notifications.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Serve your international Virtual Agent users, regardless of their language and locale.

</td><td>



</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

Integrate with other ServiceNow AI Platform applications, such as AI Search. Use Workflow Studio to add automated workflows to conversation topics, and access many third-party services using Integration Hub spokes.

</td><td>

[Assign search sources to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/add-info-sources-assistant.md)

 [Integrating Virtual Agent with Workflow Studio workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/va-flow-designer-integration.md)

 [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integrationhub.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr><tr><td>

The Virtual Agent API enables developers, advanced users, and admins to use Virtual Agent as a standalone or secondary bot in your chat environment. Use Virtual Agent Bot Interconnect as the primary bot in a diverse chat environment.

</td><td>

[Virtual Agent API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/virtual-agent-api-landing-page.md)

 [Using Virtual Agent Bot Interconnect in your configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/using-sn-va-primary-bot-api.md)

</td><td>

virtual\_agent\_admin or admin

</td></tr></tbody>
</table>**Note:** For developer training, go to the [Developer's Portal](https://developer.servicenow.com/dev.do) \(login required\). Navigate to **Learn** &gt; **Courses** &gt; **Virtual Agent**.

