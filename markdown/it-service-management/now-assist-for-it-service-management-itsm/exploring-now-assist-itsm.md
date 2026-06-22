---
title: Exploring Now Assist for IT Service Management \(ITSM\)
description: With the Now Assist for IT Service Management \(ITSM\) application, your agents can summarize the chat conversations and incident details, generate the incident resolution notes to share with other agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/now-assist-for-it-service-management-itsm/exploring-now-assist-itsm.html
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Exploring Now Assist for IT Service Management \(ITSM\)

With the Now Assist for IT Service Management \(ITSM\) application, your agents can summarize the chat conversations and incident details, generate the incident resolution notes to share with other agents.

## Now Assist for IT Service Management \(ITSM\) overview

The following generative AI capabilities are available for an agent:

-   An incident summary enables your agents to understand the incident context.
-   The incident resolution notes provide the context to other agents who might encounter similar incidents.
-   An interaction chat summary provides the context about the chat conversation to an agent by specifying all points of the handoff, including the Virtual Agent conversation.

## Now Assist for IT Service Management \(ITSM\) skills

The Now Assist for ITSM application includes the generative AI skills and features that enable your agents to understand the chat and incident context so that they can propose quicker resolutions to the requester.

-   **Chat summarization**

    Provides an agent with a summary of a requester's Virtual Agent chat history. An agent can also generate a summary of the entire interaction when the chat ends or when an incident is created for further troubleshooting before or after the chat ends.

    \[Omitted image "itsm-chat-summary.png"\] Alt text: Chat summarization for an interaction.

-   **Sidebar discussion summarization**

    Generates a summary of Sidebar discussions between agents, requesters, and subject matter experts using this skill. An agent can also post the summary to the incident work notes for further troubleshooting before or after the chat ends.

    \[Omitted image "now-assist-itsm-sidebar-discuss.png"\] Alt text: Sidebar discussion summarization.

-   **Incident summarization**

    Enables an agent to expedite the incident troubleshooting process by reviewing its summary that includes the issue, actions taken, and resolution. Your agent can generate an incident summary for active incidents to understand the incident context. Your agent can also refresh the summary, post the summary to the incident work notes, copy the summary, and provide feedback about the summary.

    The incident summary includes the information that an agent enters in the following incident record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Email
    \[Omitted image "incident-summary-now-assist.png"\] Alt text: Incident summary that specifies the issue and actions taken.

-   **Incident assist**

    Enables an agent to quickly obtain common incident related information conversationally within the incident record by asking questions related to the supported topics in the Now Assist panel.

    Incident assist topics supported in the Now Assist panel include:

    -   Caller's assets
    -   Caller's recent incidents
    -   On-call experts from support groups
    -   Similar resolved incidents
    \[Omitted image "now-assist-itsm-inc-assist-pan.png"\] Alt text: Incident assist panel in Service Operations Workspace in an incident.

-   **Change request summarization**

    Enables an agent to expedite the change request process by reviewing its summary that includes objective, plan, and risk. Your agent can generate a change request summary for active change requests to understand the change request context. Your agent can also refresh the summary, post the summary to the change request work notes, copy the summary, and provide feedback about the summary.

    The change request summary includes the information that an agent enters in the following incident record fields:

    -   Short description
    -   Description
    -   Work notes
    -   Additional comments
    -   Risk
    -   Impact
    -   Justification
    -   Implementation plan
    -   Risk and impact analysis
    -   Test plan
    -   Backout plan
    -   Close code
    -   Close notes
    -   Configuration item
    -   Service
    -   Service offering
    -   State
    -   Conflict status
    -   Type
    \[Omitted image "now-assist-change-summary.png"\] Alt text: Change request summary in Service Operations Workspace.

-   **Change request risk explanation**

    Enables an agent to understand the change request risk by reviewing the explanation for the risk rating. Your agent can generate a change request risk explanation for change requests that have a risk rating \(high, med, low\). Your agent can also copy the summary, and provide feedback about the summary.

    The change request risk explanation includes the information that an agent enters in the following incident record fields:

    -   Short description
    -   Implementation plan
    -   Assignment group
    -   Risk
    Additional inputs include: similar change requests and the incidents caused by those changes, and risk condition that was met.

    \[Omitted image "now-assist-chg-risk-explanation.png"\] Alt text: Change request risk explanation in Service Operations Workspace.

-   **Resolution notes generation**

    Automatically generates the resolution notes for an incident using the Now Assist icon and provides context to the other agents who might encounter similar incidents.

    \[Omitted image "itsm-resolution-notes-generation.png"\] Alt text: Resolution notes for an incident.

-   **Knowledge generation**

    Enables an agent to generate a knowledge article from an incident after proposing a resolution or closing the incident.

    The knowledge generation skill displays a pop-up window that an agent can use to generate a knowledge article and review it before publishing the knowledge article draft.

    \[Omitted image "now-assist-itsm-kb-gen-modal.png"\] Alt text: Now Assist in ITSM knowledge article choice modal.

-   **Chat reply recommendation**

    Enables an agent to generate a reply recommendation from a chat using the Now Assist icon.

    The chat reply recommendation skill displays a pop-up window that an agent can use to generate a recommendation and review it before sending it as a reply to the requester.

    \[Omitted image "now-assist-itsm-generate-reply.png"\] Alt text: Write with Now Assist chat reply recommendation.

-   **Release notes generation for a release in Digital Product Release**

    Enables a product manager to generate structured release notes for a release that is in the readiness phase.

    The Generate release notes skill uses artifacts in the release scope to generate the release notes that you can review it before publishing.\[Omitted image "dpr-release-notes-preview.png"\] Alt text: Release notes for a release generated using AI-driven summarization, in Digital Product Release Workspace.


## Now Assist panel in Service Operations Workspace for ITSM

An agent can use the Now Assist panel in Service Operations Workspace for ITSM. This conversational interface enables an agent to request a chat summary or incident summary and generate the incident resolution notes. For more information about the Now Assist panel, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md).

-   **[Supporting information for Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/supporting-information-now-assist-itsm.md)**  
Get a quick overview of the important information that is related to the Now Assist for IT Service Management \(ITSM\) application.

**Parent Topic:**[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)

**Related topics**  


[Exploring Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/exploring-now-assist-platform.md)

