---
title: Summarize an email interaction
description: Use ServiceNow Otto to generate an AI summary of an email interaction, giving agents a concise overview of customer issues, conversation context, and action items without reading through entire email threads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/summarize-email-interaction-eaai.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [summarize email interaction, AI summary, email interaction]
breadcrumb: [Using Email Interaction for CSM, Customer communication, Use, Customer Service Management]
---

# Summarize an email interaction

Use ServiceNow Otto to generate an AI summary of an email interaction, giving agents a concise overview of customer issues, conversation context, and action items without reading through entire email threads.

## Before you begin

Verify that ServiceNow Otto for Customer Service Management is installed and the AI summarization skill is activated. For activation steps, see [Activate email interaction summarization for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-email-summarization-csm.md).

Role required: sn\_customerservice\_agent

## About this task

Email interactions can contain lengthy conversation threads with multiple participants and complex customer issues. The AI summarization feature analyzes email content and generates structured summaries that highlight key information and action items, helping agents quickly understand the interaction context.

**Note:** AI-generated summaries may not capture all nuances of human communication. Agents must review summaries for accuracy.

## Interaction states and summary display

The Summarize this interaction section displays differently depending on the interaction state:

-   **__New__**

    The Summarize this interaction section appears with a **Summarize** button. No summary has been generated yet. Select **Summarize** to generate the summary.

-   **__Work in Progress__**

    If a summary has already been generated, the Interaction Summary card displays automatically showing components such as Issue, Key Actions Taken, and Next Steps. Select the refresh icon to regenerate the summary if the email thread has changed.

-   **__Closed__ or __Closed Complete__**

    The Interaction Summary card displays the last generated summary. The Check AI-generated content for accuracy message appears below the summary with thumbs-up and thumbs-down feedback controls.


## Procedure

1.  Navigate to **Customer Service** &gt; **Email Interactions** &gt; **All**.

2.  Open the email interaction record that you want to summarize.

3.  Select **Summarize**.

    The AI-generated summary appears, displaying key conversation points, customer issues, and action items.

4.  Review the summary and complete any of the following actions.

    -   **View AI disclaimer information:** Select the information icon next to **Email interaction summarized by ServiceNow Otto** to view the disclaimer.
    -   **Expand or collapse the summary:** Select **View less** to partially collapse the summary or **View more** to expand it.
    -   **Copy the summary:** Select the copy icon to copy the summary content to your clipboard.
    -   **Provide feedback:** Select the helpful icon for positive feedback or the not helpful icon if the summary was not useful.
    -   **Regenerate the summary:** Select the refresh icon to regenerate the summary if email interaction data has changed since the original summary was created.

## Result

The AI summary provides a structured overview of the email interaction, including customer issues, key conversation points, action items, and resolution status, helping agents respond to customer issues more efficiently.

## What to do next

The summary reflects interaction data at the time of generation. As the email interaction progresses with new messages or updates, regenerate the summary to capture the latest information.

