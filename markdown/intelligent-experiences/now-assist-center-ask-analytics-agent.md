---
title: AI Analytics Q and A agent
description: Use the AI Analytics Q and A agent to get answers about AI analytics metrics, dashboard widgets, and calculations by asking questions in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-center-ask-analytics-agent.html
release: zurich
topic_type: concept
last_updated: "2026-07-30"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using the ServiceNow Otto panel conversational experience, Use, AI Admin Center, Enable AI experiences]
---

# AI Analytics Q and A agent

Use the AI Analytics Q and A agent to get answers about AI analytics metrics, dashboard widgets, and calculations by asking questions in the ServiceNow Otto® panel.

## AI Analytics Q and A agent overview

The AI Analytics Q and A agent answers natural-language questions about AI analytics in AI Admin Center. When you ask an analytics-related question in the ServiceNow Otto panel or in ServiceNow Otto for Virtual Agent, the AI Analytics Q and A Workflow is triggered first. This LLM-controlled agentic workflow has a single step that calls the AI Analytics Q and A agent to generate a response.

**Note:** The AI Analytics Q and A agent is not listed in AI Admin Hub under AI skills. It is built into the ServiceNow Otto conversational experience and is not available for separate configuration. The agent does not consume any assists from your entitlements.

The AI Analytics Q and A agent may work with other AI agents to accomplish tasks. For more information on AI agents, see [AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/na-ai-agents.md).

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

1.  Ask a question about AI analytics dashboards using the panel or in ServiceNow Otto for Virtual Agent, for example, what a metric means or how a KPI is calculated.
2.  The AI Analytics Q and A Workflow is triggered. This LLM-controlled agentic workflow evaluates your question and calls the AI Analytics Q and A agent.
3.  The AI Analytics Q and A agent searches AI analytics content and displays a response.
4.  Review the response. Ask follow-up questions to get more detail.

**Parent Topic:**[Using the conversational experience in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/using-now-assist-panel-now-assist-center.md)

