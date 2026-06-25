---
title: Workforce Optimization for CSM release notes
description: The ServiceNow Workforce Optimization application enables you to efficiently route work to your team, manage your team's skills and schedules, and monitor their performance. Workforce Optimization was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Workforce Optimization for CSM release notes

The ServiceNow® Workforce Optimization application enables you to efficiently route work to your team, manage your team's skills and schedules, and monitor their performance. Workforce Optimization was enhanced and updated in the Australia release.

## Workforce Optimization for Customer Service highlights for the Australia release

-   Manage location‑based holiday calendars to improve workforce scheduling by mapping holidays to specific regions, enabling managers to plan shifts with accuracy, and reduce manual adjustments.
-   Enhance the Manager Dashboard with standalone installation support and new AI-powered widgets \(Sentiment Analysis, Trending Topics, and Auto QA\) to provide actionable insights.
-   Support real-time supervisor assistance during customer calls in Manager Workspace, enabling monitoring, whisper coaching, and direct participation
-   Analyze the help requested interactions segmented by different channels, such as Chat, Email, Messaging, Phone and Video.
-   Enable Schedule Management as a standalone capability, with backward compatibility for existing deployments and no additional configuration required after activation.

See [Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configurable-wfo-cs.md) for more information.

**Important:** Workforce Optimization for Customer Service is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Location Based Holiday Calendar Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/location-based-holiday-calendar-management.md)**

    Enable location-based holiday calendars to

    -   Manage location‑based holiday calendars that auto‑sync to schedules, providing real‑time visibility into regional holiday impacts and supporting accurate shift planning.
    -   Improve workforce scheduling and compliance by mapping holidays to specific regions, reducing manual adjustments and ensuring agents see their location‑based holidays in My Calendar.
-   **[Manager Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-configurable-manager-workspace-dashboards-new.md)**

    Enhance the Manager Dashboard to view

    -   New **AI Insights** tab on the Manager Dashboard in the Manager Workspace.
    -   The AI powered widgets: Sentiment Analysis, Trending Topics, and Auto QA. These widgets provide deeper, real‑time visibility into customer sentiment signals, trending interaction themes, and quality evaluations.
-   **[Manager Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-configurable-manager-workspace-dashboards-new.md)**

    Decouple the existing Manager Dashboard to make it available as a standalone feature.

    -   Install and configure the Manager Dashboard independently to provide a streamlined, modular experience, retaining only essential alerts and core widgets for performance, work management, and resource visibility while removing scheduling and coaching components.
    -   Managers can view Help Request alerts and Operational Insights when Channel Management is used with the Manager Dashboard. These capabilities are not available when Channel Management is used without the Manager Dashboard.
    -   The Manager Dashboard includes a tab-based layout with widgets for Customer Signals and Quality Management — Sentiment Analysis, Trending Topics, and Auto QA. Managers can access the Operations Insights tab with widgets such as Performance, Work Management, and Resource Management when additional capabilities are enabled.
-   **[Listen, Monitor or Barge in to an agent call](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/listen-agent-call-configurable-wfo-cs.md)**

    Monitor, coach, or barge into voice calls to

    -   Assist agents during live customer calls by opening the agent’s active phone interaction in Manager Workspace.
    -   Enable supervisors to silently monitor calls, whisper‑coach agents, join conversations, view real‑time transcription when the conversation panel is enabled, and switch modes or end the session at any time using the NVC utility panel.
-   **[Manager Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-configurable-manager-workspace-dashboards-new.md)**

    Enable Manager dashboard to view the Help Request on the landing page.

    -   View the **Help Request** tab on the Manager Workspace landing page and in Conversation Monitoring list view.
    -   Segment Help Request interactions by different channel including Chat, Email, Messaging, Phone and Video.
-   **[Channel Management in Workforce Optimization for Customer Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/explore-channels-configurable-wfo-cs.md)**
    -   View the **Help Request** tab on the Channel Management landing page.
    -   Enable supervisors to open any active voice request to review context and take action by monitoring the live call, coaching the agent privately, or barging in to speak with both the agent and the customer.
-   ****

    Enable Schedule Management schedule management capabilities in CSM configurable workspace:

    -   Provide a standalone licensing and entitlement model for Schedule Management schedule management using the  "com.sn\_shift\_planning" plugin.
    -   Support independent deployment of Schedule Management schedule management without Forecasting, Intraday Management, Coaching, or other Workforce Optimization modules.
    -   Extend scheduling to support shift and roster management for FSM and Retail, enabling phased use of Workforce Optimization modules.

## UI changes

-   **[Manager Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-configurable-manager-workspace-dashboards-new.md)**

    The following UI components have been added on the Manger Dashboard:

    -   The dashboard includes new AI‑powered widgets — Sentiment Analysis,Trending Topics, and Auto QA
    -   **Help requested** can be viewed on the **Manager Workspace landing page** and in **Conversation Monitoring** list view.
    -   The **Help requested** include different channels, such as **Chat**, **Email**, **Messaging**, **Phone** and **Video**.

## Activation information

Install Workforce Optimization by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-overview.md)**

    Automatically assign work items to your agents based on their availability, capacity, and skills using ServiceNow® Advanced Work Assignment.

-   **[Skills Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/skills-management.md)**

    Assess the skills that your organization needs, identify gaps, and plan for the hiring and training of your teams using ServiceNow® Skills Management.

-   **[CSM Workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md)**

    Agents can swap shifts, manage their time-off requests and approvals, and complete assigned training using ServiceNow® CSM Agent Workspace.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/customer-service-mgmt-rn-landing.md)

