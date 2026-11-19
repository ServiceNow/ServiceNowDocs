---
title: Analyze response feedback on Virtual Agent responses
description: Review the response feedback, reasons, and comments that users give on ServiceNow Otto for Virtual Agent responses in the Virtual Agent Feedback Analysis dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/now-assist-in-virtual-agent/analyze-response-feedback-on-virtual-agent-responses.html
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: concept
last_updated: "2026-11-12"
reading_time_minutes: 4
keywords: [Virtual Agent Feedback Analysis, response feedback, Accepted, Rejected, free text feedback]
breadcrumb: [Analyzing assistants, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Analyze response feedback on Virtual Agent responses

Review the response feedback, reasons, and comments that users give on ServiceNow Otto for Virtual Agent responses in the Virtual Agent Feedback Analysis dashboard.

The Virtual Agent Feedback Analysis dashboard shows how users rate the responses that their assistants return. It reports the number of conversations and requests, the thumbs-up and thumbs-down ratings that users give, the reasons that they select, and the comments that they enter.

\[Omitted image "NAinVA-virtual-agent-feedback-analysis-dashboard.png"\] Alt text: Virtual Agent Feedback Analysis dashboard in Platform Analytics.

The visualizations on the dashboard provide the following insights.

-   The proportion of responses that users accept and reject indicates how well responses meet user needs.
-   The reasons that users select when they rate a response show which response qualities to improve.
-   The trend of feedback over time shows whether changes to your assistant affect user ratings.

## Feedback that users submit

When a user selects thumbs-up or thumbs-down on a response, the user can also select one or more reasons and enter an optional comment of up to 300 characters.

\[Omitted image "NAinVA-response-feedback-form.png"\] Alt text: Response feedback form with reasons, a comment box, and the Submit feedback button.

Feedback is recorded for a single response item, not for the whole request. Each feedback action is logged as a separate event. If a user changes their feedback on a response, only the most recent feedback is considered. Earlier records remain available, depending on your data retention settings.

## Access the dashboard

Role required: virtual\_agent\_admin or admin

Navigate to **Platform Analytics** &gt; **Dashboards** and search for **Virtual Agent Feedback Analysis**. For more information about opening and managing dashboards, see [Platform Analytics experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/par-workspace.md).

## Requirements

The dashboard reports on feedback that is stored in the Now Assist analytics tables. Before the dashboard shows data, verify that your instance meets the following requirements.

-   AI Analytics version 5.2.5 or later is installed.
-   The `sn_nowassist_va.analytics.persistence_strategy` system property is set to `table` or `both`. Set the property to `both` to keep the data already stored in the legacy table while also writing to the Now Assist analytics tables. If the property is set to `event`, the dashboard shows no data. For more information about the property and the tables that store feedback, see [Virtual Agent feedback data tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/virtual-agent-feedback-analysis-dashboard.md).
-   Response feedback is turned on for your assistant. For more information, see [Manage response feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/now-assist-in-virtual-agent/manage-sentiment-survey.md). To change the feedback options that users see, see [Configure response feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/nava-configure-response-feedback-manually.md).

The dashboard supports standard chat, enhanced chat, premium chat, and the full-page experience.

**Important:**

-   The dashboard shows no historical data. Data is collected only from the time that you set the `sn_nowassist_va.analytics.persistence_strategy` property to `table` or `both`.
-   Feedback is captured only for synthesized responses. Agentic responses don't support the feedback mechanism.
-   Responses in Microsoft Teams and Slack aren't supported.

## Filter the dashboard data

Use the **Date** filter to view the dashboard data for a specific date range. The filter applies to every widget on the dashboard.

## Dashboard widgets

-   **Total Virtual Agent Conversations**

    This area of the dashboard shows the total number of conversations in the selected date range. A conversation groups the individual requests that a user makes during an interaction with an assistant. Use this metric as the baseline for the feedback metrics.

-   **Total Virtual Agent Requests**

    This area of the dashboard shows the total number of user requests in the selected date range. A request is a single user utterance or API request that an assistant handles.

-   **Total Feedback**

    This area of the dashboard shows the total number of thumbs-up and thumbs-down ratings that users gave on responses in the selected date range.

-   **Total Granular Feedback**

    This area of the dashboard shows the total number of response feedback reasons that users selected when they rated a response in the selected date range. A single rating can include more than one reason.

-   **Total Free Text Feedback**

    This area of the dashboard shows the total number of comments that users entered when they rated a response in the selected date range.

-   **Free Text feedback distribution**

    This area of the dashboard shows how the comments that users entered divide between Accepted and Rejected ratings. Use this chart to see whether users comment more on responses that they accept or reject.

-   **Virtual Agent feedback distribution**

    This area of the dashboard shows the proportion of responses that users accepted and rejected in the selected date range. Accepted represents a thumbs-up rating and Rejected represents a thumbs-down rating. Use this chart to assess overall user satisfaction with assistant responses.

-   **Virtual Agent granular feedback distribution**

    This area of the dashboard shows the distribution of the reasons that users selected when they rated a response. Use this chart to identify the most frequently selected reasons and to prioritize improvements to responses.

-   **Virtual Agent feedback trend**

    This area of the dashboard shows the number of Accepted and Rejected ratings over the selected date range. Use this trend to identify changes in user satisfaction after you update your assistant, its knowledge sources, or its skills.

-   **Virtual Agent feedback trend**

    This area of the dashboard shows the number of response feedback reasons that users selected over the selected date range. Use this trend to identify reasons that increase or decrease over time.


