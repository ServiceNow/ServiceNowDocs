---
title: Configure a cost center or department spend limit
description: Create a consumption spend limit for a cost center or a department.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/configure-a-cost-center-spend-limit.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
breadcrumb: [Set up an AI spend limit, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Configure a cost center or department spend limit

Create a consumption spend limit for a cost center or a department.

## Before you begin

You must have integrated with at least one consumption AI account. See [Integrating with AI providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/integrating-ai-saas-providers.md) for more information.

Role required: ai\_cost\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  From the navigation panel of the AI Cost Management application, navigate to **Settings** &gt; **Spend limits**.

3.  Select the **Cost center** or **Department** tab.

4.  Use the **Cost center** or **Department** drop-down to select the entity.

    Entities that already have spend limits are shown by selecting the **Configured** tab.

    1.  To select a new entity, select **Not configured** and then search for or scroll to find it.

    2.  Select **Add account** to select the account to associate with this spend limit.

    3.  In the **Add account** dialog, enter the following:

<table id="table_uv1_kpq_skc"><tbody><tr><td>

**Account**

</td><td>

Select the AI account to associate with this cost center or department. Any spend made by the entity on this account will roll up to the total spend for the account.

</td></tr><tr><td>

**Owner**

</td><td>

Search for and select the person who should own the spend for this entity.

</td></tr><tr><td>

**Spend limit**

</td><td>

Enter a dollar amount for the monthly spend limit for this entity on this account.

</td></tr><tr><td>

**Alert thresholds**

</td><td>

Select a percentage of the spend limit that will trigger an alert when exceeded.You can create more than one threshold \(limit is two\). An alert is generated when each threshold is exceeded.

</td></tr><tr><td>

**Notification**

</td><td>

Select **Email** to have an email sent to the configured owner when the threshold is exceeded. Select **in-product** to have an alert displayed in the Alerts Center.

</td></tr></tbody>
</table>5.  Select **Add**.


## Result

The entity now has an associated spend limit.

To configure a spend limit for the same entity, but for a different AI account, repeat the procedure and select a different account when configuring the spend limit. You can see the spend for the separate accounts when you drill-down into the entity's spend. See [View your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/view-ai-usage-spend.md) for more information.

