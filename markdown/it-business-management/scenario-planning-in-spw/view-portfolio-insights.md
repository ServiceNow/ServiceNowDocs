---
title: View insights for a portfolio plan in Strategic Planning Workspace or Portfolio Planning Workspace using ServiceNow Otto for SPM
description: View AI-generated insights for a portfolio plan in Strategic Planning Workspace or Portfolio Planning Workspace to identify planning items at risk of schedule delays, monitor active projects showing early risk indicators, analyze root causes, and review recommended actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/view-portfolio-insights.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Manage portfolio plans, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# View insights for a portfolio plan in Strategic Planning Workspace or Portfolio Planning Workspace using ServiceNow Otto for SPM

View AI-generated insights for a portfolio plan in Strategic Planning Workspace or Portfolio Planning Workspace to identify planning items at risk of schedule delays, monitor active projects showing early risk indicators,analyze root causes, and review recommended actions.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: sn\_align\_core.apw\_user

## About this task

Use Portfolio Insights to identify prioritized planning items that are at risk of schedule delays. The insights are categorized by impact severity and include root cause analyses and AI-generated recommended actions to help you address identified risks.

The insights are generated for the following categories for a portfolio plan:

-   Delayed planning items — Planning items delayed beyond the planned end date
-   Date misalignment — Planned versus approved date misalignment
-   Delayed start — Planning items with delayed starts
-   Projects at risk — Active projects that show early risk indicators but have not yet experienced delays
-   Budget overrun — Planning items whose current fiscal year forecast exceeds the approved budget

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select the portfolio plan to view insights.

3.  From the portfolio plan header, select **Portfolio insights**.

    **Note:** If insights were generated previously, the AI Insights window displays the timestamp of the last generation. You can select **Regenerate** or Refresh icon to generate updated insights and recommendations based on the latest available data.

    Portfolio Insights displays risk signals across the following areas: delayed planning items, projects at risk, delayed starts, and planned versus approved date misalignments.

4.  On the Portfolio insights modal, review the insight categories displayed.

    Insights are grouped by impact severity — critical, medium, and low — to help you prioritize which items require immediate attention.

5.  Select an insight to view the root cause analysis.

    The system displays detailed root cause information, including compounding risks such as resource overallocation across multiple planning items.

6.  Review the AI-generated recommended actions for each root cause.

    Recommended actions provide specific steps to mitigate delays and resolve misalignments within the portfolio plan.

7.  Take corrective action based on the recommendations, as needed.


## Result

Portfolio Insights identifies prioritized planning items at risk, along with root cause analyses and recommended actions to help you maintain portfolio health.

**Parent Topic:**[Managing portfolio plans in Strategic Planning Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/managing-portfolio-plans-in-alignment-planner-workspace.md)

