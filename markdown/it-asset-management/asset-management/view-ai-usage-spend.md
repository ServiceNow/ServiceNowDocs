---
title: View your AI spend and usage
description: View and analyze your AI spend and usage so that you can optimize your AI licensing costs and plan for future AI investments. You can view your AI spend and usage by account, product, model, cost center, department, or user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/view-ai-usage-spend.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Monitoring your AI spend and usage, AI Cost Management, IT Asset Management, Asset Management]
---

# View your AI spend and usage

View and analyze your AI spend and usage so that you can optimize your AI licensing costs and plan for future AI investments. You can view your AI spend and usage by account, product, model, cost center, department, or user.

## Before you begin

Role required: ai\_cost\_admin

## About this task

**Note:** The AI Cost Management application populates AI spend in USD only.

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  In the navigation panel of the AI Cost Management application, select **Spend**.

3.  Select any tabs to view your AI spend and usage by entity type.\[Omitted image "aicm\_spend\_tabs.png"\] Alt text: Spend page with Account tab selected, showing tabs for Product, Model, Cost center, and Department.

    You can view total consumption spend, spend change from the prior period, subscription spend and seats, and total token usage. For accounts, cost centers, departments, and users, you can also view the current spend limit. Subscription spend and seats in not available for models.

    Filter your results by time period by using the time period drop-down list. The default time period is **This month**.

    **Note:** Imported entities that could not be normalized to ServiceNow data are bucketed into an Uncategorized entity.

4.  View additional details for a specific entity, such as an account or cost center.

    1.  Select the name of the entity that you want to view additional details for.

        The corresponding spend record opens.

    2.  Select any of the following tabs to drill down into additional details.\[Omitted image "aicm\_spend\_detail\_tabs.png"\] Alt text: Tabs used to filter spend details by overview, product, model, cost center, or department.

<table id="table_j2j_xrr_xjc"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Overview

</td><td>

View the overall AI spend and usage for the given entity. This tab contains the following widgets \(not all widgets display, depending on the entity type\):-   AI spend: General AI spend details for the given entity, including the total overall and daily or weekly spend.
-   Spend by vendor: Total AI spend by AI provider.
-   Spend by product: Total AI spend by AI application.
-   Spend by model: Total AI spend by AI model.
-   Top 5 movers: Top five accounts, products, models, cost centers, departments, and users with the highest overall AI usage.


</td></tr><tr><td>

Product

</td><td>

Drill down into the AI spend and usage for the given entity, by AI product.

</td></tr><tr><td>

Model

</td><td>

Drill down into the AI spend and usage for the given entity, by AI model.

</td></tr><tr><td>

Cost center

</td><td>

Drill down into the AI spend and usage for the given entity, by cost center.

</td></tr><tr><td>

Department

</td><td>

Drill down into the AI spend and usage for the given entity, by business department.

</td></tr><tr><td>

User

</td><td>

Drill down into the AI spend and usage for the given entity, by user.

</td></tr></tbody>
</table>
