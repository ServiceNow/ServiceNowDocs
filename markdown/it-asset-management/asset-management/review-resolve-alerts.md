---
title: Review AI spend alerts
description: Review the AI spend alerts that trigger when you exceed the specified spend limit thresholds. These alerts help you maintain visibility and control over your AI spend so that you can avoid unexpected overages and stay aligned with your AI budget.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/review-resolve-alerts.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Monitoring your AI spend and usage, AI Cost Management, IT Asset Management, Asset Management]
---

# Review AI spend alerts

Review the AI spend alerts that trigger when you exceed the specified spend limit thresholds. These alerts help you maintain visibility and control over your AI spend so that you can avoid unexpected overages and stay aligned with your AI budget.

## Before you begin

-   Set up spend limits that align with your organization's AI budget thresholds. The AI Cost Management application triggers AI spend alerts based on these spend limits. For detailed instructions, see [Set up an AI spend limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/set-up-spend-limits.md).

Role required: ai\_cost\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  In the navigation panel of the AI Cost Management application, select **Alerts center**.

3.  Filter the alerts that appear in the Alerts center view.

    By default, the Alerts center view displays all alerts that trigger across your organization, in ascending chronological order. However, you can filter the alerts that appear based on the alert category and criticality level.

    1.  Select the Filter icon.

    2.  In the Refine list window, select one or more categories or criticality levels to filter by.

    3.  Select **Apply**.

        The Alerts center view automatically reloads, displaying only the alerts that match your selected filter options.\[Omitted image "aicm\_alerts\_filter.png"\] Alt text: Alerts center showing the Refine list panel with Category and Criticality filter options.

4.  Review the details of each alert.

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
5.  View additional details for an alert.

    1.  Select **Open**.

    2.  In the alert details window, review the following fields:

<table id="table_dql_dhd_ckc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Criticality

</td><td>

The criticality level of the alert. The levels are Low, Medium, and High.

</td></tr><tr><td>

Spend

</td><td>

The amount spent against the spend limit, in dollars.

</td></tr><tr><td>

Recommendations

</td><td>

Recommended next steps to prevent a potential AI spend overage. Review these steps to determine what actions you can take to stay within budget.-   **View spend**: View detailed spend and usage information by model, and then ask the entity to use a lower-cost model. Select a model name to view detailed usage for that entity and model. For more information, see
-   **Increase limit**: View the current spend limit and edit as needed.
-   **View users** \(not available for users\): View the current users with the highest spend. Select a user's name to view spend details.


</td></tr></tbody>
</table>6.  Remove an alert from the Alerts center view.

    If you no longer want to display an alert in the Alerts center view, you can remove it by expanding the actions drop-down menu and then selecting **Dismiss**.

    **Note:** Dismissing an alert removes it only from your view. It will still display to other users with access to the alert.


