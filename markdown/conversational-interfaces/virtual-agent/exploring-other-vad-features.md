---
title: Exploring other Virtual Agent features
description: After creating topics with the basic Virtual Agent Designer controls and scripting, you can also enhance conversation functionality and topic maintenance by using additional Virtual Agent features.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Virtual Agent, features, link unfurling, code reuse, Workflow studio, Agent Chat]
breadcrumb: [Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Exploring other Virtual Agent features

After creating topics with the basic Virtual Agent Designer controls and scripting, you can also enhance conversation functionality and topic maintenance by using additional Virtual Agent features.

After learning the basics, here are some other Virtual Agent features that may help you improve your authoring and end-user experience.

-   **[Deploy Virtual Agent in other channels](va-integrations.md)**

    By default, Virtual Agent runs in a chat widget, but you can also run it in other channels. While some features may not be available in certain channels \(such as the carousel user input control\), you can customize your conversation flow to accommodate these differences.

-   **[Use link unfurling in Virtual Agent](va-link-unfurling.md)**

    Virtual Agent supports link unfurling on the chat widget, mobile devices, and various channels. Link unfurling generates a content-rich preview when a supported link is shared in a conversation with a user, a virtual agent, or in a text-based bot response.

-   **[Improve the user experience with AI Search](va-ai-search.md)**

    What happens when a user utterance isn't matched to a keyword or intent? Enable AI Search as a fallback so that the user sees a list of search results as a response when no other match is found.

-   **[Maximize code reuse with topic blocks](topic-blocks-overview.md)**

    Rather than duplicate common functionality in multiple topics, you can create reusable topic blocks that you can reference in many topics. This allows you to maintain frequently used functionality in one central location.

-   **[Customize Virtual Agent with custom controls](custom-controls.md)**

    If a Virtual Agent Designer control doesn't quite work for what you want to achieve, create a custom control. You can create your own controls to accept input from the conversation, as well as custom response controls to handle the output. Use these controls within topics to handle specialized tasks.

-   **[Integrate Virtual Agent with Workflow Studio workflows](va-flow-designer-integration.md)**

    If your company is using Workflow Studio to create workflows, you can integrate them into Virtual Agent. You may need to do this if your conversations require you to pass secure inputs, such as a password. Workflow Studio actions and subflows support the password2 data type, which lets you pass the input securely.

-   **[Use Virtual Agent with Agent Chat](using-va-agent-chat.md)**

    Customize Virtual Agent to hand off some conversations to a live agent when needed.

-   **[Use Virtual Agent for Incident Auto-Resolution](auto-resolution-va.md)**

    Initiate a Virtual Agent conversation with an end user after they submit an incident through email or the ServiceNow® Service Portal if an existing Virtual Agent topic can resolve the issue.

-   **[Localize Virtual Agent topics](localize-va-topic.md)**

    Use the ServiceNow Localization Framework to translate topics and NLU models into other languages.

-   **NLU Workbench - Advanced Features**

    Expand the functionality of NLU Workbench to help you manage and improve your models. NLU Workbench - Advanced Features is available from the ServiceNow Store.

-   **[Integrate Virtual Agent with other portals and apps](integrate-virtual-agent.md)**

    Integrate and extend the capabilities of Virtual Agent by connecting to your employees and customers where they already are.

-   **[Use Virtual Agent REST API in a standalone or multi-bot environment](virtual-agent-api-landing-page.md)**

    Integrate any chat interface or bot using this REST API that is available in the ServiceNow Store.


## Additional resources

Take advantage of the following ServiceNow® resources to help you customize your Virtual Agent:

-   [Virtual Agent and Natural Language Understanding \(NLU\) community forum](https://community.servicenow.com/community?id=community_forum&sys_id=bf5abf94db54e3c42be0a851ca961915)
-   [Virtual Agent Academy](https://community.servicenow.com/community?id=community_event&sys_id=be9b3a771ba680d4d01143f6fe4bcbda&view_source=featuredList)

-   **[Deploying Virtual Agent topics in other channels](va-integrations.md)**  
When creating a topic or topic block, you can specify the chat channels in which the topic or topic block will run. During conversation design, Virtual Agent Designer provides built-in guardrails to help you tailor your conversations to those channels.
-   **[Using link unfurling in Virtual Agent](va-link-unfurling.md)**  
Virtual Agent supports link unfurling on the chat widget, mobile devices, and various channels. Link unfurling generates a content-rich preview when a supported link is shared in a conversation with a user, a virtual agent, or in a text-based bot response.
-   **[Improving the user experience with AI Search](va-ai-search.md)**  
Virtual Agent uses the ServiceNow AI Platform® AI Search application to return search results in bot conversations as a fallback when there are no relevant topics to display to end users. Virtual Agent also provides a Run AI Search topic block that topic authors can use to generate search results in a topic.
-   **[Integrating Virtual Agent with Workflow Studio workflows](va-flow-designer-integration.md)**  
The workflows of ServiceNow® Workflow Studio can be integrated within ServiceNow Virtual Agent topics. You can then use these workflows in Virtual Agent conversations.

**Parent Topic:**[Building and deploying Virtual Agent](using-virtual-agent.md)

