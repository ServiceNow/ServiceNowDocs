---
title: Map spend categories to product categories manually
description: You can manually map spend categories to product categories to better organize and manage your organization’s expenses by grouping similar goods or services into logical categories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/map-spend-product-categories.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Spend and Savings Management, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Map spend categories to product categories manually

You can manually map spend categories to product categories to better organize and manage your organization’s expenses by grouping similar goods or services into logical categories.

## Before you begin

Role required: sn\_spend\_mgmt.category\_manager\_admin

## Procedure

1.  Navigate to **All** &gt; **Spend and Savings Management** &gt; **Spend Categories**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Category name|Name of the spend category.|
    |Category code|Code of the spend category.|
    |Spend category manager|Name of the spend category manager.|
    |Parent spend category|Category that contains more specific child categories or subcategories of spend.|
    |Sourcing manager|Name of the sourcing manager.|

4.  Select **Submit**.

    The Child Spend Categories, Product Categories, and Ledger Assignment Rules related lists appear.\[Omitted image "spend-prod-cat-map.png"\] Alt text: The Child Spend Categories, Product Categories, and Ledger Assignment Rules related lists appear on the Spend Category page.

5.  Do the following:

<table id="table_vxz_42c_y2c"><thead><tr><th>

To

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Create child spend categories

</td><td>

1.  Select the **Child Spend Categories** related list, and select **New**.
2.  On the form, fill in the fields.

The **Parent spend category** field is auto-populated.

See [step 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/map-spend-product-categories.md) for a description of the field values on the Spend category form.

</td></tr><tr><td>

Create product categories

</td><td>

1.  Select the **Product Categories** related list and select **Edit**.
2.  In the collection list pop up window, do one of the following to move the categories to the Product Categories List

    -   Select a category and then click the right arrow icon \(\[Omitted image "right-arrow-icon.png"\] Alt text: Right arrow icon.\) icon.
    -   Double-click a category.
**Note:** In the Collection list, you can search for product categories by entering the category name or by using wild cards \(\*\).

3.  Select **Save**.


</td></tr><tr><td>

Create ledger assignment rules

</td><td>

Select the **Ledger Assignment Rules** related list and select **New**. For more information, see [Create ledger assignment rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/create-ledger-assignment-rules.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Spend and Savings Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/using-spend-mgmt.md)

**Related topics**  


[Map spend categories to product categories using an Excel file]()

[Action or dismiss a savings opportunity]()

