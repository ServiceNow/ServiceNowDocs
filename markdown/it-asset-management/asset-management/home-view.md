---
title: Home view in the AI Cost Management application
description: The Home view is the landing page of the AI Cost Management application. This view provides an overview of key AI spend metrics to help you understand your overall AI spend and usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/home-view.html
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Views in AI Cost Management, Explore, AI Cost Management, IT Asset Management, Asset Management]
---

# Home view in the AI Cost Management application

The Home view is the landing page of the AI Cost Management application. This view provides an overview of key AI spend metrics to help you understand your overall AI spend and usage.

You can use the Home view to perform the following tasks:

-   View the total overall spend across your AI providers.
-   View the highest usages of your AI providers by account, product, model, cost center, department, and user.
-   View alerts for AI spend that approaches or exceeds your defined thresholds on spend limits.

\[Omitted image "aicm\_home.png"\] Alt text: Dashboard displaying total AI consumption spend, action items, trend chart, and breakdown by subscriptions and vendors.

The Home view is the first view that opens when you launch the AI Cost Management application. To navigate back to the Home view from any other view, select **Home** in the navigation panel of the application.

You can also filter your results by time period by using the time period drop-down list. The default time period is **This month**.

<table id="table_xtz_jy5_kkc"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Top action items

</td><td>

Alerts triggered when consumption-based AI spend has exceeded the spend limit thresholds that you have defined. Each alert displays the following information:-   The criticality level of the alert. The levels are Low, Medium, High, and Critical.
-   The amount of time that has elapsed since the alert was triggered.
-   The alert category, such as Account, Cost Center, Department, or User.
-   The affected entity, such as a specific user or cost center.
-   The amount spent against the spend limit, in both percentage and dollars.

You can filter the alerts based on the criticality level by selecting an option from the **Criticality** drop-down menu. You can also perform additional actions by using the actions drop-down menu in each alert:-   To view detailed spend and usage information for the affected entity, select **Open**.
-   To remove the alert from your view, select the drop-down menu and then select **Dismiss**.

</td></tr><tr><td>

Consumption spend

</td><td>

Total overall spend across your consumption-based AI accounts. The AI Cost Management application calculates this spend based on your token consumption.**Note:** You can currently view the total spend for Claude only.

</td></tr><tr><td>

Subscriptions

</td><td>

Total spend across subscription accounts. Use the toggle to view the number of seats. By default, the widget shows the entitlement amount or number of sets. Use the dropdown menu to instead view by assigned or unassigned amount or seats.

</td></tr><tr><td>

Consumption

</td><td>

Total consumption spend broken down by product.

</td></tr><tr><td>

Consumption breakdown

</td><td>

Breakdown of consumption spend. Use the toggle to change the Y axis.

</td></tr><tr><td>

Top consumption spenders

</td><td>

Top five accounts, products, models, cost centers, departments, and users with the highest overall AI usage.Select an entity's link, such as department or user name, to drill down into details of their spend. See [View your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/view-ai-usage-spend.md) for more information.

</td></tr></tbody>
</table>