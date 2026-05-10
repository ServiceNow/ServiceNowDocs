---
title: Configure Now Assist in Virtual Agent for ITSM
description: Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can provide an additional self-service tool.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Configure Now Assist in Virtual Agent for ITSM

Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can provide an additional self-service tool.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

Detect and mask sensitive data using the Sensitive Data Handler so it is not viewed by the agent or requester. For more information, see:

-   [Sensitive Data Handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ac-sensitive-data-overview.md)
-   [Configuring Sensitive Data Handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/agent-chat/ac-configure-sensitive-data-handling.md)

## About this task

The generative AI capabilities can provide a human-like catalog request experience over the Virtual Agent conversational interface. By using the generative AI capabilities with Virtual Agent, your organization can provide a conversational experience for request submissions.

Drive productivity by providing a virtual agent on familiar channels, such as Slack, Microsoft Teams, and Microsoft Copilot.

When you configure generative AI for catalog item request submissions, your requesters get the following experience:

-   Contextual question prompts that enable a more human-like conversation that is based on answers to previous questions.
-   Slot filling that recognizes the answers to one or more questions on the requester's input.
-   Ability to answer catalog item questions.
-   Ability to exit the request submission process at any point.

Although the following catalog item question types are supported in the conversation mode, natural language responses aren't supported for them:

-   Reference
-   Lookup select box
-   Lookup multiple choice
-   Requested For
-   Attachment
-   Multiple choice question with more than 10 choices

## Now Assist features supported in Now Assist for ITSM Virtual Agent

|Feature|Topic Reference|
|-------|---------------|
|Upload file formats such as text, PDF, Word \(.doc, .docx\) and image files such as JPEG and PNG.|[Upload documents in a chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/upload-documents-na-va.md).|
|Combine AI Search with generative AI chat skills to speed up issue resolution and reduce deflection to a live agent using Now Assist for ITSM in Virtual Agent.|[Enhanced chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/nava-enhanced-chat.md)|
|Use the structured and unstructured data from ServiceNow records, knowledge bases, and external sources to enhance the performance of Now Assist in Virtual Agent, AI agents, and generative AI skills using Knowledge Graph.|[Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md)|
|Define crawl settings for external content connectors to crawl source systems and send it to AI Search for indexing.|[Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ext-cont-connectors.md)|
|Monitor your device's performance and diagnose potential issues.|[Check device health using Now Assist for ITSM Virtual Agent](../../digital-end-user-experience/task/check-your-device-s-health-using-now-assist-for-itsm.md)|

## Procedure

1.  Turn on the required Virtual Agent skills: **Now Assist Multi-Turn Catalog Ordering**, **Now-Assist Q&amp;A Genius Results**, or **Now Assist Topics**.

2.  Set up Now Assist in Virtual Agent.

    For more information on how to turn on the skills and set up generative AI for Virtual Agent, see [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/now-assist-in-virtual-agent/configure-now-assist-va.md).

    **Note:**

    -   Configure the required conditions for the Virtual Agent skills.
    -   ITSM Virtual Agent is now replaced with the generative AI Virtual Agent.

