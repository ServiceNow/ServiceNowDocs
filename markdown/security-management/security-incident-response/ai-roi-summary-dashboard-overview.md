---
title: Security Incident AI ROI Summary dashboard overview
description: The Security Incident AI ROI Summary dashboard derives its values from Platform Analytics indicators and an estimation framework rather than from live queries. Knowing how each metric is calculated helps you interpret the time, monetary, and adoption figures that the dashboard reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/ai-roi-summary-dashboard-overview.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 5
keywords: [AI ROI dashboard, value realization, time saved, AI adoption, assist consumption, Now Assist for Security Incident Response]
breadcrumb: [View SIR Workspace Dashboards, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident AI ROI Summary dashboard overview

The Security Incident AI ROI Summary dashboard derives its values from Platform Analytics indicators and an estimation framework rather than from live queries. Knowing how each metric is calculated helps you interpret the time, monetary, and adoption figures that the dashboard reports.

## How the dashboard collects data

Every widget on this dashboard reads from a Platform Analytics indicator rather than from a live query. Indicators collect on a schedule, so the dashboard reflects data as of the last collection rather than the current moment.

Indicator collection is filtered by the derived scope of the application that a skill or agentic workflow originates from. A capability delivered from a scope that isn't included in the indicator source filters doesn't appear on this dashboard.

**Note:**

The AI usage log tables that these indicators read from are subject to platform data cleaners. The dashboard can't report on periods older than the platform retention window.

## How the dashboard estimates time and monetary value

Values on the **Value and time saved** tab come from a framework that estimates how long an analyst would take to produce the same output manually. The framework runs for each skill execution and derives its estimate in the following sequence.

1.  Count the words in the prompt sent to the skill and the words in the response that the skill returns.
2.  Convert the word counts to minutes by applying the standard reading velocity and writing velocity.
3.  Multiply the result by the complexity factor assigned to that skill.
4.  Add the per-execution values for every skill execution in the selected date range.

The complexity factor accounts for skills whose manual equivalent involves more than reading and writing. For example, producing recommended actions manually requires locating knowledge articles and gathering related context, so it carries a higher factor than summarizing a record. The factors are listed in the following table.

|Complexity level|Factor|
|----------------|------|
|Low \(default\)|1|
|Medium|1.25|
|High|1.5|

To convert time to monetary value, the framework converts the estimated time to hours and multiplies it by a default rate of $25 per hour. This rate is embedded in the formula indicator that computes **Dollars saved**.

**Note:**

Monetary values are estimates. A single rate applies to all users, and the dashboard doesn't apply different rates by analyst tier.

## Metric derivations

The derivation of each metric on the **Value and time saved** tab is described in the following table.

|Metric|Derivation|
|------|----------|
|Total time saved|Sum of the per-execution time estimates for every skill execution in the selected date range, shown in hours.|
|Dollars saved|Total time saved, converted to hours and multiplied by the default hourly rate.|
|Hours saved per user|Daily trend of the average number of hours saved per user in SIR.|
|Time saved per skill|Per-execution time estimates grouped by the skill that ran.|

The derivation of each metric on the **Adoption** tab is described in the following table.

<table id="table_roi_dash_adoption_derivation"><thead><tr><th>

Metric

</th><th>

Derivation

</th></tr></thead><tbody><tr><td>

Users using AI

</td><td>

Monthly trend comparing the total number of security users to the number of security users who have used Otto AI skills in SIR.

</td></tr><tr><td>

Daily unique users invoking AI

</td><td>

Daily trend of the number of unique users invoking Otto AI skills in SIR.

</td></tr><tr><td>

Top users by AI invocations

</td><td>

Count of Otto skill invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by user, ranked highest to lowest.

</td></tr><tr><td>

Top AI skills used

</td><td>

Count of Otto skill invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by the generative AI skill, ranked highest to lowest.

</td></tr><tr><td>

Top agentic workflows used

</td><td>

Count of agentic workflow invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by agentic workflow, ranked highest to lowest.

</td></tr><tr><td>

Invocations by team and skill

</td><td>

Invocation counts grouped by team, segmented by capability.

</td></tr><tr><td>

Adoption by team

</td><td>

Count of Otto credits consumed in SIR over a selected date range \(cumulative sum of daily counts\), broken down by team.

</td></tr><tr><td>

Total assists consumed

</td><td>

Aggregate sum of the assist value recorded on each skill and agentic workflow execution in the range.

</td></tr><tr><td>

Assist per active user

</td><td>

Total assists consumed divided by the number of distinct users who invoked an AI capability, calculated for each day.

</td></tr><tr><td>

Assist spend per skill

</td><td>

Total assists consumed, grouped by the skill that consumed them.

</td></tr><tr><td>

Assist spend per agentic workflow

</td><td>

Total assists consumed, grouped by the agentic workflow that consumed them.

</td></tr><tr><td>

Assist consumption by team

</td><td>

Count of Otto credits consumed in SIR over the selected date range \(cumulative sum of daily counts\), broken down by team.

</td></tr><tr><td>

Assists per resolved incident

</td><td>

Daily trend of the average number of Otto invocations per resolved security incident in SIR.**Note:** This value is a period average. Assist consumption isn't attributed to individual incidents.

</td></tr></tbody>
</table>## Change the hourly rate used for monetary values

The hourly rate is embedded in the formula indicator that computes **Dollars saved**. The rate isn't exposed as a system property and can't be read from a table record, so changing it requires editing the formula indicator.

1.  Navigate to the formula indicator.
2.  In the formula, update the hourly rate that your organization uses.
3.  Save the indicator.

## Override the time-saved computation for a custom skill

A customer-facing script include exposes the values that the time-saved framework uses. Extend this script include when your organization builds a custom skill whose manual equivalent doesn't match the default reading and writing model.

In that script include, you can do the following:

-   Override the default reading velocity and writing velocity.
-   Add your own complexity levels and complexity factors.
-   Supply your own time-saved computation for a specific capability.

**Related topics**  


[Review Security Incident AI ROI Summary dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/ai-roi-summary-dashboard.md)

