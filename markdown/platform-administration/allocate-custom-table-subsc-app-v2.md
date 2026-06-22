---
title: Map custom tables to a product subscription in Subscription Management
description: Maintain accurate entitlement for custom tables in the global scope and stay in compliance by mapping the tables to a product subscription in Subscription Management. Mapping your custom tables keeps your custom table allotment updated and helps you avoid running out of custom table entitlements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/allocate-custom-table-subsc-app-v2.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing custom tables and apps, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Map custom tables to a product subscription in Subscription Management

Maintain accurate entitlement for custom tables in the global scope and stay in compliance by mapping the tables to a product subscription in Subscription Management. Mapping your custom tables keeps your custom table allotment updated and helps you avoid running out of custom table entitlements.

## Before you begin

Role required: usage\_admin, sn\_sub\_man.admin, or admin

## Procedure

1.  Navigate to the **Issues** tab in Subscription Management in one of the following ways.

    -   Navigate to **Admin** &gt; **Subscription Management** &gt; **Issues**.
    -   Navigate to **All** &gt; **Subscription Management** &gt; **Issues**.
2.  In the **Unmapped global custom tables** tab, look for custom tables that aren't mapped to a subscription.

3.  Update your entitlements by mapping one or more custom tables to a recommended product or a product of your choice.

    When possible, Subscription Management displays recommendations for product subscriptions with available custom table entitlements in the **Recommended Product** column. Subscription Management can't display product subscription recommendations for some unmapped custom tables, which therefore aren't shown in the **Unmapped custom applications** tab. For more information about mapping missing custom tables to product subscriptions, see [Map a missing custom table to a product subscription in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/map-missing-custom-table-sub-mgt.md)

<table id="choicetable_iph_zpv_2yb"><thead><tr><th align="left" id="d43920e145">

Option

</th><th align="left" id="d43920e148">

Description

</th></tr></thead><tbody><tr><td id="d43920e154">

**Map to a recommended product**

</td><td>

1.  Select the check box next to one or more unmapped custom tables.
2.  Select **Map to product**.
3.  Select **Save**.


</td></tr><tr><td id="d43920e181">

**Map to a product of your choice**

</td><td>

1.  Select an unmapped custom table.
2.  In the **Subscription** lookup list on the Custom Table Inventory form, select the subscription.
3.  Select **Update**.
4.  Repeat these steps for each remaining unmapped table.


</td></tr><tr><td id="d43920e211">

**Manually map to a product through the Custom Applications table**

</td><td>

If subscription recommendations shown in the Subscription Management UI aren't correct for your environment, you can manually update custom table mappings.1.  From the platform's application navigator, select **All**.
2.  In the navigation filter, enter `sys_app.list`.
3.  Select the Update Personalized List icon \[Omitted image "gear.png"\] Alt text:.
4.  Move **Subscription\(subscription\_entitlement\)** from the **Available** column to the **Selected** column.
5.  Select **OK**.
6.  Find and select the record for the custom table you want to map.
7.  In the **Subscription** field, find and select the product subscription the table should be mapped to.
8.  Select **Save**.


</td></tr></tbody>
</table>
## Result

One or more custom tables are mapped to a product subscription and your custom table entitlement count is updated. If you mapped a custom table to a subscription through the Custom Table Inventory form, Subscription Management is updated the next day.

**Parent Topic:**[Managing custom tables and applications in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/allocating-custom-tables-subscr-apps-v2.md)

