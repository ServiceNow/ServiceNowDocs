---
title: IT Service Management AI agent collection Who is On Call agentic workflow
description: Use the Who is On Call agentic workflow to retrieve on-call roster information for specific shifts, groups, or time periods. The agent provides accurate information to conversationally understand who is on-call.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-on-call-usecase.html
release: zurich
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI, On-Call Retrieval, On-Call Roster]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, ServiceNow Otto for IT Service Management \(ITSM\), IT Service Management]
---

# IT Service Management AI agent collection Who is On Call agentic workflow

Use the Who is On Call agentic workflow to retrieve on-call roster information for specific shifts, groups, or time periods. The agent provides accurate information to conversationally understand who is on-call.

## Who is On Call agentic workflow overview

Using the Who is On Call agentic workflow, retrieve on-call roster information to determine who is currently assigned to on-call duties. The agent performs the following tasks:

-   Validates user input for shifts, groups, and time periods
-   Resolves shift and group entities with fuzzy matching capabilities
-   Retrieves on-call member information with contact details
-   Supports date-range queries with automatic fallback mechanisms

The Who is On Call agent streamlines on-call roster queries by providing accurate, timezone-aware responses. This reduces manual lookups and ensures the correct on-call personnel are identified even across multiple shifts and groups.

To modify the Who is On Call agentic workflow, [duplicate it](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-aia-usecase.md), and adjust the settings according to your requirements.

**Important:** When you modify a use case, AI agent, or tool, make sure that you update all instructions accordingly.

## Who is On Call agentic workflow

Query on-call roster information to retrieve the current on-call member for a specified shift, group, or time period.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select the **Agentic workflows** tab.
3.  Select **Who is On Call**.

**Important:** The Who is On Call agent is available in the Otto Panel for Virtual Agent contexts. To enable the agent in other Virtual Agent contexts, verify that the agent has been added to the appropriate context profile skills.

## AI agents used in the Who is on call agentic workflow

The On Call Retrieval AI agent looks up on-call schedules, shifts, and rotations for any group and returns roster or coverage information. This agent is not enabled by default. You can enable it in the Select channels and status screen.

\[Omitted image "image.now-assist-itsm-who-is-on-call"\] Alt text: Who is on call Otto panel

