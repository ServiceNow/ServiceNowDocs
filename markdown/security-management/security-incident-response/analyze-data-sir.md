---
title: Analyze security incident data
description: Analyze and get insights into your security incident data using available prompts or natural language queries from the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/analyze-data-sir.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-11"
reading_time_minutes: 2
keywords: [data analysis, agentic workflow, security incident, natural language]
breadcrumb: [Use agentic workflows, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Analyze security incident data

Analyze and get insights into your security incident data using available prompts or natural language queries from the ServiceNow Otto panel.

## Before you begin

-   The ServiceNow Otto panel must be activated.

Role required: sn\_si.analyst or sn\_si.manager.

## About this task

**Important:** This agentic workflow is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

This agentic workflow answers questions about the data in Security Incident Response Core. The AI agent returns only the data that you're authorized to access. If you ask about data that your roles don't grant access to, the AI agent responds that it can't provide that information at your access level.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Select the ServiceNow Otto icon \[Omitted image "icon-ai-sparkle.png"\] Alt text:.

    The ServiceNow Otto panel is displayed.

3.  Select **Security Incident 360** in the panel.

    **Note:**

    The panel displays a limited number of agentic workflow tiles. If the tile isn't displayed, enter `Security Incident 360` in the search bar.

    Suggested questions are displayed in the panel.

4.  Enter your question in natural language or copy one of the suggested questions.

    The AI agent recognizes common alternatives, such as SIR for a security incident, and team for an assignment group.

    Request one action at a time. The AI agent can't combine requests.

    |Your request|Description|
    |------------|-----------|
    |Which assignment group has the most security incidents?|Aggregate security incidents across a field and identify the highest or lowest values.|
    |Show me all critical priority security incidents.|Return a filtered list of security incidents.|
    |Who are the users impacted by this security incident?|Return details for a specific security incident. Include the record number in your request.|

5.  Review the response, and then expand the **Sources** list.

    The **Sources** list identifies the data behind the response, including the table that the AI agent queried, the filter that it applied, and any aggregation that it performed.

    The entries in the **Sources** list are links to the matching lists of records.

6.  Enter a follow-up question in the same chat.

    The AI agent retains the context of your conversation within a single chat. For example, after you ask which users are impacted by a security incident, you can ask whether the same users are impacted by other security incidents.

    Your conversation is saved until you start a new chat. Start a new chat to clear the context of your previous questions, or return to your saved chat to continue. To start a new chat, select the new chat icon \[Omitted image "na-new-chat.png"\] Alt text:.


**Parent Topic:**[Using agentic AI workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-now-assist-ai-agents-sir.md)

