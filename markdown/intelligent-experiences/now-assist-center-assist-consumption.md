---
title: AI Admin Center Assist Consumption page
description: Use the Assist Consumption page in AI Admin Center to monitor assist consumption trends and identify which AI assets are consuming the most assists across your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/now-assist-center-assist-consumption.html
release: australia
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, assist consumption]
breadcrumb: [View your assist consumption \(Lux UI\), Managing assist consumption \(Lux UI\), Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# AI Admin Center Assist Consumption page

Use the Assist Consumption page in AI Admin Center to monitor assist consumption trends and identify which AI assets are consuming the most assists across your organization.

## Assist Consumption page

The Assist Consumption page is accessible from the side navigation bar in AI Admin Center. Use the page to track total assist consumption and identify usage patterns across AI assets, departments, and users.

The Overview tab displays a **Last 3 months** label at the top of the page. This label indicates the fixed period for all data on the tab. This includes the trend chart, the top assets table, the top departments table, and the consumption band chart.



\[Omitted image "ai-admin-center-assist-consumption-overview.png"\] Alt text: Overview tab of the Assist Consumption page, showing the Total Assist Consumption summary, the Assists by asset type trend chart, and the Top assets by assist usage table.

The Overview tab of the Assist Consumption page contains the following components:

-   **Total Assist Consumption**

    This area of the page displays a bar chart with a legend summarizing assist consumption for the Last 3 months period, broken down by asset type. Use this area to assess overall consumption and compare spend across asset types.

-   **Assists by asset type**

    This area of the page displays a trend chart showing assist consumption over time for the Last 3 months period. Each filled area in the chart represents an asset type: Skills, Agents, Agentic Workflows, or Others. The Others series represents assists not attributed to the other asset types. Select Day or Week to set the granularity of the chart, and select a series in the legend to show or hide it.

-   **Top assets by assist usage**

    This area of the page displays a table ranking AI assets by assist consumption in descending order for the Last 3 months period.

    -   **Asset name**

        The name of the skill, agent, or agentic workflow.

    -   **Type**

        The asset type, displayed as a color-coded badge.

    -   **Total executions**

        The total number of executions for the asset in the Last 3 months period.

    -   **Assists used**

        The total number of assists consumed by the asset in the Last 3 months period.

    For agentic workflow rows, select the expand icon next to the asset name to view the list of individual tools within the workflow.

-   **Users by Assist Consumption Band**

    This area of the page displays a chart showing the distribution of users across consumption bands for the Last 3 months period. A consumption band represents a range of assists consumed by a user per month: fewer than 10, 10 to 100, 100 to 1,000, or more than 1,000. Use this chart to identify the concentration of high-consumption users and track how usage patterns shift over time.

-   **Top 10 departments by assist consumption**

    This area of the page displays a table listing the departments with the highest assist consumption for the Last 3 months period. Assists consumed are broken down by day in the table.

    -   **Department**

        The name of the department.

    -   **Assists**

        The total number of assists consumed by the department for the Last 3 months period.

    -   **Avg / day**

        The average number of assists consumed per day by the department for the Last 3 months period.

    A column for each day in the Last 3 months period shows the number of assists the department consumed on that day. A Total row summarizes the values for all listed departments.


