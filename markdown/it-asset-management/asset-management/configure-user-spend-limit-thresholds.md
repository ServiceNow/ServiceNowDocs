---
title: Configure user spend limit thresholds
description: Add thresholds for user consumption spend limits that generate alerts when the threshold is exceeded.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/configure-user-spend-limit-thresholds.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [Set up an AI spend limit, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Configure user spend limit thresholds

Add thresholds for user consumption spend limits that generate alerts when the threshold is exceeded.

## About this task

You configure user spend limits directly in Anthropic. AI Cost Management ingests and displays these limits. However, you can configure thresholds on those limits to generate alerts when they are exceeded.

## Before you begin

You must have integrated with at least one consumption AI account. See [Integrating with AI providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/integrating-ai-saas-providers.md) for more information.

Role required: ai\_cost\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  From the navigation panel of the AI Cost Management application, navigate to **Settings** &gt; **Spend limits**.

3.  Select the **User** tab.

4.  Select the **Edit** icon for the account.

5.  In the **Edit user limit** dialog, enter the following:

<table id="table_ixw_mdr_skc"><tbody><tr><td>

**Alert thresholds**

</td><td>

Select a percentage of the spend limit that will trigger an alert when exceeded.You can create more than one threshold \(limit is 2\). An alert is generated when each threshold is exceeded.

</td></tr><tr><td>

**Notification**

</td><td>

Select **Email** to have an email sent to the configured owner when the threshold is exceeded. Select **in-product** to have an alert displayed in the Alerts Center.

</td></tr></tbody>
</table>6.  Select **Update**.


