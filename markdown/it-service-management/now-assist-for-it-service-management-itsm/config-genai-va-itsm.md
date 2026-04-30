---
title: Configure Now Assist in Virtual Agent for ITSM
description: Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can provide an additional self-service tool.
locale: en-US
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Configure Now Assist in Virtual Agent for ITSM

Enable your requesters to have a streamlined, conversational experience that is based on generative AI as they submit a catalog item request in Virtual Agent. By offering this generative AI experience, your organization can provide an additional self-service tool.

## Before you begin

Role required: admin

Detect and mask sensitive data using the Sensitive Data Handler so it is not viewed by the agent or requester. For more information, see:

-   [Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-sensitive-data-overview&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)
-   [Configuring Sensitive Data Handler](https://www.servicenow.com/docs/access?context=ac-configure-sensitive-data-handling&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

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
|Upload file formats such as text, PDF, Word \(.doc, .docx\) and image files such as JPEG and PNG.|[Upload documents in Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=upload-documents-na-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).|
|Combine AI Search with generative AI chat skills to speed up issue resolution and reduce deflection to a live agent using Now Assist for ITSM in Virtual Agent.|[Enhanced chat](https://www.servicenow.com/docs/access?context=nava-enhanced-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)|
|Use the structured and unstructured data from ServiceNow records, knowledge bases, and external sources to enhance the performance of Now Assist in Virtual Agent, AI agents, and generative AI skills using Knowledge Graph.|[Knowledge Graph](https://www.servicenow.com/docs/access?context=knowledge-graph-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)|
|Define crawl settings for external content connectors to crawl source systems and send it to AI Search for indexing.|[Configuring External Content Connectors](https://www.servicenow.com/docs/access?context=configuring-ext-cont-connectors&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)|
|Monitor your device's performance and diagnose potential issues.||

## Procedure

1.  Turn on the required Virtual Agent skills: **Now Assist Multi-Turn Catalog Ordering**, **Now-Assist Q&amp;A Genius Results**, or **Now Assist Topics**.

2.  Set up Now Assist in Virtual Agent.

    For more information on how to turn on the skills and set up generative AI for Virtual Agent, see [Configuring Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

    **Note:**

    -   Configure the required conditions for the Virtual Agent skills.
    -   ITSM Virtual Agent is now replaced with the generative AI Virtual Agent.

