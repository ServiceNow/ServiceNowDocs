---
title: Using Now Assist for Public Sector Digital Services \(PSDS\)
description: If you have an agent role, you can summarize the case details and generate the case resolution notes with the Now Assist for Public Sector Digital Services \(PSDS\) application.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Using Now Assist for Public Sector Digital Services \(PSDS\)

If you have an agent role, you can summarize the case details and generate the case resolution notes with the Now Assist for Public Sector Digital Services \(PSDS\) application.

Summarize the case details to help you understand the case context quicker. These summaries are useful for long-running or complex cases that include multiple conversations between agents and constituents.

Generate the case resolution notes to help wrap up cases faster. When you're ready to propose a solution to a constituent or relay a decision about their application, this feature can generate resolution notes and add them to the Case form. The resolution notes also provide the context about the case resolution to other agents who might encounter similar issues or cases.

Generate a summary of the Virtual Agent chat history and the chat conversation between a live agent and a customer by using the chat summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application.

Synthesize and summarize information from multiple KBs to deliver relevant answers in a conversational format using the Now Assist AI Search for CSM Workspace​ plugin​. This skill provides actionable AI-generated or AI-selected answers to a search in CSM Workspace, and can replace a list of possible findings with a single-turn conversational result.

## Skills

The Now Assist for PSDS application includes the generative AI skills that can enable your agents to understand the case context so that they can propose resolutions to the constituent or approve an application faster.

-   **Case summarization**

    Provides an agent with a summary of a public service case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context, refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The case summarization skill generates a case summary and displays it above the activity stream. The summary includes the information that the agent enters in the following case record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Email
    -   Service level agreement \(SLA\)
    ![AI-generated case summary for a case record.](../image/now_assist_psds_case_summary.png)

-   **Chat summarization**

    Provides an agent with a summary of a customer's Virtual Agent chat history, live agent chat history, and the interaction history. Agents can view or create the following summaries:

    -   Virtual Agent chat handoff summary: Summarizes the conversation when Virtual Agent hands off a chat to a live agent​ and displays the summary in the Active Chat window. An agent can view a summary of the actions that were taken by a customer before engaging with a live agent.
    -   Live Agent to Live Agent handoff summary: Summarizes the conversation when a live agent hands off a chat to another live agent​ and displays the summary in the Active Chat window. An agent can view a summary of the actions that were taken by a customer before hand off to another live agent.
    -   Quick action summary: Provides a summary when an agent uses the `/summarize` quick action in the Active Chat window.
    -   Chat wrap up summary: Populates the **Chat Summary** and **Short description** fields on the interaction record when a live agent wraps up a chat with a customer.

        **Note:** If a chat summary isn’t available for the interaction, the **Chat Summary** field doesn’t appear on the interaction record.

    ![AI-generated chat summaries for an interaction.](../image/chat-summary-now-assist-psds-pointer.png)

-   **Resolution notes generation**

    Can enable an agent to generate the resolution notes for a case, propose the resolution to the constituent or applicant, and add the information to the case record.

    The resolution notes generation skill displays a pop-up window that an agent can use to select a resolution code and review the resolution notes text before proposing a resolution to a constituent or relaying a decision to an applicant.

    **Note:** The resolution notes generation skill requires a minimum of 200 words in the case record to generate the resolution notes. If the resolution notes can't be generated, the system displays a message below the **Resolution notes** field.


**Related topics**  


[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

[Install and configure Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring.md)

[Using Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-using.md)

