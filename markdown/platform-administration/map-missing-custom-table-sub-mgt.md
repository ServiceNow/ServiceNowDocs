---
title: Map a missing custom table to a product subscription in Subscription Management
description: Map a custom table in the global scope to a product subscription when that table isn't shown in the Unmapped global custom tables tab of Subscription Management. To stay in compliance, all custom tables must be mapped to a product subscription.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Map a missing custom table to a product subscription in Subscription Management

Map a custom table in the global scope to a product subscription when that table isn't shown in the **Unmapped global custom tables** tab of Subscription Management. To stay in compliance, all custom tables must be mapped to a product subscription.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## About this task

Subscription Management can't display product subscription recommendations for some unmapped global custom tables, and those tables aren't shown in the **Unmapped global custom tables** tab. As a result, you might see fewer tables in the **Unmapped global custom tables** tab than the number shown on the Unmapped Global Custom Tables report in the Subscription Management Overview page. You can map any missing custom tables to product subscriptions from the Custom Table Inventory list.

## Procedure

1.  Navigate to the **Issues** tab in Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Issues**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Issues**.
2.  Select the **Unmapped global custom tables** tab.

3.  Select **Map missing tables from custom table inventory list**.

4.  If the Custom Table Inventory list is in the default view, select **Custom Table Inventory** &gt; **View** &gt; **Subscription Entitlement**.

    In the **Subscription** column, you can see which product subscriptions each of your custom tables are mapped to.

5.  Select an unmapped custom table.

    You can identify unmapped custom tables using the **Subscription** column. The **Subscription** column for unmapped custom tables is empty.

6.  In the **Subscription** lookup list on the Custom Table Inventory form for the table, select a product subscription.

7.  Select **Update**


## Result

One or more custom tables are mapped to a product subscription and your custom table entitlement count is updated. Updates made through the Custom Table Inventory form show in Subscription Management the next day.

**Parent Topic:**[Managing custom tables and applications in Subscription Management](../concept/allocating-custom-tables-subscr-apps-v2.md)

