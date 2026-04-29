---
title: Using Now Assist for IT Service Management \(ITSM\) Generative AI skills
description: If you have the itil role, you can summarize the chat interactions with a requester, summarize an incident, and generate resolution notes by using the Now Assist for IT Service Management \(ITSM\) application. You can also understand the chat and incident context and propose resolutions more quickly to the requester.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Using Now Assist for IT Service Management \(ITSM\) Generative AI skills

If you have the itil role, you can summarize the chat interactions with a requester, summarize an incident, and generate resolution notes by using the Now Assist for IT Service Management \(ITSM\) application. You can also understand the chat and incident context and propose resolutions more quickly to the requester.

**Note:**

-   If you want a subset of users with itil role to access the Now Assist for IT Service Management \(ITSM\) skills, you can create a role or a group for those users. For more information, see [Create a new role or a group to access Now Assist skills](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2078019).
-   Some of the Now Assist for ITSM skills are now turned on by default. The skill will be automatically available to appropriate role users for the application.

    When new customers install a Now Assist product, designated skills are turned on automatically.

    **Note:** For existing users who upgrade, there will be no change to the skill activation.

    For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)


|Skill Name|Description|Link|
|----------|-----------|----|
|Chat summarization|Summarizes the Virtual Agent chat conversation between a live agent and a requester in Service Operations Workspace for ITSM.|[Summarize a chat conversation](../task/generate-chat-summary-interaction-now-assist-itsm.md)|
|Sidebar discussion summarization|Generates summaries of Sidebar chat discussions between agents, requesters, and subject matter experts.|[Summarize a sidebar discussion](../task/now-assist-itsm-sidebar-discussion.md)|
|Incident summarization|Generates summaries of incident details to quickly understand the incident context and respond to a requester's inquiries.|[Summarize an incident by using Now Assist for IT Service Management \(ITSM\)](../task/summarize-incident-now-assist.md)[Summarize an incident](https://www.servicenow.com/docs/bundle/zurich-it-service-management/page/product/now-assist-itsm/task/summarize-incident-now-assist.html)|
|Incident reassignment summarization|Provides information about the incident when assigning it to another agent or assignment group by summarizing all actions until hand off.|[Summarize an incident on reassignment](../task/reassign-incident-now-assist-itsm.md)|
|Change request summarization|Quickly captures the important details of a change request including the current status.|[Summarize a change request](../task/summarize-change-now-assist.md)|
|Change request risk explanation|Explains the risk assessment of a change request to help agents understand potential impacts.|[Explain a change request risk](../task/change-risk-exp-now-assist.md)|
|Resolution notes generation|Automatically generates the resolution notes for an incident on demand using the Now Assist context menu \(NACM\).|[Generate the resolution notes](../task/resolve-incident-now-assist.md)|
|Knowledge article generation|Creates knowledge articles from incidents to help deflect future similar issues.|[Generate a knowledge article](../../knowledge-management/task/Now-Assist-generate-article-SOW-itsm.md)|
|Chat reply recommendation|Generates a reply based on the context of the chat conversation using the Now Assist icon.|[Generate a chat reply recommendation](../task/now-assist-itsm-chat-recommendation.md)|
|Email response generation|Generate an email as a recommendation based on the context of the incident using the Now Assist icon.|[Generate an email response](../task/now-assist-itsm-email-recommendation.md)|
|Major Incident email recommendation|Creates a draft version of an email to communicate with stakeholders on a major incident using an email template.|[Generate a Major Incident email recommendation](../task/now-assist-itsm-mim-email-recommendation.md)|
|Incident Q&amp;A|Allows agents to obtain common incident-related information conversationally to get quick answers.|[Ask questions on an incident](../task/now-assist-itsm-incident-assist.md)|
|Generative AI capabilities request|Enables users to request contextual generative AI capabilities such as a chat summary, incident summary, or incident resolution notes in a conversational manner.|[Request generative AI capabilities](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md)|
|Incident deflection with self-service|Deflects incidents by providing self-service solutions.|[Deflect an incident with self-service](../task/deflect-incidents-now-assist-itsm.md)|
|Sentiment analysis|Enables users to make informed decisions on incidents based on requester's sentiment and the reasoning behind it.|[Analyze sentiments](../task/sentiment-analysis-now-assist-itsm.md)|
|Suggested steps generation|Generates suggested steps automatically by analyzing clusters of closed incidents with similar incident resolution.|[Generate suggested steps](../task/resolution-steps-generation-now-assist-itsm.md)|
|Activity stream response generation|Automatically generates a response in an incident record activity stream.|Generate a response in the activity stream|
|Release notes generation|Generates structured release notes for a release using AI-driven summarization.|[Generate release notes for a release](../task/now-assist-itsm-dpr-generate-release-notes.md)|
|Investigating Zoom call issues|Investigates zoom call quality issues.|[Investigate Zoom call issues](../../digital-end-user-experience/task/investigate-and-resolve-zoom-call-issues.md)|
|Investigating Zoom call issues|Investigates boot time issues|[Investigate boot time issues](../../digital-end-user-experience/task/investigate-and-resolve-boot-time-issues.md)|

