---
title: AI Analytics Q and A agent
description: Use the AI Analytics Q and A agent to get answers about AI analytics metrics, dashboard widgets, and calculations by asking questions in the Now Assist panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-ask-analytics-agent.html
release: zurich
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Monitor, Now Assist Center, Enable AI experiences]
---

# AI Analytics Q and A agent

Use the AI Analytics Q and A agent to get answers about AI analytics metrics, dashboard widgets, and calculations by asking questions in the Now Assist panel.

## AI Analytics Q and A agent overview

The AI Analytics Q and A agent answers natural-language questions about AI analytics in Now Assist Center. When you ask an analytics-related question in the Now Assist panel or in Now Assist in Virtual Agent, the AI Analytics Q and A Workflow is triggered first. This LLM-controlled agentic workflow has a single step that calls the AI Analytics Q and A agent to generate a response.

**Note:** The AI Analytics Q and A agent is not listed in Now Assist admin under Now Assist skills. It is built into the Now Assist conversational experience and is not available for separate configuration. The agent does not consume any assists from your entitlements.

The AI Analytics Q and A agent may work with other AI agents to accomplish tasks. For more information on AI agents, see [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-agents.md).

Responses from the AI Analytics Q and A agent are generated using AI and may be inaccurate or incomplete. Review a response before you act on it.

## Agent uses

Use the AI Analytics Q and A agent to ask about topics such as:

-   KPI definitions in AI analytics dashboards, such as CSAT, deflection rate, and so on.
-   How a dashboard widget or metric is calculated
-   Data flows and processing context for AI analytics
-   Deflection log states and common deflection scenarios
-   Changes to AI analytics dashboards between releases, such as updated or removed indicators and new dashboards

## Access requirements

Role required: sn\_na\_analytics.viewer

## How it works

1.  Ask a question about AI analytics dashboards using the Now Assist panel or in Now Assist in Virtual Agent, for example, what a metric means or how a KPI is calculated.
2.  The AI Analytics Q and A Workflow is triggered. This LLM-controlled agentic workflow evaluates your question and calls the AI Analytics Q and A agent.
3.  The AI Analytics Q and A agent searches AI analytics content and displays a response.
4.  Review the response. Ask follow-up questions to get more detail.

**Parent Topic:**[Monitoring in Now Assist Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-center-monitoring.md)

**Related topics**  


[Monitor your recently activated Now Assist solution in Now Assist Center]()

[View AI assets usage and performance in Now Assist Center]()

