---
title: Incident assist agentic workflow
description: Use the Incident assist agentic workflow to get answers to questions about an incident, including caller assets, recent incidents, similar resolved incidents, and on-call experts.
locale: en-US
release: australia
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Now Assist, Agentic AI, generative AI, Gen AI]
breadcrumb: [ITSM, Use agentic AI in IT Service Management, Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Incident assist agentic workflow

Use the Incident assist agentic workflow to get answers to questions about an incident, including caller assets, recent incidents, similar resolved incidents, and on-call experts.

**Important:** The Incident assist agentic workflow is active by default and includes all the capabilities of the \[DEPRECATED\] Incident assist skill, with enhancements. If you have the \[DEPRECATED\] Incident assist skill activated, consider deactivating it to avoid redundancy.

To deactivate the skill:

1.  Navigate to **Admin** &gt; **Now Assist Admin**.
2.  Select the **Now Assist Skills** tab.
3.  Go to **Technology** &gt; **ITSM**.
4.  Select the Ask questions about an incident by using the Now Assist panel skill.
5.  Select **Deactivate skill**.

For more information, see [Incident assist skill](../task/now-assist-itsm-incident-assist.md)

As an IT support agent, use the Incident assist agentic workflow to ask questions about an incident. Based on your question, the workflow routes to the appropriate specialist AI agent, which retrieves data from the incident record and related tables and returns a direct answer in the Now Assist panel.

The Incident assist agentic workflow is available by default.

**Note:** To modify the Incident assist agentic workflow, duplicate it and adjust the settings to meet your requirements.

## Incident assist agentic workflow overview

The Incident assist agentic workflow uses a team of specialist AI agents, each responsible for a specific category of incident-related questions. When you ask a question, the workflow parses your intent, retrieves the incident context, and routes to the appropriate agent. The agent queries the relevant data, formats the response, and returns it to you. You can ask follow-up questions or request a different topic without starting over.

The workflow supports the following types of queries:

-   Questions about the incident record itself, including status, SLA breach risk, related changes, outages, and CI details.
-   Caller's hardware assets assigned to the incident caller.
-   Caller's recent incidents from a configurable time period.
-   Similar resolved incidents found using semantic search.
-   On-call experts for the incident's assignment group.

When the workflow is triggered, it evaluates the incident context and routes to agents based on your query.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Incident assist**.

## AI agents used in the Incident assist workflow

The Incident assist agentic workflow consists of the following specialist agents.

**Note:** All agents return 10 records at a time. You can continue through results or ask a new question at any point.

|AI agent name|AI agent role|
|-------------|-------------|
|Incident context AI agent|Answers questions about the incident record and related data including SLAs, CIs, changes, outages, problems, and child incidents.|
|Additional incident context AI agent|Retrieves information based on on-call experts, callers recent incidents, caller's hardware assets, similar resolved incidents.|

## How the Incident assist agentic workflow works

Here's the workflow sequence when you ask a question in the Now Assist panel on an incident record.

|Steps|Task|Description|
|-----|----|-----------|
|1|Parse user input|Classifies your intent. If a query is detected, proceeds to routing. If not, presents options: incident details, caller's hardware assets, caller's recent incidents, similar resolved incidents, and on-call experts.|
|2|Get incident context|Extracts the incident number from the page context. If unavailable, prompts you to provide one.|
|3|Route to agents|Invokes one or more specialist agents based on your query. If your question spans multiple areas, multiple agents can be invoked in a single turn.|
|4|Continue or exit|After the agent responds, asks if you need anything else. If yes, returns to step 1. If no, the conversation ends.|

## Incident agentic workflow output

In the agentic workflow record:

1.  Review the information in the each screen, make any necessary updates and then select **Save and Continue**.
2.  In the Select channels and status screen, select **Save and test**.

    The agent executes the request for the agentic workflow.


**Example of Incident assist agentic workflow output with the Incident context AI agent in the ServiceNow AI Agent Studio**![Incident context AI agent in the Incident assist agentic workflow](../image/now-assist-itsm-incident-assist-inc-context-ai-agent.png)

**Example of Incident assist agentic workflow output with the Additional incident context AI agent in the ServiceNow AI Agent Studio**![Additional Incident context AI agent in the Incident assist agentic workflow](../image/now-assist-itsm-incident-assist-add-inc-context-aiagent.png)

In the AI Agent Studio, the human agent gets notified as soon as the recommendations to resolve incidents get generated so that they can follow the on-screen instructions and complete the task. For more information, see [Request the generative AI capabilities in ITSM by using the Now Assist panel](../task/request-gen-ai-capabilities-itsm-now-assist-panel.md).

## Generating answers to user questions in the Now Assist panel

As a user, follow these steps in the Now Assist panel. You need the itil role to access this workflow in the Now Assist panel.

**Note:** The Incident assist agentic workflow loads automatically with the current incident in context when you open the Now Assist panel on an incident record.

1.  Open an incident record in Service Operations Workspace or in the Core UI and select the Now Assist panel icon.

    The Incident assist workflow loads automatically with the current incident in context.

2.  Type a free-text question, for example, **What hardware does this caller have?** or **Who is on call for the Network Support group?**and select one of the available options that the agent presents.
3.  The agent routes your query to the appropriate sub-agent and returns results:
    -   **Incident context AI agent:** Routes to the Incident context details AI agent and returns incident fields, related records, and troubleshooting information.
    -   **Additional incident context AI agent:** Routes to the Additional incident context AI agent and returns hardware, recent incidents, similar resolved incidents, or on-call experts.
4.  After each response, the agent asks: **Need anything else about this incident?**

    You can do one of the following:

    -   Reply with another question to continue.
    -   Indicate that you're done to end the conversation.

To refine or ask a new question, do any of the following:

-   Ask about a different topic. For example, switch from assets to on-call experts.
-   Provide a different incident number or caller name to re-run the query.

The agent continues until you ask something outside its scope or end the conversation.

See examples of the screens for different use cases for this workflow in the Now Assist panel.

**Example of options available using the Incident assist agentic workflow in the Now Assist panel**![Example of options available using the Incident assist agentic workflow in the Now Assist panel](../image/now-assist-itsm-incident-assist-nap.png)

**Example of getting similar resolved incidents using the Incident assist agentic workflow in the Now Assist panel**![Example of getting similar resolved incidents using the Incident assist agentic workflow in the Now Assist panel](../image/now-assist-itsm-incident-assist-similar-incidents.png)

