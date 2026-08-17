---
title: Summarize an opportunity using ServiceNow Otto for Sales Automation
description: Generate an AI-powered summary of an opportunity in the CRM Workspace to get an immediate view of key details, customer needs, recent activity, and risks without reviewing multiple records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/now-assist-som-summarize-opportunity.html
release: australia
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 2
keywords: [opportunity summarization, generative AI]
breadcrumb: [Opportunity Management, Sales automation apps, Use, Sales Customer Relationship Management]
---

# Summarize an opportunity using ServiceNow Otto for Sales Automation

Generate an AI-powered summary of an opportunity in the CRM Workspace to get an immediate view of key details, customer needs, recent activity, and risks without reviewing multiple records.

## Before you begin

The opportunity summarization skill must be active before you can generate summaries. For more information, see [Customize the opportunity summarization skill in ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/customize-opportunity-summarization-skill-now-assist-som.md).

Role required: sn\_sfa.sales\_rep, sn\_sfa.sales\_manager

## About this task

Opportunity summary tile provides a synthesized summary of emails, meetings, touchpoints, work notes, and line items in a concise deal overview. Use opportunity summary to:

-   Understand the current state of a deal at a glance, without opening multiple records.
-   Surface the top customer needs and pain points identified across recent emails and meetings, with inline source attribution.
-   Review the most recent and upcoming activity on an opportunity in a single view.
-   Share deal context quickly by copying the summary or pushing it to work notes.
-   Keep summaries current by refreshing on demand to reflect the latest opportunity data.

## Procedure

1.  In the CRM Workspace, open the opportunity to summarize.

2.  Select the **Overview** tab.

    The Opportunity Snapshot panel appears and displays the AI-generated summary. The summary loads automatically when the page opens. Generating and displaying the summary may take several seconds.

3.  To generate a new summary, select **Summarize** in the Opportunity Snapshot panel.

    Use this option after significant updates to the opportunity, such as new emails, meetings, or changes to line items.

4.  After reviewing the summary, take any of the following actions.

    |Option|Procedure|
    |------|---------|
    |**Expand or collapse the summary**|Select the expand icon \[Omitted image "icon-expand.png"\] Alt text: or the collapse icon \[Omitted image "icon-collapse.png"\] Alt text: to show more or fewer summary details.|
    |**Provide feedback on the summary**|Select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: if the summary was useful, or the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: if it was not. This feedback helps improve the AI model for future summaries.|
    |**Copy the summary**|Select the copy to clipboard icon \[Omitted image "icon-copy.png"\] Alt text: to copy the summary text for use in another context, such as an email or a note.|
    |**View summary details**|Select the more info icon \[Omitted image "icon-more-info.png"\] Alt text: to check details about how the summary was generated.|

5.  Review the summary on the Opportunity summary card.

    An at-a-glance summary of key deal information includes:

    -   Deal size and scope \(number of users, contract value\)
    -   Most recent meeting with the Champion \(title and recency\)
    -   Most recent activity \(for example, a check-in email\) and when it occurred

## Result

The Opportunity snapshot card displays a structured summary with up to four sections: opportunity overview, customer needs and pain points, recent and upcoming activity, and risks detected from activity. Sections without data are not displayed.

**Parent Topic:**[Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-mgmt-using.md)

