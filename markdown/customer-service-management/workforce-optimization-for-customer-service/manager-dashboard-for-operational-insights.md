---
title: Manager dashboard for operational Insights
description: The Manager Dashboard can be installed and configured independently. This change aligns dashboard packaging with channel management and enables broader adoption across Pro and Pro+ customers.
locale: en-US
release: australia
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Workforce Optimization for Customer Service, Customer Service Management]
---

# Manager dashboard for operational Insights

The Manager Dashboard can be installed and configured independently. This change aligns dashboard packaging with channel management and enables broader adoption across Pro and Pro+ customers.

## Manager dashboard for Pro and Pro+ customers

Pro and Pro+ customers can access manager insights without the full WFO suite. Packaging aligns with channel management so administrators manage dashboards the same way across products. UIB components make the dashboard easier to reuse and extend.

The dashboard and its widgets are available as UIB components you can place in Agent/Manager Workspace. Components render conditionally based on SKU entitlements to ensure a consistent experience across Pro and Enterprise.

Pro Customers can view Help Request alerts and Operational Insights when Channel Management is adopted with the dashboard. These capabilities are not available when Channel Management is adopted without the dashboard.

Pro+ Customers, can view a tab‑based dashboard layout with AI‑powered widgets for Customer Signals and Quality Management. They can access the Operations Insights tab with widgets like Performance, Work Management, and Resource Management.

## Tabs and widgets

-   **Operational Insights**: Provides existing operational widgets and retains current data sources and configurations. Uses UIB layout and handles no‑data and error states gracefully.
-   **AI Insights**: Shows AI widgets—**Sentiment Analysis** and **Trending Topics** based on entitlements. Shares global filters with overview and avoids performance impact. If the AI plugins are not installed, the AI tab does not appear.

    **Access and governance**: Access is role‑based \(sn\_mgr\_dashboard.user\) and enforced through ACLs at the page, tab, and widget level. Unauthorized users do not see the dashboard in navigation, and APIs are protected. Role inheritance keeps additional manager records in sync with the primary manager’s roles \(sn\_mgr\_dashboard.user\) and entitlements.


![New widgets Operational and AI Insights widgets are added on the manager dashboard](../image/mangr-dashboard-new-widgets.png "Manager Dashboard with New Widgets")

