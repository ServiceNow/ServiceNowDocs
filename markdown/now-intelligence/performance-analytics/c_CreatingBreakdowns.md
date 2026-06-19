---
title: Indicator breakdowns
description: Breakdowns enable you to group or filter indicator scores by a qualitative attribute such as Priority, Category, or Assignment Group. You can apply a breakdown on the Analytics Hub, in KPI Details, and on dashboards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/c\_CreatingBreakdowns.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indicator breakdowns

Breakdowns enable you to group or filter indicator scores by a qualitative attribute such as Priority, Category, or Assignment Group. You can apply a breakdown on the Analytics Hub, in KPI Details, and on dashboards.

The values for each breakdown are called breakdown elements. For example, the Priority breakdown may have the elements Critical, High, and Low. Breakdowns are categorized as automated, manual, or external, depending on where these elements come from. Automated breakdown elements are specified in breakdown sources. Manual breakdowns have their elements entered manually to define an organization. Lastly, an external breakdown specifies the JDBC data source and SQL statement for retrieving breakdown elements.

For example, you can look at the Number of Open Changes by Assignment Group. Or you can see the Number of New Changes by Priority.

-   **[Create a breakdown from a wizard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/t_CreateBreakdownFromWizard.md)**  
Create a breakdown, breakdown source, and breakdown mappings, and associate the breakdown with indicators.
-   **[Breakdown sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/breakdown-sources.md)**  
Breakdown sources specify which unique values, called breakdown elements, a breakdown contains.
-   **[Automated breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/automated-breakdowns.md)**  
An automated breakdown uses a breakdown source to determine selectable elements.
-   **[Manual breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/manual-breakdowns.md)**  
In a manual breakdown, you define the breakdown elements and the indicator scores for each element manually instead of using records from a breakdown source.
-   **[Element filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_BreakdownElementFilters.md)**  
Element filters enable you to specify or limit the displayed breakdown elements on visualizations.
-   **[Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/breakdown-relations.md)**  
Breakdown relations open a new navigation path for viewing breakdown scores, by moving from one breakdown element to another element of the same breakdown. The elements should be in an hierarchical relationship.
-   **[Control ability to view breakdown elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/t_ControlAccessToABreakdown.md)**  
To limit which breakdown elements a subset of users can view on indicators, implement element security. Element security applies to widgets, workspaces, and the Analytics Hub.
-   **[Using breakdowns on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_SpecialDashboards.md)**  
You can add breakdown sources to a dashboard. Dashboard users then can select a breakdown source and one or more breakdown elements to filter scores in the visualizations on the dashboard.

**Parent Topic:**[Configure Performance Analytics fundamentals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_PAWidgetsAndDashboards.md)

