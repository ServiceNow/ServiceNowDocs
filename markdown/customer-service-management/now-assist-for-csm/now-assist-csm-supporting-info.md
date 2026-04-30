---
title: Supporting information for Now Assist for Customer Service Management \(CSM\)
description: Get a quick overview of the important information that is related to the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist for CSM, Customer Service Management]
---

# Supporting information for Now Assist for Customer Service Management \(CSM\)

Get a quick overview of the important information that is related to the Now Assist for Customer Service Management \(CSM\) application.

## Supported versions

Now Assist for CSM is supported starting with Vancouver Patch 4.

## Supported language models

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Supported user interfaces

The Now Assist for CSM application includes the skills that are listed in the following table.

<table id="table_odd_d2y_wyb"><thead><tr><th>

Interface

</th><th>

Skill

</th></tr></thead><tbody><tr><td>

CSM Configurable Workspace

</td><td>

-   Chat summarization
-   Case summarization
-   Resolution notes generation
-   Knowledge article generation
-   Call summarization
-   Sidebar discussion
-   Chat recommendation
-   Email response
-   Sentiment analysis
-   Suggested steps generation
-   Sentiment analysis dashboard
-   Trending topics dashboard
-   Activity response generation

</td></tr><tr><td>

Core UI

</td><td>

-   Case summarization
-   Resolution notes generation
-   Knowledge article generation
-   Sentiment analysis
-   Activity response generation

</td></tr></tbody>
</table>## Languages supported

Now Assist for CSM supports the following languages across all skills:

-   German
-   French
-   Japanese
-   Dutch
-   French Canadian
-   Spanish
-   Brazilian Portuguese
-   Italian

For more info, see [Configure multilingual service for Now Assist applications](https://www.servicenow.com/docs/access?context=enable-dynamic-translation-for-now-assist-applications&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

## Role masking for Now Assist for CSM agentic workflows, AI agents, and skills

Role masking is used to restrict user access to agentic workflows, standalone AI agents, and skills. This ensures that users only receive the permissions necessary for their tasks, enhancing security and reducing the risk of unauthorized access.

**How Role Masking Works**

Imagine a user assigned roles A, B, and C, where each role grants access to a specific set of data. Normally, only if using Access Control Lists \(ACLs\), the user could access any data or functions available to roles A, B, and C. With role masking applied, the user can only access data tied to the active role, limiting exposure to unnecessary information.

**Role Masking Considerations for Now Assist in CSM Skills**

When a CSM skill runs, its features are initially controlled by ACL permissions, ensuring users only access authorized data and functions. If the skill uses a Large Language Model \(LLM\) to perform its task, role masking adds an extra layer of control by filtering the LLM-generated output according to the user’s active role.

Consider a user with roles A, B, and C, each granting different privileges. If the ACLs defined in the Case Summarization are roles A, B, and C and the masking role defined is role A, If the user activates the Case Summarization skill, and selects Summarize, the process occurs in two steps:

1.  **Data Retrieval**

    ACL permissions for role A are applied to fetch relevant case data. This ensures the user only sees data they are authorized to view.

2.  **Data Summarization**

    After data retrieval, an LLM summarizes the case. Role masking is then applied to the output, tailoring the summary to the access privileges defined for role A.


By applying both ACL permissions and role masking, the system ensures a secure and granular access control mechanism for CSM skills, protecting sensitive information while providing users with the insights they need to perform their tasks effectively. For information on role masking, see.

## AI color gradient support

Now Assist for CSM supports the AI color gradient across the following skills and workflows:

-   Case summarization
-   Resolution notes generation
-   KB generation
-   Call summarization
-   Sidebar discussion
-   Chat recommendation
-   Email recommendation
-   Sentiment analysis case
-   Suggested steps generation
-   Sentiment analysis dashboard
-   Trending topics dashboard
-   Now Assist context menu activities- tone and refining options

## Application information

Activate the Now Assist for CSM store app \(sn\_csm\_gen\_ai\) to use the chat and case summarization skills and to generate case resolution notes.

This store app has the following dependencies:

-   Customer Service \(com.sn\_customerservice\)
-   UXC Generative AI \(sn\_uxc\_gen\_ai\)

Activate the applications in the following order:

1.  Customer Service
2.  UXC Generative AI
3.  Now Assist for CSM

For more information, see [Configuring Now Assist for Customer Service Management \(CSM\)](now-assist-csm-configuring.md).

**Parent Topic:**[Exploring Now Assist for Customer Service Management \(CSM\)](now-assist-csm-exploring.md)

