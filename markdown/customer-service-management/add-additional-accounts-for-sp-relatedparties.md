---
title: Add additional accounts for the sold product
description: Add additional accounts or contacts for your business-to-business \(B2B\) or business-to-business-to-consumer \(B2B2C\) sold products by defining the type and responsibility of additional accounts or contacts. Once you add accounts as related parties, all contacts associated with the related party account can access the sold product.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Adding related parties to a sold product, Using customer access management, Customer management, Use, Customer Service Management]
---

# Add additional accounts for the sold product

Add additional accounts or contacts for your business-to-business \(B2B\) or business-to-business-to-consumer \(B2B2C\) sold products by defining the type and responsibility of additional accounts or contacts. Once you add accounts as related parties, all contacts associated with the related party account can access the sold product.

## Before you begin

Role required: admin and sn\_customerservice\_manager

## About this task

The responsibility assigned to the additional accounts that is associated with a sold product gets access to the sold product and the related entities, which include installed products, install base items, and cases associated with sold products.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Products** &gt; **Sold Products**.

2.  Select the record that you want to add the additional account to.

3.  From the Sold Product Related Parties related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_esz_qdw_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sold Product

</td><td>

Products and components that are sold to an account.

</td></tr><tr><td>

Type

</td><td>

Related party type.**Note:** By selecting the related party type, the default responsibility that is mentioned in the type is added in the related party responsibility.

</td></tr><tr><td>

Account

</td><td>

Contacts of the account responsible for the sold product.

</td></tr><tr><td>

Responsibility

</td><td>

Access level to the sold product and related information.Additional account with the Authorized Account responsibility requires the sn\_install\_base.sold\_product\_authorized\_contact role to get access to the associated sold product and related entities. For details, see [Roles installed with customer access management](../reference/r_rolesinstalledwithcustaccessmgmt.md).

 **Note:** If the **Responsibility** field is empty, the accounts don't have any access to the sold product and associated case.

</td></tr><tr><td>

Order

</td><td>

Specifies the sequence in which records are displayed, organized according to business preferences.

</td></tr></tbody>
</table>5.  Select **Submit**.

    You can add additional accounts to the B2B sold product.

    **Note:** Added accounts can be from the same account, partner account, or from contact relationships.


## Result

After additional accounts are added to the sold product with Authorized Account responsibility, the contacts of those accounts having a required functional role can perform the following actions:

-   View the list of sold products and associated install base items.
-   Create cases by selecting sold products or install bases.
-   View the list of cases that are related to the sold products or affected install bases.
-   View the list of installed products.
-   Access cases that are associated with the sold product.

**Note:**

-   While creating a case for a sold product, you can only see the authorized accounts on the account's sold product.
-   If you choose an account, you can only associate a sold product that you have full access to on the case.

