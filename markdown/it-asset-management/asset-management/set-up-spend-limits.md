---
title: Set up an AI spend limit
description: Spend limits define the maximum amount of consumption AI spend permitted each month. Align this spend limit with your organization's AI budget thresholds.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/set-up-spend-limits.html
release: australia
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Set up an AI spend limit

Spend limits define the maximum amount of consumption AI spend permitted each month. Align this spend limit with your organization's AI budget thresholds.

You can set spend limits for consumption AI accounts, cost centers, and departments. You can also set thresholds as percentages of that spend limit. User spend limits are imported directly from Anthropic, but you can set thresholds for the spend in AI Cost Management.

When you integrate with a new consumption account, AI Cost Management creates default spend limits and thresholds for you in the following manner:

-   The AI Cost administrator is set as the owner for the account.
-   The app totals the monthly from the previous month for the selected account and sets that as the monthly spend limit. If there was no spend in the previous month, the spend limit is set to $0.00.
-   The app sets the organization monthly spend limit as the total of the monthly spend for all accounts. When you change the spend limit for an account, the spend limit for the organization reflects that change.
-   User spend limits reflect the spend limits set in Anthropic.
-   The app creates two thresholds for each spend limit it created; one at 75% and one at 95%. Alerts are configured to be shown in the UI and to send an email.

These defaults are set only when you create an integration and don't update to reflect changes in spending.

**Note:** Spend limits aren't enforced and don't block AI usage. They are used only for alerting purposes.

AI Cost Management evaluates the percentage of spend every three hours. When that percentage exceeds a threshold, the application generates an alert. You can configure notification of the alert to be in the UI, by email, or both. The notification is available and sent to the owner of the account and the owner of the entity that reached the threshold. For more information on AI spend alerts, see [Review AI spend alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/review-resolve-alerts.md)

Alerts are cleared on the 10th day of the month and clear the previous month's alerts.

**Note:** User spend limits are imported directly from Anthropic.

