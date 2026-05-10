---
title: AI cases tab
description: Track, monitor, and analyze your AI case workflows, identify your workflow bottlenecks, and monitor your accountability of your AI-related risks by using the AI risk and compliance dashboard. As an AI steward, you can also use the dashboard to track the status and trends of your AI-related inquiries.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [AI Risk and Compliance workspace, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI cases tab

Track, monitor, and analyze your AI case workflows, identify your workflow bottlenecks, and monitor your accountability of your AI-related risks by using the AI risk and compliance dashboard. As an AI steward, you can also use the dashboard to track the status and trends of your AI-related inquiries.

## AI cases

The **AI cases** tab on the AI risk and compliance dashboard provides the key metrics, trends, and actionable tasks that you can use to track your AI risks, case activities, compliance tracking, and governance enforcement. You can get case-level insights, task-level tracking, and accountability for your responsibilities and progress. As an AI steward, you can report a case when a violation is found. An AI analyst also follows the case and comes up with a resolution.

**Note:** Dashboards in the AI Risk and Compliance Workspace \(Risk and Compliance, Operations, and AI Cases\) display data for **Managed** AI assets only. AI assets that are marked as **Unmanaged** are excluded from dashboard widgets, metrics, and summary counts, but remain visible in inventory and list views. If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, you can mark assets as Managed or Unmanaged. For more information, see [Assets list managed and unmanaged assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/assets-list-managing-and-unmanaging-assets.md).

You can drill down into the data on each of the following widgets to learn more about an AI case.

-   **AI cases status by state**

    Shows distribution of reported AI Cases by life cycle state or workflow state.

-   **AI cases status by priority**

    AI cases based on their priority: Critical, High, Moderate, Low, and Planning.

-   **AI cases**

    Summarized list of AI cases reported:

    -   All: All the AI cases
    -   Overdue: AI cases that are past the due date.
    -   Due in 7 days: AI cases due in the next 7 days.
    -   Unassigned: AI cases that aren’t assigned to anyone.
    Attributes of each case, such as Name, Sub-type, Case analyst, Priority, and State are available in a list view. Select each card to view that category of AI cases in a list view.

-   **Trends**

    Visual patterns and historical data that are associated with the AI cases:

    -   AI cases by subtype widget: Trends by different categories of the AI case subtypes. You can group data by business unit, location, or primary cause to get contextual insight into the issues or AI cases patterns across the departments or systems. You can filter by AI assets.
    -   Open and closed cases widget: Historical trends of the case resolutions over a specified time frame. You can see the historical trends in the last 12 months. The historical trends help stakeholders to analyze the volume fluctuations and how efficiently the cases were closed.

        For example, in the last 12 months, consider that 4,200 cases were created and 3,960 cases were closed. The average time of case closure was 2.8 days, the peak case volume was in January 2025 \(510 cases were created\), and the fastest case resolution month was March 2025. You can see that over the past 12 months, the case closure efficiency has steadily improved, with a 12% decrease in the average resolution time compared to the previous year.

-   **Tracking**

    AI case progress at the task and issue level:

    -   Action tasks
        -   Number of tasks in the Overdue, Due in 7 days, or Unassigned states.
        -   Task distribution by the status, such as Draft or Work in Progress.
    -   Issues
        -   Counts of issues that are linked to AI cases by their states like New, Review, or Responds.
        -   Counts of issues that are linked to AI cases by additional details like Overdue, Due in 7 days, or Unassigned.

The [**Create AI case**](../task/create-ai-case-in-the-ai-risk-and-compliance-workspace.md) button enables you to initiate a new AI case record within the monitoring dashboard. This action is typically used to document, investigate, or track issues, risks, or compliance concerns that are related to AI models or datasets. Use the [**Create issue**](../task/create-ai-issue-in-the-ai-risk-and-compliance-workspace.md) button to create an issue related to AI cases.

The following example shows the **AI cases** tab on the AI risk and compliance dashboard.

![AI cases tab on the AI risk and compliance dashboard. See the text in the previous section for descriptions of the different widgets on the dashboard.](../image/ai-case-landing-page.png "AI cases tab on the AI risk and compliance dashboard")

## Inquiries

The **Inquiries** tab on the AI risk and compliance dashboard provides you with a structured view of the AI inquiry workflow. Use the following widgets on the dashboard to track the compliance and then to monitor the status and progress of an inquiry:

You can drill down into the data on each of the following widgets to learn more about an AI case.

-   **Inquiries status by state**

    Counts of inquiries by state. New, Triage, In progress, and Approved inquiries are represented in the donut chart.

-   **Inquiries status by priority**

    Counts of inquiries by priority. An inquiry can have Critical, High, Moderate, Low, or Planning priorities.

-   **Inquiries**

    Summarized list of all AI inquiries. It’s filterable based on parameters such as status, priority, and assignment.

    The essential attributes of inquiries are based on the operational relevance or urgency. Each inquiry entry includes metadata such as:

    -   Name
    -   Requested by
    -   Assigned to
    -   State
    -   Priority
-   **Trends**

    Trend-based insights into your inquiry activity across the organization. These visualizations support longitudinal analysis to improve planning and compliance responsiveness.

    **Note:** Longitudinal analysis refers to the process of analyzing data points across departments, teams, or systems over a period of time.

    Filters, such as the AI assets and the time range, help you to refine the analytics.

    -   Inquiries by business unit: You can see the distribution of inquiries across the various departments or functional areas of your organization. This distribution helps you to identify where most AI-related concerns originate so that you can plan on more targeted risk mitigation or awareness training.
    -   Open and closed inquiries: You can track the volume of inquiries that are initiated and resolved within a selected time range. This tracking enables you to track how your workflow is performing and to plan for future capacity.

Use the [**Create inquiry**](../task/raise-ai-inquiry.md) button to initiate a new inquiry. You can make timely reports of AI-related concerns or clarification requests.

The following example shows the **Inquiries** tab on the AI risk and compliance dashboard.

![Inquiries tab on the AI risk and compliance dashboard. See the text in the previous section for descriptions of the different widgets on the dashboard.](../image/ai-cases-inquiries-tab.png "Inquiries tab on the AI risk and compliance dashboard")

**Related topics**  


[AI governance life cycle](ai-gov-lifecycle.md)

[AI cases and inquiries](airc-cases-inquiries.md)

