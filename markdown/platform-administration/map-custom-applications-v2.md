---
title: Map a custom application to a product subscription in Subscription Management
description: Maintain accurate entitlement for custom tables in a scoped application by mapping the application to a product subscription in Subscription Management. To stay in compliance, you must map custom tables to a product subscription.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Map a custom application to a product subscription in Subscription Management

Maintain accurate entitlement for custom tables in a scoped application by mapping the application to a product subscription in Subscription Management. To stay in compliance, you must map custom tables to a product subscription.

## Before you begin

Role required: usage\_admin or admin

## About this task

As your developers create and deploy new custom applications and tables on your instances, use Subscription Management to map them to subscriptions. After you map a custom application to a product subscription, additional tables that developers add to the application are automatically mapped to the subscription.

## Procedure

1.  Navigate to the **Issues** tab in Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Issues**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Issues**.
2.  In the **Unmapped custom applications** tab, look for custom applications that aren't mapped to a subscription.

3.  Update your entitlements by mapping one or more custom applications to a recommended product or a product of your choice.

    Subscription Management recommends product subscriptions with available custom table entitlements in the **Recommended Product** column.

<table id="choicetable_nbw_q4g_cyb"><thead><tr><th align="left" id="d173069e135">

Option

</th><th align="left" id="d173069e138">

Description

</th></tr></thead><tbody><tr><td id="d173069e144">

**Map to a recommended product**

</td><td>

1.  Select the check box next to one or more unmapped custom applications.
2.  Select **Map to product**.
3.  Select **Confirm**.


</td></tr><tr><td id="d173069e171">

**Map to a product of your choice**

</td><td>

1.  Select an unmapped custom application.
2.  On the Custom Application form, select a subscription in the **Subscription** lookup list.

**Note:** The lookup list does not include expired, grandfathered, or Store application subscriptions. If you have a store application with custom tables that must be mapped to a subscription, select a subscription with a custom table entitlement.

3.  Select **Update**.


</td></tr></tbody>
</table>
## Result

One or more custom applications are mapped to a product subscription and your custom table entitlement count is updated.

**Parent Topic:**[Managing custom tables and applications in Subscription Management](../concept/allocating-custom-tables-subscr-apps-v2.md)

