---
title: Configure an account spend limit
description: Create spend limits for individual consumption AI accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/configure-an-account-spend-limit.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [Set up an AI spend limit, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Configure an account spend limit

Create spend limits for individual consumption AI accounts.

## Before you begin

You must have integrated with at least one consumption AI account. See [Integrating with AI providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/integrating-ai-saas-providers.md) for more information.

Role required: ai\_cost\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  From the navigation panel of the AI Cost Management application, navigate to **Settings** &gt; **Spend limits**.

    The Account tab displays by default showing the accounts that you have integrated with. The organization-wide spend limit is derived as the total of all account spend limits.

3.  Set an account spend limit.

    1.  Select the **Edit** icon for an account.

    2.  In the **Edit account** dialog, enter the following:

<table id="table_uv1_kpq_skc"><tbody><tr><td>

**Owner**

</td><td>

Search for and select the person who should own the spend for this account.

</td></tr><tr><td>

**Spend limit**

</td><td>

Enter a dollar amount for the monthly spend limit for this account.

</td></tr><tr><td>

**Alert thresholds**

</td><td>

Select a percentage of the spend limit that will trigger an alert when exceeded.You can create more than one threshold \(limit is two\). An alert is generated when each threshold is exceeded.

</td></tr><tr><td>

**Notification**

</td><td>

Select **Email** to have an email sent to the configured owner when the threshold is exceeded. Select **in-product** to have an alert displayed in the Alerts Center.

</td></tr></tbody>
</table>4.  Select **Add**.


## Result

The account shows a monthly spend limit and configured thresholds. The organization-wide spend limit updates to the new total of all account spend limits.

