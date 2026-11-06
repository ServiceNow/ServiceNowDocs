---
title: Add an Anthropic Claude Enterprise integration
description: Add an integration to track and monitor spend and usage for Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/add-integration-anthropic.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Anthropic, Claude, Integration]
breadcrumb: [Integrating with AI providers, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Add an Anthropic Claude Enterprise integration

Add an integration to track and monitor spend and usage for Claude.

## Before you begin

You must have an Claude API key generated from the Claude console, scoped to the following roles:

-   read:analytics
-   read:spend\_limits

Refer to the [Claude Platform Docs](https://platform.claude.com/docs/en/home) for more information.

**Note:** You can retrieve usage and cost data for Claude only if you have purchased an Enterprise plan.

Role required: ai\_cost\_admin

## About this task

Create an integration for each Claude account that you want to monitor.

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  From the navigation panel of the AI Cost Management application, navigate to **Settings** &gt; **Integrations**.

3.  Select **Add integration** and then select **Claude Enterprise**.

4.  In the Add Claude for enterprise account window, fill in the fields.

<table id="table_ft1_43d_jkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Claude account to use for the integration. You can use any name, but using the same account name as your Anthropic account makes reconciling records between Anthropic and AI Cost Management easier.

</td></tr><tr><td>

API key

</td><td>

API key that you generated in the Claude Console with the following roles:-   read:analytics
-   read:spend\_limits


</td></tr><tr><td>

Usage data range

</td><td>

Select the time period to import. Data is imported from the chosen start date to yesterday.This time period only affects the initial import. Future daily imports retrieve the last 31 days of data.

</td></tr></tbody>
</table>5.  Select **Add**.


## Result

The integration is added to the list of available integrations. After the integration successfully connects, the AI Cost Management application begins retrieving the relevant cost and usage data from Anthropic.

This retrieval happens daily at 02:00 UTC by default and updates the prior 31 days of data.

The Integrations page updates to show the status of importing usage data and user spend limits.

AI Cost Management also sets default spend limits and thresholds for you in the following manner:

-   The AI Cost administrator is set as the owner for the account.
-   The app calculates the monthly spend from the previous month for this account and sets that as the monthly spend limit. If there was no spend in the previous month, the spend limit is set to $0.00.
-   The app sets the organization monthly spend limit as the total of the monthly spend for all integrated accounts. When you change the spend limit for an account, the spend limit for the organization reflects that change.
-   User spend limits reflect the spend limits set in Anthropic.
-   The app creates two thresholds for each spend limit it created; one at 75% and one at 95%. Alerts are configured to be shown in the UI and to send an email.

These defaults are set only when you create an integration and don't update to reflect changes in spending. To edit the spend limits or to add spend limits at the cost center or department level, see [Set up an AI spend limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/set-up-spend-limits.md).

## What to do next

-   Edit the default spend limits. See [Set up an AI spend limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/set-up-spend-limits.md) for more information.
-   Track and monitor your spend and usage based on the data that you retrieve through the integration. For more details, see [View your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/view-ai-usage-spend.md).

**Note:** If you later want to modify any details of the existing integration, select the Edit icon \(\[Omitted image "edit-icon-task-settings-page.png"\]\) next to the account name in the list of available integrations. In the Edit Claude for enterprise account window, modify the integration details as needed and then select **Update**.

