---
title: Record the usage on the entitlement
description: Record the consumption or usages made out of the total characteristic quantities allotted for an entitlement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/record-usage-entitlement.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Record the usage on the entitlement

Record the consumption or usages made out of the total characteristic quantities allotted for an entitlement.

## Before you begin

Role required: sn\_customerservice\_manager, sn\_customerservice\_agent, sn\_customerservice.consumer\_agent, or sn\_bus\_loc.svc\_location\_support\_agent

**Note:** For details on which entitlements, a user with sn\_bus\_loc.svc\_location\_support\_agent role can edit entitlement usage, see [Location Support Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/configure-data-model-roles.md#entry-lsa-role).

## About this task

When an entitlement moves to the Active state, usage records are created. You can update the usage records on the basis of units or quantities used as and when the customer uses the services. For example, if a characteristic includes 50 visits to the customer, then the Total units field displays 50 and the Used units field is updated after each visit. Managers can create and update usage records for an entitlement but agents can only update the Used units field.

## Procedure

1.  Navigate to the ServiceNow AI Platform interface or the CRM Workspace.

<table id="choicetable_m1c_yvj_d1c"><thead><tr><th align="left" id="d186931e72">

Interface

</th><th align="left" id="d186931e75">

Action

</th></tr></thead><tbody><tr><td id="d186931e81">

**Platform interface**

</td><td>

Navigate to **All** &gt; **Customer Service** &gt; **Contracts and Entitlements** &gt; **Customer Contracts**.

</td></tr><tr><td id="d186931e105">

**CRM Workspace**

</td><td>

-   Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **CRM Workspace**.
-   In the list view, navigate to **Contracts and Entitlements** &gt; **Entitlements**.


</td></tr></tbody>
</table>2.  Record the usage on an entitlement.

<table id="choicetable_zqd_tnc_pzb"><thead><tr><th align="left" id="d186931e158">

From

</th><th align="left" id="d186931e161">

Do this

</th></tr></thead><tbody><tr><td id="d186931e167">

**Customer Contracts**

</td><td>

1.  Select the contract that has the entitlement that you want to track the usage on.
2.  From the Customer Contract Lines related list, select the contract line that has the entitlement.
3.  From the Entitlements related list, select the entitlement.
4.  From the Entitlement Usages related list, open the usage record.


</td></tr><tr><td id="d186931e191">

**Entitlements**

</td><td>

1.  Select the entitlement that you want to track the usage on.
2.  From the Entitlement Usages related list, open the usage record.


</td></tr></tbody>
</table>3.  On the Entitlement Usage form, fill in the **Used units** field.

4.  Select **Update**.

5.  On the Entitlement page, select **Update** to save the entitlement.

    If you have used the Customer Contracts menu to record the usage, then select **Update** to save the contract line and then the customer contract.


**Parent Topic:**[Using Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-post-sales-support.md)

