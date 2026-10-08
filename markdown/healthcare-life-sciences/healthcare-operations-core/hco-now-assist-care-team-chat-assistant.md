---
title: Care Team Operations AI Chat Assistant
description: Care Team Operations ships a dedicated ServiceNow Otto assistant, pre-configured for Care Team Operations workflows, instead of relying on the shared default assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-care-team-chat-assistant.html
release: brazil
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
breadcrumb: [Explore, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Care Team Operations AI Chat Assistant

Care Team Operations ships a dedicated ServiceNow Otto assistant, pre-configured for Care Team Operations workflows, instead of relying on the shared default assistant.

The **Care Team Operations AI Chat Assistant** is a dedicated ServiceNow Otto assistant built specifically for Care Team Operations. Unlike the shared default Virtual Agent assistant, it surfaces only Care Team Operations agents and search results, so care team members aren't shown unrelated catalogs, topics, or general enterprise content.

The assistant, its AI agents, and its voice agent all ship inactive. An administrator must activate each one before care team members can use them. See [Activate the Care Team Operations AI Chat Assistant and agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-activate-cto-assistant.md).

## Agents in the assistant

|Agent or workflow|Purpose|
|-----------------|-------|
|Care team operations case intake AI agent|Collects issue details for one or more requests in a single conversation and summarizes them for confirmation.|
|Care team operations case creation AI agent|Looks up service definitions and creates the confirmed case or cases in the appropriate domain table.|
|Request care team assistance|The agentic workflow that wraps case intake and case creation into a single conversational entry point. Added to the assistant as a Promoted Asset.|
|Care Team Operations Case Creation AI voice agent|Enables the same case creation flow over a phone call. See [Activate the Care Team Operations Case Creation AI voice agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/healthcare-operations-core/hco-now-assist-activate-voice-agent.md).|

Access to these agents and this workflow requires the `sn_hco.care_team_member` or `sn_hco.care_team_manager` role. These role requirements are unchanged from the shared assistant.

## How it works

When a care team member describes a request, the case intake AI agent asks clarifying questions until it has the details it needs, such as when information is missing or ambiguous. It then summarizes the request or requests and asks the user to confirm them. After the user confirms, the intake agent passes the request to the case creation AI agent, which creates the case in the appropriate Care Team Operations application. The user receives a confirmation that includes the case number.

## Mobile availability

If Care Team Mobile \[com.sn\_cto\_mobile\] is installed, the assistant is automatically extended to Care Team Mobile with its own nav-tab channel and pre-configured suggestion groups. No additional administrator configuration is required for mobile availability beyond activating the assistant and its agents.

