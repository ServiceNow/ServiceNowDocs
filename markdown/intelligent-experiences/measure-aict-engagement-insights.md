---
title: Engagement dashboard
description: The Engagement dashboard provides visibility into AI system usage patterns across your organization, including adoption metrics, department usage, and system adoption by geographic region.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-aict-engagement-insights.html
release: australia
topic_type: concept
last_updated: "2026-08-02"
reading_time_minutes: 4
breadcrumb: [Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Engagement dashboard

The Engagement dashboard provides visibility into AI system usage patterns across your organization, including adoption metrics, department usage, and system adoption by geographic region.

The Engagement dashboard displays aggregated data about LLM-related actions and AI system usage across your enterprise. Use this dashboard to monitor AI adoption trends, identify systems that require attention, and understand usage patterns by department and location.

To view the Engagement dashboard AI Control Tower, navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Engagement**.\[Omitted image "aict-engagement-dashboard.png"\] Alt text: View the Engagement dashboard and the different usage patterns.

**Note:** All metrics on the Engagement dashboard default to the last 30 days. Use the time period selector in the top-right corner to adjust the date range and view metrics for different time periods \(for example, last 7 days, last 90 days, or a custom range\).

## Total AI actions

Displays the total number of LLM-related actions performed across all AI systems during the selected time period. This metric includes a comparison to the previous period, expressed as a percentage change.

The Total AI actions display:

-   The aggregated cost across all deployed AI systems.
-   Percentage change relative to the previous period.
-   A trend line about the daily sum of actions over the selected date range, allowing you to identify patterns and spikes in the system usage over time.

## AI systems with no usage

Lists AI systems that were not used during the selected time period. This section helps you identify systems that may require user outreach, enablement, or evaluation for continued relevance.

Systems are displayed by name; select a system name to drill into additional details.

-   **ApprovalChecklistGeneration**

    The engagement record that tracks the deployment status, lifecycle, and business value of AI system implementations. It measures productivity gains, net AI returns, and conformance metrics to help organizations monitor the impact and cost-effectiveness of their AI investments.

    Select ApprovalChecklistGeneration to see the metric cards that track productivity gains, financial returns, AI actions, and cost-related data for the engagement. All metrics are aggregated over a configurable time period, with a default view of the last 30 days.

    **Note:** Selecting ApprovalChecklistGeneration leads you to the ApprovalChecklistGeneration page opening the **Value &amp; engagement** tab.

-   **Automation Finder**

    The AI engagement record that identifies and tracks automation opportunities within an organization. It measures the productivity gains, cost savings, and AI-driven value realized from automation discovery and implementation, while monitoring deployment status, risk levels, and conformance requirements.

    Select Automation Finder to see the metric cards that track productivity gains, financial returns, AI actions, and cost-related data for the automation discovery and implementation. All metrics are aggregated over a configurable time period, with a default view of the last 30 days.

    **Note:** Selecting Automation Finder leads you to the Automation Finder page opening the **Value &amp; engagement** tab.

-   **Edit Model Provider Agent**

    The engagement record that tracks the deployment status, lifecycle, and business value of an AI agent model provider implementation. It measures productivity gains, net AI returns, total AI actions, and manages risk and conformance requirements to monitor the effectiveness and cost-efficiency of the agentic AI deployment.

    Select Edit Model Provider Agent to see the metric cards that track productivity gains, financial returns, AI actions, and cost-related data for the agentic AI deployment. All metrics are aggregated over a configurable time period, with a default view of the last 30 days.

    **Note:** Selecting Edit Model Provider Agent leads you to the Edit Model Provider Agent page opening the **Value &amp; engagement** tab.


## Usage by department

Shows the distribution of AI system usage across the top five departments in your organization. Data is displayed in a donut chart that shows total usage and breaks down usage by department.

Each department is color-coded and displayed with its usage count. The chart shows departments such as Customer Support, Sales, Engineering, HR, and others based on your organization's structure.

**Note:** View the AI systems usage by department that is measured by the number of times each system was used in an AI workflow.

## AI adoption by country

Displays AI adoption rates by geographic location, comparing the highest and lowest adoption regions. Adoption is measured as a percentage based on the number of LLM-related actions taken.

Two tabs allow you to view data sorted by highest adoption or lowest adoption. Countries are listed with their adoption percentage, shown in color-coded format to indicate adoption levels \(green for high adoption, red for low adoption\).

## Top 5 AI systems by department

Shows the five most frequently used AI systems across your organization, broken down by the departments that use them. Each system bar indicates the total usage count and shows department-level usage contribution through color coding.

Systems are listed in descending order by usage. Hover over a bar to see the department breakdown within that system's total usage.

To understand more about the Value insights from the ServiceNow AI Engagement dashboard, see [ServiceNow AI Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-snow-ai-engagement.md).

