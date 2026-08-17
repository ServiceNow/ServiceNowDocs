---
title: Value dashboard
description: The Value dashboard provides real-time visibility into the productivity gains and financial returns delivered by your AI Control Tower agents. Track hours saved, cost savings, net returns, and system performance to measure ROI and demonstrate AI investment impact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-aict-value-insights.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 5
keywords: [AI Control Tower, value dashboard, AI metrics, engagement metrics]
breadcrumb: [Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Value dashboard

The Value dashboard provides real-time visibility into the productivity gains and financial returns delivered by your AI Control Tower agents. Track hours saved, cost savings, net returns, and system performance to measure ROI and demonstrate AI investment impact.

The Value dashboard aggregates metrics across all deployed AI agents and systems, enabling you to understand the business impact of your AI Control Tower implementation. Use this dashboard to track productivity improvements, monitor financial returns, compare agent performance, and communicate value to stakeholders.

To view the Value dashboard on AI Control Tower, navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Insights** &gt; **Value** &gt; **.**\[Omitted image "aict-value-dashboard.png"\] Alt text: View the Value dashboard and the different value metrics.

**Note:** All metrics on the Value dashboard default to the last 30 days. Use the time period selector in the top-right corner to adjust the date range and view metrics for different time periods \(for example, last 7 days, last 90 days, or a custom range\).

## Productivity gains

The Productivity gains section displays the total hours and the money saved across all AI systems during the selected time period. This metric represents direct productivity improvements delivered by AI agents through:

-   **Hours saved**

    Total agent-hours of work eliminated or accelerated through AI automation. The trend line shows how hours saved has changed over time, with percentage comparison to the previous period.

-   **Money saved**

    Monetary value of the productivity gains, calculated in dollar terms. This metric helps translate productivity improvements into business-relevant financial impact.


Both these metrics include trend lines showing daily fluctuations and a percentage comparison badge indicating whether productivity is increasing or decreasing relative to the previous period.

You can view the AI systems and edit the set the time period for productivity gains. On the AI system productivity gains page, you will see the AI systems listed along with the Productivity gains in hours and Productivity gains in currency. To change the time period, select the calendar drop-down, choose the time period, and select **Apply**.

## Value breakdown by AI system

The Value breakdown by AI system section lists the top-performing AI agents and their individual productivity contributions, ranked by hours saved.

For each agent, the dashboard displays:

-   Agent name
-   Hours saved by that agent or USD saved by the agent

    **Note:** You can view the value breakdown either by hours or USD using the drop-down.

-   Percentage change compared to the previous period

This breakdown helps you identify which agents deliver the most value, prioritize optimization efforts, and allocate resources toward the highest-impact use cases.

## Net AI returns

The Net AI returns section shows the net financial return from AI consumption after deducting costs. This metric represents the true ROI of your AI investment.

The Net AI return displays:

-   Money saved minus Total AI cost
-   Percentage change relative to the previous period
-   A trend line about how the net returns have evolved over time

Use this metric to demonstrate business value and justify continued investment in AI Control Tower capabilities.

## Total AI cost

The Total AI cost section displays the total usage cost across all AI systems, measured in assists and tokens \(Enterprise AI\). This metric reflects the investment required to generate the value shown on the dashboard.

-   The aggregated cost across all deployed AI systems
-   Percentage change relative to the previous period
-   A bar chart showing daily cost distribution, broken down by Assist and Tokens displayed with legends.

Monitor this metric to optimize AI spending and understand the cost-to-value ratio of your deployment.

View the AI cost overview and the AI cost breakdown by selecting the external link icon on the Total AI cost section. On the Total AI cost value page, you will see:

-   The AI cost overview trend with AI total cost in USD vs the selected time period \(to change the time period, select the calendar drop-down, choose the time period, and select **Apply**\).

    **Note:** You can view this data for all vendors or a selected vendor.

-   The AI cost breakdown data for only those AI systems and vendors whose token consumption is captured via integrations or manual cost configuration.

## AI system usage

The AI system usage section provides insights into how your AI systems are being consumed across the organization through:

-   **Productivity gains by vendor**

    The Productivity gains by vendor visualization shows how the value is distributed across different AI vendors \(for example, ServiceNow, Microsoft, Amazon\). The donut chart helps you understand which vendor platforms contribute the most to your overall value delivery.

-   **Persona mix**

    The Persona mix section indicates which user personas are driving the most value from your AI Control Tower. This metric shows what percentage of your AI systems serve fulfiller personas or other user types.

    The persona mix helps target adoption efforts, identify the under-served user groups, and prioritize agent development for high-value personas.

-   **Model performance**

    The Model performance section indicates the AI model types powering your AI Control Tower systems. For example, this metric flags whether all your AI systems are using agentic AI models or if you're using a mix of model types.

    Use this insight to verify consistency in AI capabilities and plan upgrades to newer, higher-performing models.

-   **Platform spread**

    The Platform spread section shows which platforms are running your AI systems. For example, this metric displays what percentage of your AI runs on ServiceNow, Microsoft, Amazon or other platforms.

    Monitor platform spread to understand vendor dependencies, plan multi-vendor strategies, and optimize for platform consolidation if needed.


View the overall AI system usage that's displayed agent-wise with persona, deployed date, actions, average user using the agent, productivity gains, AI system type, Vendor and the total AI usage.You can use the time period selector in the top-right corner to adjust the date range and view metrics for different time periods.

To understand more about the value insights from the ServiceNow AI value dashboard, see [ServiceNow AI Value dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-snow-ai-value.md).

