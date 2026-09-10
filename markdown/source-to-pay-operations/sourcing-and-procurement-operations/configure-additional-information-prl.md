---
title: Configure line-level questions in ShoppingHub
description: Create configurable, line-level questions for shoppers to provide the information needed to complete the purchase during the checkout process in Shopping Hub. These questions are defined in Catalog Builder and specific to certain products or product categories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/configure-additional-information-prl.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-08-07"
reading_time_minutes: 3
breadcrumb: [Complete your checkout, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure line-level questions in ShoppingHub

Create configurable, line-level questions for shoppers to provide the information needed to complete the purchase during the checkout process in Shopping Hub. These questions are defined in Catalog Builder and specific to certain products or product categories.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

Plugin required: Shopping Hub \(sn\_spend\_uib\)

Create a custom set of questions to ask shoppers during the quick and full checkout for specific products or product categories using a record producer. Build the record producer in Catalog Builder using the **ShoppingHub: Additional information on supplier products or product models or product categories** template. For information on how to create a record producer, see [Create a catalog item using a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-item-cat-builder.md).

\[Omitted image "sh-addl-catalog.png"\] Alt text: ShoppingHub additional information for supplier product.

Shopping Hub checks for the existence of the record producer used for the additional information configuration in the specified order:

-   Supplier product
-   Product model
-   Product category
-   Parent category
-   Supplier\(s\)

**Note:** Shopping Hub applies the **Supplier\(s\)** filter differently depending on which type of match is found:

-   For a Product model, Product category, or Parent category match, the **Supplier\(s\)** field, if set on the configuration, further restricts the question set to products from those suppliers. If **Supplier\(s\)** is empty on the configuration, the question set applies to products from any supplier.
-   For a Supplier product match, **Supplier\(s\)** is not evaluated, because a supplier product is already specific to a single supplier.
-   If none of the above match, Shopping Hub makes one more attempt: it looks for a configuration that has **Supplier\(s\)** set but no **Supplier product**, **Product model**, or **Product category**, and applies its question set to any product from that supplier.

For example, if a configuration has **Product category** set to Name Badge and **Supplier\(s\)** set to Banner, the question set applies only to Name Badge products supplied by Banner. A Name Badge product supplied by Office Depot would not receive this question set unless a separate configuration matches it.

## Procedure

1.  Navigate to one of the following:

    -   **All** &gt; **Sourcing and Purchasing Automation**, **Primary Data**, or **Supplier Product**
    -   **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Model Categories**
    -   **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **All Models**
2.  Select and open a record for a supplier product, product model, or a model category.

3.  In the **Related Links** section, select **Add additional information**.

    \[Omitted image "sh-addl-info.png"\] Alt text: Add additional information option in Related Links.

    The Create record producer page opens in Catalog Builder.

4.  In Catalog Builder, configure a record producer using the **ShoppingHub: Additional information on supplier products or product models or product categories** template.

    This record producer is used to store additional information from a shopper specific to a purchase.

    **Note:** For information on how to create a record producer, see [Create a catalog item using a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-item-cat-builder.md).

5.  Navigate to **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

    \[Omitted image "sh-addl-questions-record.png"\] Alt text: ShoppingHub Configuration page showing the Content details tab and Record producer field.

6.  In the **Name** field, enter a name for the configuration.

7.  In the **Configuration type** field, select **Additional Information**.

8.  In the **Content details** tab, complete one or more of the following fields.

    -   In the **Supplier product** field, search for and add a supplier product for which you want to display additional information at checkout.
    -   In the **Product model** field, search for and add a product model for which you want to display additional information at checkout.
    -   In the **Product category** field, search for and add a product category for which you want to display additional information at checkout.
    -   In the **Supplier\(s\)** field, search for and add one or more suppliers to limit the product model or product category question set to supplier products from those suppliers. This field is optional and is read-only when the configuration contains a supplier product.
9.  In the **Record producer** field, search for and select the record producer you created.

    You must first create this record producer using the **ShoppingHub: Additional information on supplier products or product models or product categories** template.

10. Select **Submit**.

    The questions added in the record producer for a specific product, product model, or product category appear during checkout in Shopping Hub.


**Parent Topic:**[Complete your checkout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/complete-your-checkout.md)

