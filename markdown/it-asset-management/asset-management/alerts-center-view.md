---
title: Alerts center view in the AI Cost Management application
description: The Alerts center view displays alerts related to your AI consumption spend limits. You can review these alerts to prevent potential AI spend overages so that you can stay within budget.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/alerts-center-view.html
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Views in AI Cost Management, Explore, AI Cost Management, IT Asset Management, Asset Management]
---

# Alerts center view in the AI Cost Management application

The Alerts center view displays alerts related to your AI consumption spend limits. You can review these alerts to prevent potential AI spend overages so that you can stay within budget.

The AI Cost Management application triggers alerts based on the thresholds you set against spend limits. You define spend limits from the Settings view of the AI Cost Management application. These limits and thresholds help you maintain control over your AI spend and avoid overages. For more details on spend limits, see [Set up an AI spend limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/set-up-spend-limits.md).

You access the Alerts center view by selecting **Alerts center** in the navigation panel of the AI Cost Management application.

\[Omitted image "aicm\_alerts.png"\] Alt text: Alerts center showing seven alert cards with severity levels, departments, and spending limit percentages.

Each alert displays the following information:

-   The criticality level of the alert. Levels are determined by comparing how much spend is left before meeting a threshold to how much time is left in the month.

    |Alert level|Definition|
    |-----------|----------|
    |Critical|The spend limit has been reached.|
    |High|The spend is over 50% faster than accounted for \(for example, the limit might be reached in the last third of a month\).|
    |Medium|The spend is as accounted for.|
    |Low|The spend will likely not reach the limit.|

-   The amount of time that has elapsed since the alert was triggered.
-   The alert category, such as Account, Cost Center, Department, or User.
-   The affected entity, such as a specific user or cost center.
-   The amount spent against the spend limit, in both percentage and dollars.

Filter the alerts that appear in this view by selecting the Filter icon. When the Refine list window opens, you can select filter by entity type such as the entire organization or users, and also by criticality.

Select **Open** to take remedial actions.

To dismiss an alert, select the actions drop-down menu and choose **Dismiss**.

**Note:** Dismissing an alert removes it only from your view. It will still display to other users with access to the alert.

For more details on the information and actions that are available for each alert, see [Review AI spend alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/review-resolve-alerts.md).

