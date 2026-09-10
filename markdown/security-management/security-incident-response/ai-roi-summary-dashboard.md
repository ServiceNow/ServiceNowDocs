---
title: Review Security Incident AI ROI Summary dashboard
description: The Security Incident AI ROI Summary dashboard displays time savings, monetary value, and adoption metrics for ServiceNow Otto capabilities. Use this dashboard to measure AI impact across your Security Incident Response team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/ai-roi-summary-dashboard.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 3
keywords: [AI ROI dashboard, value realization, time saved, AI adoption, Now Assist for Security Incident Response]
breadcrumb: [Security Incident AI ROI Summary dashboard overview, View SIR Workspace Dashboards, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Review Security Incident AI ROI Summary dashboard

The Security Incident AI ROI Summary dashboard displays time savings, monetary value, and adoption metrics for ServiceNow Otto capabilities. Use this dashboard to measure AI impact across your Security Incident Response team.

## Before you begin

Role required: sn\_si.admin or sn\_si.manager

## About this task

**Important:**

The **Generate summary** and **Insights** features use generative AI, which may produce inaccurate or incomplete information. Always validate AI-generated content.

The Security Incident AI ROI Summary dashboard provides two views of AI capability performance:

-   **Value and time saved**: Displays hours and monetary value saved by AI capabilities, both in total and per skill.
-   **Adoption**: Displays analyst usage patterns, capability invocation counts, and assist consumption metrics.

\[Omitted image "ai-roi-dash-value-dashboard.png"\] Alt text: Dashboard showing Value and time saved tab with widgets for total time saved, dollars saved, hours saved per user, and time saved per skill

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Select **SIR Dashboards**.

3.  Select **Security Incident AI ROI Summary** from the list of dashboards.

4.  In the **Select date range** filter, set the reporting period, then select **Apply**.

    All widgets on both tabs use the date range you apply.

    **Note:**

    The **Hours saved per user** and **Daily unique users invoking AI** widgets require at least one full calendar month in the selected range to display data.

5.  Select the **Value and time saved** tab to review productivity value delivered by AI capabilities.

    **Note:**

    Values on this tab cover skill executions only. Agentic workflow executions aren't included in the time and monetary estimates, although they do appear in the assist consumption metrics on the **Adoption** tab.

    The tab contains the following widgets:

    -   **Total time saved**: Total time saved from the skill invocations \(excludes agent interactions\) in SIR over the selected date range \(cumulative sum of daily totals\).
    -   **Dollars saved**: Total dollar value saved by Otto in SIR over the selected date range \(cumulative sum of daily totals\), based on time saved from skill invocations valued at $50/hour.
    -   **Hours saved per user**: Daily trend of the average number of hours saved by Otto per user in SIR.
    -   **Time saved per skill**: Total time saved from Otto skill invocations in SIR over the selected date range \(cumulative sum of daily totals\), broken down by which GenAI skill generated the savings.
6.  Select the **Adoption** tab to review AI capability usage across your team.

    The **Adoption** tab contains two sections. The first section reports the number of invocations for each capability. The second section, **How much AI is being consumed**, reports the number of assists consumed by those invocations.

    **Note:**

    An invocation is a single use of an AI capability. An assist is the licensed unit that an invocation consumes. One invocation can consume more than one assist.

    The invocation section contains the following widgets:

    -   **Users using AI**: Monthly trend comparing the total number of security users to the number of security users who have used Otto AI skills in SIR.
    -   **Top users by AI invocations**: Count of Otto skill invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by user, ranked highest to lowest.
    -   **Daily unique users invoking AI**: Daily trend of unique users who invoked an AI capability.
    -   **Top AI skills used**: Count of Otto skill invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by the generative AI skill, ranked highest to lowest.
    -   **Top agentic workflows used**: Count of agentic workflow invocations in SIR over the selected date range \(cumulative sum of daily counts\), broken down by agentic workflow, ranked highest to lowest.
    -   **Adoption by team**: Count of Otto credits consumed in SIR over a selected date range \(cumulative sum of daily counts\), broken down by team.
    The **How much AI is being consumed** section contains the following widgets:

    -   **Total assists consumed**: Cumulative assist count across all capability invocations.
    -   **Assist consumption by team**: Count of Otto credits consumed in SIR over the selected date range \(cumulative sum of daily counts\), broken down by team.
    -   **Assist spend per skill**: Total assist consumption by skill.
    -   **Assist spend per agentic workflow**: Total assist consumption by agentic workflow.
    -   **Assist per active user**: Daily trend of the average number of Otto invocations per active user in SIR.
    -   **Assists per resolved incident**: Daily trend of the average number of Otto invocations per resolved security incident in SIR.
7.  Select the **Dashboard details** icon to access dashboard configuration and sharing options.

8.  Select **Generate summary** to create an AI-generated summary of dashboard insights.

9.  Select **Refresh** to update dashboard data with the latest metrics.

10. Select **Insights** to view AI-generated recommendations based on dashboard data.


