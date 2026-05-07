---
title: Generate insights for Enterprise Architecture Workspace dashboard widgets
description: You can use the conversational interface provided by AI Data Explorer Now Assist skill to query and analyze data from Enterprise Architecture Workspace dashboards. Instead of manually reviewing dashboard visualizations, you can use the AI Data Explorer to ask natural language questions to retrieve insights and identify trends.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use Now Assist, Now Assist for Enterprise Architecture \(EA\), Enterprise Architecture]
---

# Generate insights for Enterprise Architecture Workspace dashboard widgets

You can use the conversational interface provided by AI Data Explorer Now Assist skill to query and analyze data from Enterprise Architecture Workspace dashboards. Instead of manually reviewing dashboard visualizations, you can use the AI Data Explorer to ask natural language questions to retrieve insights and identify trends.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

AI Data Explorer, Query Generation Now Assist skills must be activated. Also, AI Search must be configured. For information, see [Configure AI Data Explorer and Query Generation skills](configure-ai-data-explr-qry-genr-skills.md).

Role required:

-   sn\_apm.apm\_user and sn\_apm.apm\_read \(to access EA workspace\)
-   now\_assist\_explorer\_user \(to use the AI Data Explorer feature\)

## About this task

You can ask questions about application portfolios, technology trends, business units, lifecycle stages, and other metrics displayed on the dashboard. You can use the AI Data Explorer to perform the following:

-   Ask specific queries on metrics and dimensions displayed on the widgets
-   Perform relationship analysis
-   Ask follow-up questions to explore deeper into the insights
-   Generate dashboards and graphs

You can ask AI Data Explorer the following types of queries.

-   Trend analysis queries
    -   How have application counts changed over time?
    -   What is the distribution of business applications by lifecycle stage?
    -   How do application scores vary across business units?
-   Comparative queries
    -   Compare application counts across different technology types
    -   Which business unit has the highest number of applications?
    -   What is the difference between Windows and UNIX application counts?
-   Specific metric queries
    -   Which application family is most used?
    -   What percentage of applications are in the retired lifecycle stage?
    -   Show me business applications by user base

The AI Data Explorer also considers the filters applied on the dashboard page while generating insights.

You can use the AI Data Explorer on widgets that are based on the following tables:

-   CI Scores \(apm\_app\_score\)
-   Business Applications \(cmdb\_ci\_business\_app\)
-   Information Objects \(cmdb\_ci\_information\_object\)
-   Indicator Scores \(apm\_app\_indicator\_score\)
-   Total Cost of Ownership \(sn\_apm\_tco\)
-   Capabilities \(cmdb\_ci\_business\_capability\)
-   Digital Interfaces\(sn\_apm\_di\_digital\_interface\)

**Note:**

-   The AI Data Explorer generates insights based on data from one widget at a time. It cannot generate insights by combining or correlating data from multiple widgets simultaneously.
-   The insights are displayed based on current data only and does not support time-series comparisons, such as comparing today's metric values against values from a previous period.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace** &gt; **Dashboard**.

2.  Select the Explore with AI icon \(![Explore with AI icon.](../image/explore-ai.png)\) on any widget on the dashboard.

    The AI pop-up window appears.

    ![Enterprise Architecture Workspace Dashboard page displaying the Explore with AI pop-up window.](../image/explore-ai-popup.png)

3.  On the pop-up window, perform any of the following options.

<table id="choicetable_nn3_qpl_f3c"><thead><tr><th align="left" id="d53897e283">

UI element

</th><th align="left" id="d53897e286">

Function

</th></tr></thead><tbody><tr><td id="d53897e292">

**Text box**

</td><td>

Use this option to ask any question related to the data associated with the selected widget. This option helps you get specific information on the widget data.

</td></tr><tr><td id="d53897e304">

**Analyze trend**

</td><td>

Use this option to analyze overall trends in the data. This option helps you to understand how the metrics have changed over time or identify growth or decline patterns.

</td></tr><tr><td id="d53897e316">

**Show different distribution**

</td><td>

Use this option to view the same data broken down by different dimensions. This option helps you to compare data distributions across alternative categorizations and view the data from different analytical perspectives.

</td></tr><tr><td id="d53897e328">

**+ Add to exploration**

</td><td>

Use this option to enable Now Assist to generate its own insights into the widget data.

</td></tr></tbody>
</table>    **Note:** You also have the option to choose your analysis mode. The available options are:

    -   **Standard analysis**: Use this option when you want quick and concise responses.
    -   **Extended analysis**: Use this option when you want to view deeper insights, trends, and patterns in the data.
    ![Screenshot of the explore with AI pop-up window with the analysis type options highlighted.](../image/explore-ai-zoom.png)

4.  Enter your query or select any of the available options.

    The AI Data Explorer pop-up window appears displaying insights on the widget data. It also generates graphs or charts to complement the insights.

    ![Screenshot of the AI Data Explorer window displaying the insights generated for the selected widget.](../image/explore-ai-output.png)

5.  View the AI Data Explorer insights and take further actions.

    You can perform the following:

    -   Define a goal in the **Goal** box for Now Assist to improve the quality of insights and suggestions.

        ![Screenshot of the AI Data Explorer window displaying the Goal box.](../image/explore-ai-goal.png)

    -   Ask follow-up questions based on suggestions provided by Now Assist

        ![Screenshot of the AI Data Explorer window displaying list of follow-up questions.](../image/explore-ai-flw-up-qst.png)

    -   Select **Summarize** to summarize the insights generated.

        ![Screenshot of the AI Data Explorer window with the Summarize button highlighted.](../image/explore-ai-summarize.png)

    -   Share, duplicate, or delete the insights generated by AI Data Explorer by selecting the more actions icon \(![More actions icon.](../../application-portfolio-management/image/eaw-image/eaw-icon-menu.png)\).

        ![Screenshot of the AI Data Explorer window displaying the more actions drop-down menu.](../image/explore-ai-share.png)


**Parent Topic:**[Using Now Assist for Enterprise Architecture \(EA\)](../concept/using-now-assist-for-ea.md)

**Related topics**  


[Configure AI Data Explorer and Query Generation skills](configure-ai-data-explr-qry-genr-skills.md)

[Explore the Enterprise Architecture Workspace dashboard](../../../use/dashboards/concept/eaw-workspace-dashboard.md)

