---
title: Exploring Now Assist for Public Sector Digital Services \(PSDS\)
description: With the Now Assist for Public Sector Digital Services \(PSDS\) application, your agents can use generative AI to summarize the details and comment activity of each public service case to get the context of the case. They can also generate the case resolution notes to share with other agents.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Exploring Now Assist for Public Sector Digital Services \(PSDS\)

With the Now Assist for Public Sector Digital Services \(PSDS\) application, your agents can use generative AI to summarize the details and comment activity of each public service case to get the context of the case. They can also generate the case resolution notes to share with other agents.

The following generative AI capabilities are available for an agent:

-   A case summary enables an agent to gather the case context on long-running or complex cases. Because these cases can contain a lot of information, including the conversations with the constituent or other agents, an agent can generate a summary to gain understanding faster.
-   The case resolution notes can help an agent to wrap up cases faster and provide the context about the case resolution to the other agents who might encounter similar issues.

## Skills

The Now Assist for PSDS application includes the generative AI skills that enable your agents to understand the case context so that they can propose resolutions to the constituent or approve an application faster.

-   **Case summarization**

    Provides an agent with a summary of a public service case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context, refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The case summarization skill generates a case summary and displays it above the activity stream. The summary includes the information that the agent enters in the following case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Email
    -   Service level agreement \(SLA\)
    ![AI-generated case summary for a case record.](../image/now_assist_psds_case_summary.png "Case record with case summary")

-   **Resolution notes generation**

    Enables an agent to generate the resolution notes for a case, propose the resolution to the constituent or applicant, and add the information to the case record.

    The resolution notes generation skill displays a pop-up window that an agent can use to select a resolution code and review the resolution notes text before proposing a resolution to a constituent or relaying a decision to an applicant.

    **Note:** The resolution notes generation skill requires a minimum of 200 words in the case record to generate the resolution notes. If the resolution notes can't be generated, the system displays a message below the **Resolution notes** field.


## Now Assist panel in CSM Configurable Workspace

An agent can use the Now Assist panel in CSM Configurable Workspace. This conversational interface enables an agent to request a case summary and generate the case resolution notes. For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Now Assist in AI Search

The Now Assist in AI Search application uses Now LLM Service to extract actionable Q&amp;A Genius Result answers from the knowledge articles that are found in Service Portal, Virtual Agent, Employee Center, and global searches. By using this application, an agent can improve the customer's experience by retrieving the relevant content from the knowledge base and generating concise answers. For more information, see [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it does not appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service is not exposed to any sensitive information. For more information, see [Multi-turn catalog ordering](https://www.servicenow.com/docs/access?context=configure-sensitive-data-handling-for-generative-ai&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Related topics**  


[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

[Exploring Now Assist](https://www.servicenow.com/docs/access?context=exploring-now-assist-platform&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

