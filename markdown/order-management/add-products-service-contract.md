---
title: Add a sold product or install base item to a customer contract
description: Add the sold products or the install base items covered to customer contracts, contract lines, or entitlements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Contracts and Entitlements, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Add a sold product or install base item to a customer contract

Add the sold products or the install base items covered to customer contracts, contract lines, or entitlements.

## Before you begin

Role required: sn\_customerservice\_manager

## About this task

Sold products are products and components that have been sold to an account or a consumer and can have multiple contracts. An install base item is an instance of sold product that has been provisioned for an account or consumer.

Associating sold products or install base items to a Customer Contracts and Entitlements entity helps keep a track of the products or install base items that are serviced to a customer under that entity.

A sold product or an install base item can be added to a Customer Contracts and Entitlements entity in the Draft, Active, or Suspended states.

**Note:** If an entity is deleted, the related sold product or install base item covered is also deleted.

## Procedure

1.  Navigate to the ServiceNow AI Platform interface or the CSM Configurable Workspace.

<table id="choicetable_zqd_tnc_pzb"><thead><tr><th align="left" id="d87313e88">

Interface

</th><th align="left" id="d87313e91">

Action

</th></tr></thead><tbody><tr><td id="d87313e97">

**ServiceNow AI Platform interface**

</td><td>

Navigate to **All** &gt; **Customer Service** &gt; **Contracts and Entitlements**.

</td></tr><tr><td id="d87313e120">

**CSM Configurable Workspace**

</td><td>

-   Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** &gt; **CSM Configurable Workspace**.
-   In the list view, navigate to **Contracts and Entitlements**.


</td></tr></tbody>
</table>2.  Add the sold product or install base item covered to customer contracts, contract lines, or entitlements.

<table id="choicetable_zqd_tnc_pzb1"><thead><tr><th align="left" id="d87313e170">

Add to

</th><th align="left" id="d87313e173">

Procedure

</th></tr></thead><tbody><tr><td id="d87313e179">

**Customer Contracts**

</td><td>

1.  In the list view, navigate to **Contracts and Entitlements** &gt; **Customer Contracts**.

**Note:** In the ServiceNow AI Platform interface, select **Customer Contracts** in the navigation menu.

2.  Select the customer contract that you want to add the sold product or install base item to.
3.  From the Products Covered or Install Base Items Covered related list, select **New**.


</td></tr><tr><td id="d87313e220">

**Customer Contract Lines**

</td><td>

1.  In the list view, navigate to **Contracts and Entitlements** &gt; **Customer Contracts**.

**Note:** In the ServiceNow AI Platform interface, select **Customer Contracts** in the navigation menu.

2.  Select the customer contract that has the required contract line.
3.  From the Customer Contract Lines related list, select the contract line that you want to add the sold product or install base item covered to.
4.  From the Sold Product Covered or Install Base Items Covered related list, select **New**.
 **Note:** When a sold product or an install base item covered is added to a contract line, it is not added to the related entitlements.

</td></tr><tr><td id="d87313e267">

**Entitlements**

</td><td>

1.  In the list view, navigate to **Contracts and Entitlements** &gt; **Customer Contracts**.

**Note:** In the ServiceNow AI Platform interface, select **Customer Contracts** in the navigation menu.

2.  Select the customer contract that has the required contract line.
3.  From the Customer Contract Lines related list, select the contract line that has the required entitlement.
4.  From the Entitlements related list, select the entitlement that you want to add the sold product or install base item to.
5.  From the Sold Product Covered or Install Base Items Covered related list, select **New**.
 You can also directly navigate to Entitlements form as follows:

 1.  In the list view, navigate to **Contracts and Entitlements** &gt; **Entitlements**.

**Note:** In the ServiceNow AI Platform interface, select **Entitlements** in the navigation menu.

2.  Select the entitlement that the sold product or install base item must be added to.
3.  From the Sold Product Covered or Install Base Items Covered related list, select **New**.


</td></tr></tbody>
</table>    **Note:**

    -   You can either add a sold product or an install base item to the Customer Contracts and Entitlements entity.
    -   The state of the entity shouldn't be Expired or Canceled.
3.  On the Sold Product Covered form, fill in the fields.

    For a description of the field values, see [Sold product form](https://www.servicenow.com/docs/access?context=sold-product-form&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

4.  Select **Submit**.


**Parent Topic:**[Using Customer Contracts and Entitlements](../concept/using-post-sales-support.md)

