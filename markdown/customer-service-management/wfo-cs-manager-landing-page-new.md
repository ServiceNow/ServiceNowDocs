---
title: Manager workspace landing page
description: The Manager Workspace landing page provides managers with real-time alerts and key metrics that reflect the overall health and performance of the organization. By consolidating work and resource management data, managers can effectively oversee team performance, optimize agent utilization, and drive continuous improvement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/wfo-cs-manager-landing-page-new.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 5
breadcrumb: [Workforce Optimization for Customer Service, Agent management, Use, Customer Service Management]
---

# Manager workspace landing page

The Manager Workspace landing page provides managers with real-time alerts and key metrics that reflect the overall health and performance of the organization. By consolidating work and resource management data, managers can effectively oversee team performance, optimize agent utilization, and drive continuous improvement.

The Manager Workspace landing page showcases the various available widgets.

\[Omitted image "manager-workspace-landing-page.png"\] Alt text: manager dashboard with new widgets

The landing page provides the real-time data of the current workload and the team performance.

|Alert|Description|
|-----|-----------|
|Help requested|View the help requests from agents and act on them. **Help requested** can be viewed on the **Manager Workspace landing page** and in **Conversation Monitoring** list view. Analyze the help requested interactions segmented by different channels, such as **Chat**, **Email**, **Messaging**, **Phone** and **Video**. This feature improves visibility into ongoing challenges, facilitating quicker responses to team members and improving collaboration.|
|Overdue learnings|View the training tasks that remain incomplete past their deadlines. This feature helps you to identify training gaps and verify timely skill development.|
|Time off requests|List of submitted time-off requests pending for approval. This feature helps in managing employee leave, making it easier to plan and coordinate within your team.|
|Shift swap requests|Access the submitted shift swap requests to approve, reject, or add comments as needed. Once a request is approved or rejected, it’s removed from the list. This feature enables you to handle shift swap requests effectively.|

|Key metrics|Description|
|-----------|-----------|
|CSAT \(Past 1hr\)|Review customer satisfaction \(CSAT\) scores across various channels, including case, chat', voice and messaging. Additionally, you can filter CSAT by teams. This feature enables you to analyze customer feedback and improve service.|
|Interaction service level \(Past 1hr\)|Displays service level of customer interactions. This feature helps identify improvement areas and enhances overall service quality, resulting in increased customer satisfaction.|
|Average wait time \(Past 1hr\)|Monitor the average wait time for customer interactions across various channels, including voice, case, chat, and messaging. This feature helps you identify trends and make informed decisions to improve service efficiency.|

|Key metrics|Description|
|-----------|-----------|
|Volume by channel|Analyze the volume of interactions segmented by different channels, such as case, chat, voice, and messaging. This feature provides insights into customer engagement trends, helping you assess the resource needs.|
|Today's work status|Monitor the status of ongoing cases and interactions. This feature enables you to effectively track the progress ongoing work items.|
|Open P1 cases|Access the active priority 1 \(P1\) cases that require your immediate attention, listed with the longest-open cases first. Select **View All** to see all critical cases. This feature enables you to identify and address urgent issues.|

|Key metrics|Description|
|-----------|-----------|
|Agent presence status|Check the current availability of your agents, indicating whether they’re active, away, or offline. This feature helps you to monitor workforce engagement and optimize resource allocation for effective customer support.|
|Average agent utilization|Track the current average utilization rate of agents to assess how effectively their time is spent on productive tasks. Additionally, you can also filter average utilization by teams. This feature helps you to balance your workload and optimize resource allocation.|
|Top skills in 24 hrs|View the most frequently utilized skills over the past 24 hours. This feature helps you identify high-demand skills and guide or plan training efforts.|
|Team's performance|View important metrics for individual team members, including agent adherence percentages and CSAT scores. This feature helps you evaluate each agent's contributions and confirms they meet scheduled commitments and customer expectations.|

The Manager Dashboard includes Sentiment Analysis and Trending Topic widgets that give supervisors visibility into customer sentiment and agent performance.

The Manager Dashboard in Manager Workspace includes an **AI Insights** tab. This tab contains AI widgets that surface customer sentiment signals, trending interaction themes, and quality evaluations. The tab follows existing UI and loading standards, and its tab-switching behavior is consistent with current dashboard interactions.

## Tabs and widgets

-   **Operational Insights**: Provides existing operational widgets and retains current data sources and configurations. Uses UIB layout and handles no-data and error states gracefully.
-   **AI Insights**: Shows AI widgets such as **Sentiment Analysis** and **Trending Topics** based on enabled capabilities. Shares global filters with overview and avoids performance impact. If the AI plugins are not installed, the AI tab does not appear.

    **Access and governance**: Access is role‑based \(`sn_mgr_dashboard.user`\) and enforced through ACLs at the page, tab, and widget level. Unauthorized users do not see the dashboard in navigation, and APIs are protected. Role inheritance keeps additional manager records in sync with the primary manager’s roles \(sn\_mgr\_dashboard.user\) and entitlements.

-   **Sentiment Analysis Widget**: Provides a consolidated view of customer sentiment indicators, enabling supervisors to quickly gauge shifts in satisfaction and emerging pain points.
-   **Trending Topics Widget**: Displays recurring themes from customer interactions, helping managers identify the root causes of service patterns or issues.

## Manager dashboard availability and configurations

The Manager Dashboard provides manager insights across multiple configurations. You can manage the dashboard the same way they manage other channel-based experiences, ensuring consistent setup across products. UI Builder \(UIB\) components make the dashboard easier to reuse and extend.

The dashboard and its widgets are built using UIB components. You can add these components to Agent Workspace or Manager Workspace. Widgets appear only when the required capabilities are enabled, providing a consistent experience across configurations.

When Channel Management is used with the Manager Dashboard, managers can view:

-   Help Request alerts
-   Operational Insights

These insights are not available when Channel Management is used without the Manager Dashboard.

Advanced configuration: When additional insights and analytics capabilities are enabled, the dashboard includes;

-   A tab-based layout
-   An AI-powered widgets for Customer Signals and Quality Management
-   An Operations Insights tab with widgets such as Performance, Work Management, and Resource Management

The available widgets and tabs depend on which capabilities are enabled in the instance.

**Parent Topic:**[Using Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/use-configurable-wfo-cs.md)

