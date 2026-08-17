---
title: View opportunity scores and insights
description: Review AI-generated win probability scores and contextual insights for an opportunity to assess deal health without opening individual activity, contact, or deal records. Use this to prioritize pipeline opportunities and identify risks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/view-opty-scores-insights.html
release: australia
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 2
breadcrumb: [Opportunity Management, Sales automation apps, Use, Sales Customer Relationship Management]
---

# View opportunity scores and insights

Review AI-generated win probability scores and contextual insights for an opportunity to assess deal health without opening individual activity, contact, or deal records. Use this to prioritize pipeline opportunities and identify risks.

## Before you begin

Opportunity scoring jobs must be activated and the ML model must be trained on the existing data before sales agents can view AI-generated scores and insights. For more information, see [Set up ML-based opportunity scoring and insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/set-up-opty-score-insights.md).

Role required: sales\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Opportunity** &gt; **All**.

4.  Select an opportunity record for which you want to view insights.

5.  Select the **Overview** tab.

6.  Review the AI Win Probability score and insights information available on the Scores and Insights card.

    Opportunity scoring rates each open opportunity from 0 to 100 based on the patterns that a machine learning model finds in your closed deals. The score comes with plain-language insights that explain the factors behind it. Each score also maps to a rating that helps sellers triage their pipeline at a glance.

    |AI Win Probability|Rating|
    |------------------|------|
    |75 to 100|Healthy|
    |50 to 74|On Track|
    |25 to 49|At Risk|
    |0 to 24|Critical|

    -   AI Win Probability: A read-only score from 0 to 100 that the ML model calculates for each opportunity, representing the likelihood that the opportunity will close.
    -   Rating: A qualitative label derived from the AI Win Probability score that indicates the health of the opportunity at a glance. The **Rating** field is present on the Details tab. It updates automatically when the score changes and can be manually overridden by a sales representative.
    The Scores and Insights card also provides contextual, plain-language observations derived from opportunity signals, such as:

    -   Competitor activity detected in recent meetings
    -   Champion engagement patterns \(for example, being unresponsive, canceling demos\)
    -   Benchmarks against similar deals \(for example, "Opportunities with similar stall patterns have 35% lower close rate at this stage"\)
    \[Omitted image "opty-scores-insights.png"\] Alt text: Score and Insights card on the Overview tab of an opportunity record.

7.  Review the AI Win Probability and Score Reasons fields in the Activity stream.

    Score Reasons captures the plain-language rationale for each score computation. The system overwrites the previous rationale each time the model recalculates the score. This field is not shown on the opportunity form by default.


**Parent Topic:**[Using Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-mgmt-using.md)

**Related topics**  


[Summarize an opportunity using ServiceNow Otto for Sales Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-som-summarize-opportunity.md)

