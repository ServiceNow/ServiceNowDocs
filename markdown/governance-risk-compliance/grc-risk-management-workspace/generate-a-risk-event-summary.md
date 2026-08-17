---
title: Generate an AI risk event summary in the classic UI
description: Generate an AI risk event summary using the ServiceNow Otto for IRM application. The approvers get the key insights to understand the context quickly, and reduce the time involved in creating summaries manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-risk-management-workspace/generate-a-risk-event-summary.html
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI in Risk Management, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Generate an AI risk event summary in the classic UI

Generate an AI risk event summary using the ServiceNow Otto for IRM application. The approvers get the key insights to understand the context quickly, and reduce the time involved in creating summaries manually.

## Before you begin

Install the ServiceNow Otto for IRM application to generate a risk event summary. For more information, see [ServiceNow Otto for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/now-assist-for-irm.md).

**Note:** The Risk Event Summarization skill is activated by default, unless you manually deactivate it. For more information, see [Activate AI skills in ServiceNow Otto for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/activate-na-skills-in-irm.md).

Role required: sn\_grc\_risk\_genai.risk\_event\_user

## About this task

The risk event summarization feature enables risk managers to quickly understand the context and key details of a risk event. This is helpful when multiple coordinators have been involved over time. It simplifies onboarding for new assignees and supports efficient decision-making for approvers, particularly in multi-level approval workflows, by providing concise, AI-generated summaries of each event.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **All Events**.

2.  Open the risk event that you want to create the risk event summary for.

3.  Generate a risk event summary from the risk event record page by selecting **Summarize**.

    \[Omitted image "risk-event-summarization-classic.png"\] Alt text: Generate risk event summarization button on the risk event record page.

    A summary is generated; you can edit it and save it for reference and reporting purposes.

4.  To edit and save the generated summary do the following:

    1.  Select **Share to summary** when the risk event is in New or Analyze state.

    2.  Make the necessary edits and select **Save to summary**.

    3.  Select **Share to work notes** for all other risk event states.

    4.  Make the necessary edits and select **Save to work notes**.

        The summary is saved in the **Summary** field when the risk event is in New or Analyze state, and in **Work notes** for all other states.


