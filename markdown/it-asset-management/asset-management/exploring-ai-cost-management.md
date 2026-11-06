---
title: Exploring AI Cost Management
description: The AI Cost Management application provides a central location for monitoring and analyzing your organization's AI spend and usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/exploring-ai-cost-management.html
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [AI Cost Management, IT Asset Management, Asset Management]
---

# Exploring AI Cost Management

The AI Cost Management application provides a central location for monitoring and analyzing your organization's AI spend and usage.

## AI Cost Management overview

The AI Cost Management application enables you to monitor and analyze spend and usage across your AI accounts from a single location. The app retrieves, processes, and displays cost and usage data for both consumption accounts, such as Anthropic Claude, and subscription accounts, such as Microsoft Copilot.

\[Omitted image "aicm\_home.png"\] Alt text: Dashboard displaying total AI consumption spend, action items, trend chart, and breakdown by subscriptions and vendors.

When you integrate AI Cost Management with an external AI provider, you can view your current spend across different accounts, products, models, cost centers, departments, and users. You can drill down to view details. For example, you can view spend for a department or a user, broken down by product.

For consumption accounts, you can set spend limits on usage by account, cost center, and department. User spend limits are set in Anthropic. You can then set up alerts that trigger when an entity, such as a department or user, exceeds a specified percentage of its spend limit.

You can use this data to track your AI spend trends month over month.

**Note:** Spend limits aren't enforced and don't block AI usage. They are used only for alerting purposes.

AI Cost Management supports the following account integrations:

-   Anthropic Claude Enterprise
-   Microsoft Copilot

## AI Cost Management users

<table id="table_hv5_ghd_xjc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI cost administrator

</td><td>

AI cost administrators:-   Create and manage integrations to retrieve usage and cost data from the corresponding AI providers.
-   Set consumption spend limits across an organization and configure thresholds that send alert notifications when exceeded.

**Note:** User spend limits are imported directly from Anthropic.

-   Monitor the AI spend and usage across an organization.

</td></tr></tbody>
</table>## AI Cost Management workflow

1.  Strategic planners and finance team members define AI spend limits for each AI account that their organization owns.
2.  An AI cost administrator sets up integrations between the AI Cost Management application and the providers of each supported AI account. These integrations enable the AI Cost Management application to retrieve cost and usage data from the AI provider.
3.  After each integration connects successfully, the AI Cost Management application begins retrieving the associated cost and usage data.
4.  The application processes and normalizes the data and then populates the corresponding spend records and charts.
5.  The AI cost administrator sets up spend limits based on the defined AI budgets. Each spend limit specifies the maximum amount of AI spend for each month. The administrator then sets a threshold as a percentage of the spend limit. If the spend exceeds the specified threshold, an alert triggers.
6.  An AI cost administrator reviews and analyzes the data in the corresponding spend records and charts. They can use the findings to identify AI spend trends, optimize AI costs, and plan future AI investments.
7.  When spend exceeds a specified threshold, the owner of the account, cost center, or department receives an alert. An AI cost administrator can review the alert details to take the necessary steps to mitigate any potential overages.

## AI Cost Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|View your AI spend and usage in AI Cost Management views.|[Views in AI Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/ai-cost-management-views.md)|AI cost administrators|
|Monitor spend and track usage for your AI accounts.|[Monitoring your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/monitoring-ai-usage-spend.md)|AI cost administrators|
|Set up consumption spend limits at the account, cost center, and department level.|[Set up an AI spend limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/set-up-spend-limits.md)|AI cost administrators|
|Review and resolve alerts that trigger when spend exceeds a threshold.|[Review AI spend alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/review-resolve-alerts.md)|AI cost administrators|
|Integrate with AI provider accounts to retrieve cost and usage data for your AI applications.|[Integrating with AI providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/integrating-ai-saas-providers.md)|AI cost administrators|

## What to explore next

To learn more about configuring and using AI Cost Management, see:

-   [Configuring AI Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/configuring-ai-cost-management.md)
-   [Monitoring your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/monitoring-ai-usage-spend.md)
-   [Integrating with AI providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/integrating-ai-saas-providers.md)
-   [AI Cost Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/ai-cost-management-references.md)

