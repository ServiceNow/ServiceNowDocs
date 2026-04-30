---
title: Generate a risk event summary in the classic UI
description: Generate a risk event summary using the Now Assist for IRM application. The approvers get the key insights to understand the context quickly, and reduce the time involved in creating summaries manually.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-08-19"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Generate a risk event summary in the classic UI

Generate a risk event summary using the Now Assist for IRM application. The approvers get the key insights to understand the context quickly, and reduce the time involved in creating summaries manually.

## Before you begin

Install the Now Assist for IRM application to generate a risk event summary. For more information, see [Now Assist for Integrated Risk Management \(IRM\)](../../grc-common/concept/now-assist-for-irm.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_grc\_risk\_genai.risk\_event\_user

## About this task

The risk event summarization feature enables risk managers to quickly understand the context and key details of a risk event, even when multiple coordinators have been involved over time. It simplifies onboarding for new assignees and supports efficient decision-making for approvers, particularly in multi-level approval workflows, by providing concise, AI-generated summaries of each event.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **All Events**.

2.  Open the risk event that you want to create the risk event summary for.

3.  Generate a risk event summary from the risk event record page by selecting **Summarize**.

    ![Generate risk event summarization button on the risk event record page.](../../grc-risk/image/risk-event-summarization-classic.png)

    A summary is generated; you can edit it and save it for reference and reporting purposes.

4.  To edit and save the generated summary do the following:

    1.  Select **Share to summary** when the risk event is in New or Analyze state.

    2.  Make the necessary edits and select **Save to summary**.

    3.  Select **Share to work notes** for all other risk event states.

    4.  Make the necessary edits and select **Save to work notes**.

        The summary is saved in the **Summary** field when the risk event is in New or Analyze state, and in **Work notes** for all other states.


