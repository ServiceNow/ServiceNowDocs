---
title: Now Assist for Customer Service Management \(CSM\) release notes
description: The ServiceNow Now Assist for CSM application brings generative AI to Customer Service Management. You can improve productivity and efficiency by delivering better self-service, recommending actions, and delivering answers. Now Assist for CSM was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Now Assist for Customer Service Management \(CSM\) release notes

The ServiceNow® Now Assist for CSM application brings generative AI to Customer Service Management. You can improve productivity and efficiency by delivering better self-service, recommending actions, and delivering answers. Now Assist for CSM was enhanced and updated in the Xanadu release.

## Now Assist for CSM highlights for the Xanadu release

Xanadu Patch 10: Enable security in Now Assist for CSM and AI agents and agentic workflows by enforcing access control lists \(ACLs\) and user identity-based permissions.

Xanadu Patch 9

-   Use case resolution steps to generate recommended actions based on the data clusters from previously closed cases.
-   Use enhanced AI agents and new standalone AI agents for more specific tasks. For example, the Duplicate identifier AI agent identifies the duplicate interactions and cases from the customers and then consolidates the information.

Xanadu Patch 7: Improve agent productivity by managing long running cases with the Triage cases AI agent use case.

-   Enhance customer conversations by receiving relevant contextual recommendations in real time.
-   Help improve productivity and decrease errors by the automatic generation of emails that can be verified and sent by the agent.
-   Consolidate information from multiple similar cases and bring it all together into a knowledge base article.
-   Summarize records to make it easier to hand off calls between agents and help improve customer satisfaction.

See [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Customer Service Management \(CSM\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Triage cases agentic workflow security directives](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Implement security on AI agents and agentic workflows through ACLs and user identities.

-   **[Now Assist for CSM Gen AI security directives](https://www.servicenow.com/docs/access?context=now-assist-csm-configuring&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Implement security in Now Assist for CSM skills through ACLs and user identities.


Xanadu Patch 9

-   **[Suggested steps in Recommended Actions](https://www.servicenow.com/docs/access?context=suggested-steps-generation-in-now-assist-for-customer-service-management-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use Recommended Actions to generate suggested resolution steps for cases. You can increase agent productivity by outlining the next best actions for unfamiliar cases and automatically providing logical next steps.

-   **[Triage cases agentic workflows enhancements](https://www.servicenow.com/docs/access?context=case-resolving-use-case&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Added new standalone AI agents to check duplicate cases and split some existing standalone AI agents to focus on more specific tasks. The AI agents available are the Triage cases planner AI agent, Context validator and analyzer agent, Duplicate identifier AI agent, Informational queries AI agent, Transactional queries AI agent, Case creation AI agent, Entity extraction AI agent, Document verification AI agent, and Email response AI agent.


Xanadu Patch 7

-   **Triage cases AI agents use case**

    Use the Triage cases AI agents use case to improve agent productivity through faster assessment.

    |AI agent use case|Description|
    |-----------------|-----------|
    |Triage cases|Use AI agents to handle all routine cases coming in through email and other offline channels, so that it improves customer satisfaction and reduces resolution times.|

-   **[Summarizing sidebar conversations](https://www.servicenow.com/docs/access?context=summarize-sidebar-conversations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use Now Assist for CSM to summarize sidebar discussions between agents, requesters, and subject matter experts.

-   **[Real-time chat reply recommendations](https://www.servicenow.com/docs/access?context=generate-chat-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Use generative AI to provide the agent with relevant contextual recommendations from sources such as knowledge bases, FAQs, similar cases, chats, and calls before they respond to the customer. Agents can also write a chat response with the help of generative AI. This feature helps agents stay focused on conversations with customers instead of doing manual tasks.

-   **[Generative AI-powered email reply recommendations](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Get recommendations for email responses that can be reviewed and sent by agents. Agents can also edit email replies recommendation with the help of generative AI.

-   **[Multilingual support for Now Assist for CSM skills](https://www.servicenow.com/docs/access?context=now-assist-csm-supporting-info&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Large language model \(LLM\) now supports the following languages across all skills in Now Assist for CSM: German, French, Japanese, Dutch, and French Canadian, Spanish, Brazilian Portuguese, and Italian.


## Changed in this release

-   **[Enhancement in post-call summarization](https://www.servicenow.com/docs/access?context=summarize-a-call-by-using-now-assist-for-customer-service-management-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**
    -   You can now review a call that has been handed off from one live agent to another agent, and then provide a summary of the key topics that are covered during the conversation.
    -   Support for outbound calls from agents to the customers.
    -   Generate a call summary when the real-time transcript is not available.
-   **[Knowledge generation from multiple cases](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    You can now select and gather insights and data from multiple similar cases to draft an article by using Now Assist for CSM.

-   **[Enhancements in chat summarization](https://www.servicenow.com/docs/access?context=now-assist-csm-summarize-chat&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Multiple Language Support via Digital technology \(DT\) support and a new step in the guided flow that allows the customization of how and when the skill capability will be available in the admin console.

-   **[Enhancements in Email recommendation](https://www.servicenow.com/docs/access?context=generate-email-reply-recommendations&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Get recommendations for email responses when starting new emails, forwarding messages, or finalizing drafts. Help improve agent productivity by reducing the time taken to compose email and improve relevance of email reply recommendations. Also, get template recommendations while composing an email by leveraging AI search.

-   **[Enhancement in Resolution notes generation](https://www.servicenow.com/docs/access?context=now-assist-csm-generate-resolution&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Generate resolution notes and then shorten or elaborate the content using the Now Assist context menu in the resolution notes field of the case form, in both Core UI \(UI16\) and Workspace.

-   **[Enhancements in Knowledge generation](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-csm-workspace&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Revise the content in existing knowledge articles by using the Now Assist icon ![](../../common/image/icon-ai-sparkle.png), which is accessible as an inline capability, and create and refine knowledge articles. You can also generate knowledge articles in multiple languages.

-   **Xanadu Patch 7 Case summarization enhancement**

    Extended the capabilities of the case summarization feature so it can now be used on custom tables.


## Activation information

Now Assist features are available with activation of the Now Assist for CSM plugin. For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Starting with Vancouver Patch 4, Now Assist for CSM is supported.

Starting with Xanadu Patch 7, Customer Service Management AI agent collection is supported.

## Additional requirements

The Now Assist for CSM application requires a Customer Service Management Pro Plus or Enterprise Plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

