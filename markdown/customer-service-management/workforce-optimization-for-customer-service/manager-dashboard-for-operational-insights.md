---
title: Manager dashboard for operational Insights
description: The Manager Dashboard can be installed and configured independently. This change allows you to use the dashboard without installing the full Workforce Optimization suite and keeps dashboard packaging consistent with Channel Management.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Workforce Optimization for Customer Service, Customer Service Management]
---

# Manager dashboard for operational Insights

The Manager Dashboard can be installed and configured independently. This change allows you to use the dashboard without installing the full Workforce Optimization suite and keeps dashboard packaging consistent with Channel Management.

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

## Tabs and widgets

-   **Operational Insights**: Provides existing operational widgets and retains current data sources and configurations. Uses UIB layout and handles no-data and error states gracefully..
-   **AI Insights**: Shows AI widgets—**Sentiment Analysis** and **Trending Topics** based on enabled capabilities. Shares global filters with overview and avoids performance impact. If the AI plugins are not installed, the AI tab does not appear.

    **Access and governance**: Access is role‑based \(`sn_mgr_dashboard.user`\) and enforced through ACLs at the page, tab, and widget level. Unauthorized users do not see the dashboard in navigation, and APIs are protected. Role inheritance keeps additional manager records in sync with the primary manager’s roles \(sn\_mgr\_dashboard.user\) and entitlements.


![New widgets Operational and AI Insights widgets are added on the manager dashboard](../image/mangr-dashboard-new-widgets.png "Manager Dashboard with New Widgets")

**Parent Topic:**[Using Workforce Optimization for Customer Service](use-configurable-wfo-cs.md)

