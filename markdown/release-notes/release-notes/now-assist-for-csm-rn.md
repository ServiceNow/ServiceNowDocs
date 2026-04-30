---
title: Now Assist for Customer Service Management \(CSM\) release notes
description: The ServiceNow Now Assist for CSM application brings generative AI to Customer Service Management \(CSM\). You can improve productivity and efficiency by delivering better self-service, recommending actions, and delivering answers. Now Assist for CSM was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 10
---

# Now Assist for Customer Service Management \(CSM\) release notes

The ServiceNow® Now Assist for CSM application brings generative AI to Customer Service Management \(CSM\). You can improve productivity and efficiency by delivering better self-service, recommending actions, and delivering answers. Now Assist for CSM was enhanced and updated in the Yokohama release.

## Now Assist for CSM highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Enabled is\_template for all Now Assist skills and added support to clone and customize any base system GenAI skill in the Now Assist Skill Kit.
-   Defined the navigation path for Sentiment Analysis dashboard in Core UI to make accessing sentiment analysis data easier.
-   Track trending case topics with insights, visualizations, and customizable filters for deeper analysis with the Trending topics dashboard.
-   Monitor customer sentiment across cases with LLM-powered insights and track the sentiment trends in the dashboard.
-   Enable agents to access customer, case, and product details instantly through natural language queries with the Provide customer 360 insight agentic workflow.
-   Auto-generate work notes and comment recommendations to help improve agent efficiency with the activity response generation skill.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Yokohama Patch 6](../quality/yokohama-patch-6.md)

-   Enable security in Now Assist for CSM and AI agents and agentic workflows by enforcing access control lists \(ACLs\) and user identity-based permissions.

[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   Analyze your customers' sentiment and sentiment trends in your cases and the reasoning behind it.
-   Use case resolution steps to generate recommended actions based on the data clusters from previously closed cases.
-   Integrate the support for public web content in search queries for both standard and conversational search.
-   Use enhanced AI agents and new standalone AI agents for more specific tasks. For example, the Duplicate identifier AI agent identifies the duplicate interactions and cases from the customers and then consolidates the information.

[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   Improve agent productivity by managing long-running cases with the Triage cases AI agent.

Yokohama Early Availability

-   Use the Now LLM Service scheduling assistance when booking an appointment through Virtual Agent. You can use this scheduling assistance to schedule, reschedule, or cancel an appointment.
-   Help requesters find solutions by using Genius Results to reduce the number of cases created and decrease the effort needed by agents to close them.
-   Use the Now Assist panel global skill search to ask questions and fetch answers from knowledge articles.

See [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for CSM is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Enabled the is\_template property](https://www.servicenow.com/docs/access?context=clone-the-now-assist-for-csm-skills&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enabled the is\_template property for all Now Assist skills to ensure consistent cloning. Added the ability to clone any base system GenAI skill and customize it in the Now Assist Skill Kit \(NASK\) to reduce setup time and simplify skill modification. Applies to all Now Assist for CSM skills.

-   **Access Sentiment analysis dashboard in Core UI**

    Defined the navigation path in Sentiment Analysis dashboard in the Core UI interface to make it easier for users to locate and access sentiment analysis data without searching through multiple menus.

-   **[Sentiment trends analysis dashboard](https://www.servicenow.com/docs/access?context=use-sentiment-analysis-dashboard&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Get a comprehensive view of customer sentiment across case. The dashboard uses LLM-powered insights to explain sentiment changes and lets you drill down to find root causes and real time insights—helping managers take targeted actions.

-   **[Trending topics dashboard](https://www.servicenow.com/docs/access?context=view-trending-topics-dashboard&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Get a comprehensive view of trending topics across cases along with insights and visualizations to facilitate deeper analysis. This feature helps support teams track trend progression, regional impact, and drill down into specific trends using customizable filters.

-   **[Provide customer 360 insights agentic workflow](https://www.servicenow.com/docs/access?context=customer-service-management-ai-agent-collection-customer-360&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the provide customer 360 insights agentic workflow to provide synthesized and relevant customer insights to live agents via conversations. This agentic workflow is designed to support human agents by responding to natural language queries regarding cases, customer history, products, and interactions. This feature expedites access to vital information and case resolution, identifies patterns, and leverages past similar cases for guidance as well as triggers actions from the Now Assist panel.

-   **[Activity response generation skill](https://www.servicenow.com/docs/access?context=generate-a-recommendation-to-respond-to-an-activity&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the activity response generation skill to automatically generate recommendations for resolution notes, work notes, and comments. This feature helps agents add meaningful updates to case records, improving efficiency, and interaction.

-   **[Now Assist context menu configuration for extended tables within resolution notes](https://www.servicenow.com/docs/access?context=customize-now-assist-context-menu-for-skills&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Configure output fields for resolution notes through the Now Assist context menu configuration page so skills apply to extended tables without any additional setup.


-   **[Triage cases agentic workflow security directives](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Implement security on AI agents and agentic workflows through ACLs and user identities.

-   **[Now Assist for CSM Gen AI security directives](https://www.servicenow.com/docs/access?context=configure-chat-summarization-in-now-assist_0&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Implement security in Now Assist for CSM skills through ACLs and user identities.


[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Sentiment analysis on a case](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Make informed decisions on cases that are based on your requester’s sentiment and the reasoning behind it. You can update the sentiment when new comments or emails from your customers come in to ensure that the sentiment is always up to date​.

-   **Sentiment analysis on an account**

    Track the sentiment of a business-to-business account and analyze it by using various filters and sorting dashboards. You can get the right insights and reduce the number of escalated cases.

-   **[Suggested steps in Recommended Actions](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use Recommended Actions to generate suggested resolution steps for cases. You can increase agent productivity by outlining the next best actions for unfamiliar cases and automatically providing logical next steps.

-   **[Support for conversational subflows and actions in the Now Assist panel](https://www.servicenow.com/docs/access?context=request-gen-ai-capabilities-csm-now-assist-panel&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use natural language to describe your intent to trigger a subflow or action. This feature helps to improve your agent productivity and enables them to accomplish everything in one place within the Now Assist panel.

-   **[External web content in Q&amp;A Genius Results](https://www.servicenow.com/docs/access?context=using-ai-search-with-q-a-within-the-portal-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Provide the support for your public web content so that your requesters can use search queries in both standard search and conversational search. You can also see whether the content is internal or external, with direct links to the source.

-   **[Troubleshooting steps identification AI agent](https://www.servicenow.com/docs/access?context=troubleshooting-steps-identification-ai-agent&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Gather context from cases, identify missed fixes, and troubleshoot potential solutions by using the Troubleshooting steps identification AI agent.


[Yokohama Patch 1](../quality/yokohama-patch-1.md)

-   **[Triage cases AI agents use case](https://www.servicenow.com/docs/access?context=csm-ai-agents-use-cases&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the Triage cases AI agents use case to improve agent productivity through faster assessment.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Triage cases|Use AI agents to handle all routine cases coming in through email and other offline channels, so that it improves customer satisfaction and reduces resolution times.|


Yokohama Early Availability

-   **[Conversational search in the Now Assist panel with results from knowledge articles](https://www.servicenow.com/docs/access?context=using-conversational-search-in-now-assist-panel&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Ask questions directly within the Now Assist panel. If the answer is found in the knowledge bases \(KBs\), the answer is shown with the source information. If the answer isn't available in the KB search, you’re redirected to the global search experience for further assistance.

-   **[Now Assist in Virtual Agent-Scheduling Assistant via GenAI](https://www.servicenow.com/docs/access?context=using-scheduling-assistant-via-genai-in-virtual-agent&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Use the enhanced scheduling assistant with Now LLM Service capabilities to make it more conversational, enabling users to easily schedule, reschedule, and cancel appointments.

-   **[Now Assist in portal case form](https://www.servicenow.com/docs/access?context=using-ai-search-with-q-a-within-the-portal-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Guide requesters through a self-service flow to find solutions to their problems by using Genius Results. You can reduce the number of cases created and decrease the effort required by your agents to close open cases.


## Changed in this release

-   **[Enhancement in case summarization skill flow](https://www.servicenow.com/docs/access?context=case-summarization-generation-in-now-assist&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The **Define trigger** step has been added to the case summarization flow. This step enables admins to choose between the User Trigger option, where users select a button to generate a summary, and the Automatic Trigger option, where summaries are automatically generated based on specified conditions.

-   **[Enhancement in email reply recommendation skill](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Generate reply suggestions in the compose area using preset templates that include headers, footers, and signatures.

-   **[Unified admin experience for Now Assist skills](https://www.servicenow.com/docs/access?context=clone-the-now-assist-for-csm-skills&version=yokohama&pubname=yokohama-customer-service-management&section=customizing-now-assist-skills&ft:locale=en-US)**

    Skills cloned in Now Assist Admin console can now be edited in Now Assist Skill Kit. This update unifies the admin experience across Now Assist Admin and Now Assist Skill Kit, enabling users to add headers, configure prompts, and manage Now Assist skills in one location. The migration supports case summarization and resolution notes generation.

-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.

-   **[Display sentiment scale in case list view](https://www.servicenow.com/docs/access?context=analyze-sentiments-in-now-assist-for-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Added sentiment scoring to both the case record page and list view across cases, giving agents immediate visibility into the emotional tone of customer interactions. The sentiment scale ranges from very positive, positive, neutral, negative to very negative.


-   **[Multilingual Support](https://www.servicenow.com/docs/access?context=now-assist-csm-supporting-info&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enhanced multilingual support in chat summarization, resolution notes, and knowledge generation. Leveraged native multilingual LLMs for improved fluency and domain specificity, addressing translation inconsistencies across Tier 1 and Tier 2 languages.


[Yokohama Patch 3](../quality/yokohama-patch-3.md)

-   **[Triage cases agentic workflows enhancements](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Added new standalone AI agents to check duplicate cases and split some existing standalone AI agents to focus on more specific tasks. The AI agents available are the Triage cases planner AI agent, Context validator and analyzer agent, Duplicate identifier AI agent, Informational queries AI agent, Transactional queries AI agent, Case creation AI agent, Entity extraction AI agent, Document verification AI agent, and Email response AI agent.

-   **[Now Assist in Portal case form enhancement](https://www.servicenow.com/docs/access?context=using-ai-search-with-q-a-within-the-portal-form&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Added the new **Ask Now Assist** button that opens a contextual chat window so that a requester can carry the conversation forward. If no results are found or if the requester isn’t satisfied with the result, they can get further assistance by selecting the button to chat and get an answer, which helps to avoid case creation.


Yokohama Early Availability

-   **[Email reply recommendations enhancements](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Refined the AI-generated reply recommendation to create the best response for users by applying tone changes in the Now Assist context menu. Additional tone options, including casual, formal, and sympathetic, are available.

-   **[Chat reply recommendation enhancements](https://www.servicenow.com/docs/access?context=generate-chat-reply-recommendations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Added the chat reply recommendation enhancements to respond in a conversational tone and get feature parity in the Now Assist Admin console:

    -   Refined the AI-generated reply recommendation to create the best answer for your users by applying tone changes in the Now Assist context menu. Additional tone options, including casual, formal, and sympathetic, are available.
    -   Added parity with the chat summarization Now Assist Admin console capabilities. The Now Assist Admin console can specify the portal and channels for chat reply recommendations and assign additional support roles.
-   **[Case summarization enhancement](https://www.servicenow.com/docs/access?context=summarize-a-call-by-using-now-assist-for-customer-service-management-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Detailed feedback option is now available for negative feedback ![thumbs down icon](../../reuse/icons/product-icons/thumbs-down-outline-24.svg) in the generated case summary.

    Xanadu Patch 7: Extended the capabilities of the case summarization feature so it can now be used on custom tables.


## Activation information

Now Assist features are available with activation of the Now Assist for CSM plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Starting with Vancouver Patch 4, Now Assist for CSM is supported.

Starting with Xanadu Patch 7, Customer Service Management AI agent collection is supported.

## Additional requirements

The Now Assist for CSM application requires a Customer Service Management Pro Plus or Enterprise Plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

