---
title: Use automated quality assurance dashboard as a manager
description: Access the automated quality assurance dashboard from the CSM Configurable Workspace to view detailed agent performance metrics and quality assurance scoring data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/use-quality-assurance-dashboard-as-a-manager.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-02-04"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, ServiceNow Otto for CSM, Customer Service Management]
---

# Use automated quality assurance dashboard as a manager

Access the automated quality assurance dashboard from the CSM Configurable Workspace to view detailed agent performance metrics and quality assurance scoring data.

## Before you begin

Role required: Manager

Before you begin, confirm you have:

-   Manager role permissions in CSM
-   Access to the CSM Configurable Workspace

## About this task

The automated quality assurance \(QA\) dashboard provides managers with detailed insights into individual agent performance metrics. This view displays comprehensive QA scoring data at both the agent and case levels, enabling you to monitor, evaluate, and provide feedback on agent interactions.

The automated quality assurance widget serves as an entry point to access the quality assurance supervisor dashboard and is available on the CSM Configurable Workspace.

## Procedure

1.  Log in to CSM Configurable Workspace.

2.  Navigate to the dashboard.

    The dashboard displays various widgets and tools relevant to your management responsibilities.

3.  Locate the **Quality assurance \(QA\)** widget on your dashboard.

    The widget typically displays a summary of recent quality assessment data, including key metrics such as average quality scores and evaluation counts.

4.  Select **View dashboard** in the widget to access the detailed quality reports.

    The automated quality assurance dashboard opens, providing access to comprehensive quality assurance tools and reports.

5.  Review the quality reports for your agents.

    You can perform the following actions on the dashboard.

    -   View individual agent quality scores and evaluations.
    -   Filter reports and cases by date range, agent, quality parameters, or by assignment groups. When the **Assignment** filter is applied the trends, breakdowns, list of agents and cases are all impacted and the dashboard is refreshed to show values based on the assignment group that is selected along with the date range.

        **Note:** You can set filters for both the assignment group and the date.

    -   Select **Clear all** to remove all the filters that are set.
    -   Analyze trends in quality performance over time.
    -   Identify coaching opportunities based on quality assessment results.
    -   Export reports for further analysis or documentation.
    -   View Auto QA score breakdown by category for a selected date range.

## Result

From the quality assurance dashboard, you can monitor team performance, review quality metrics, and manage quality assurance processes.

Select any date on the **Trends** graph on the dashboard to view case information in more detail.To learn more about the trends and reviewed cases, see [Use automated quality assurance dashboard as a live agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/use-quality-assurance-dashboard-as-an-agent.md).

The Agent and Case tables present average Auto QA scores, category scores, and case information for each agent. Each category score represents the average of all parameters within that category.

The Auto QA dashboard displays quality assurance cases and associated agents as a sortable list component. To reorganize agent or case data, select the column header and arrange them in ascending or descending order. You can organize them by the number of reviewed cases, performance score, caseload, or other metrics. A new tab with more information opens when you select an agent or case from the list.

You can use the following features to manage data:

-   Filters: Use the condition builder to filter by any column.
-   Group By: Organize data by any column.
-   Sort: Arrange data by any column.
-   Search: Find specific information across columns.
-   Export: Download data as PDF, JPG, or CSV.

**Note:**

-   Agent performance is rated on a 1-5 scale with color-coded visual indicators. Managers can modify any parameter score as needed.
-   When AI-generated content is present, an alert indicator and AI tagline appear at the top of the review. When you manually edit parameter scores or feedback, the AI tagline is removed and the card component switches to a standard card.
-   When navigating from the dashboard to the case-level view, managers can perform various actions. These include viewing detailed feedback for a specific case and editing QA parameters to adjust scores for individual evaluation parameters.
-   The Category Trend Analysis view includes a drop down where one category is selected by default. Managers can choose any category from the drop down to view its performance trends. Once selected, the trend data updates to display the chosen category’s score over time.
-   AI alert with AI gradient color theme highlights that the pages are fully generated by AI. You can dismiss the alert by selecting the X on the alert banner.

**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[Use automated quality assurance dashboard as a live agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/use-quality-assurance-dashboard-as-an-agent.md)

[Automated quality assurance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/quality-assurance-management.md)

