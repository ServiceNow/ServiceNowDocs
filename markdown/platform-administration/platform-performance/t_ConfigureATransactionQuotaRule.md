---
title: Configure a transaction quota rule
description: Transaction quota rules allow you to define a quota policy for different types of transactions.
locale: en-US
release: australia
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Transaction quotas, Configure, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Configure a transaction quota rule

Transaction quota rules allow you to define a quota policy for different types of transactions.

## Before you begin

Role required: admin

## About this task

Transaction quota rules allow you to specify the following conditions.

-   The conditions under which the policy applies.
-   The order in which transaction quotas apply.
-   The maximum duration of a transaction before the quota manager cancels it.

Before setting transaction quotas, navigate to **All** &gt; **User Administration** &gt; **Active Transactions** to review the normal transaction activities for your instance. You can [view and terminate long-running transactions](t_ViewAndKillAnActiveTransaction.md) if necessary. Over time, you can determine the normal transaction load for your instance and set your quotas to match these norms.

**Warning:** Setting transaction quotas too low can severely impact your users and prevent normal instance operations. Test your transaction quotas rigorously before implementing them in production.

## Procedure

1.  If necessary, activate the Transaction Quotas plugin.

    To verify whether the Transaction Quotas plugin is already active, navigate to **Admin** &gt; **Application Manager** and search for Transaction Quotas in Application Manager. If the plugin is included in the **Installed** tab, it is already activated.

2.  Navigate to **All** &gt; **System Definition** &gt; **Quota Rules**.

3.  Click **New**.

4.  On the Transaction Quota Rule form, fill in the fields.

    For a description of the field values, see [Transaction quota rule form](../reference/transaction-quota-rule-form.md).

5.  Set a condition to specify when the transaction quota should take effect.

    The transaction quota rule condition builder displays conditions that are only applicable to transactions. For a description of the condition builder options, see [Transaction quota rule condition builder](../reference/transaction-quota-condition-builder.md).

6.  Select **Submit**.


**Parent Topic:**[Maintaining and monitoring the ServiceNow AI Platform](../../general/concept/maintain-monitor-now-platform.md)

**Related topics**  


[Optimize widget rendering time on responsive dashboards](https://www.servicenow.com/docs/access?context=t_optimizeWidgetRenderingTime&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

