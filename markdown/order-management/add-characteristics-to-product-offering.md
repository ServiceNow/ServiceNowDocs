---
title: Add characteristic and characteristic options to a product offering
description: Add characteristic and characteristic options to an existing product offering using the Product Offering Characteristic tab in Sales Customer Relationship Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/add-characteristics-to-product-offering.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Create product characteristics and characteristic options, Defining product characteristics and characteristic options, Create product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Add characteristic and characteristic options to a product offering

Add characteristic and characteristic options to an existing product offering using the **Product Offering Characteristic** tab in Sales Customer Relationship Management.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin

## About this task

There are a number of ways to create characteristic and characteristic options. The following procedure lets you add characteristics to product offerings that already exist but have not been published.

## Procedure

1.  In the CRM Workspace, select the **List** icon \[Omitted image "list-outline-24.svg"\] Alt text:.

2.  Navigate to **Offerings** &gt; **Product Offerings** and select the product offering that you're working with.

3.  In the **Product Offering Characteristics** tab, select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Characteristic|Product offering characteristic. Select an existing characteristic. Select **New** to create a characteristic.|
    |Characteristic option|Characteristic option for the product offering. Select an existing characteristic option or select **New** to create options.|
    |Characteristic type|Option that lets you select a characteristic type.|
    |Value|Default value for the characteristic, applicable only when the characteristic's input type is single-line text, integer, email, address, label, decimal, date, date/time, or duration. This field is available only when the characteristic has one of these input types. For choice, complex, or boolean characteristics, use the characteristic option instead.|
    |Product offering|Name of the product offering.|
    |Order|Numerical order for the options. Options designated with the number 1 appear first in the order.|
    |Mandatory|Option indicating that the characteristic option is required to complete the order.|
    |Default|Option indicating this characteristic option is the default choice.|
    |Customer input required|Option indicating that consumer input is required for the product option.|

5.  Select **Save**.

    The product offering characteristic is added to the product offering. Select the characteristic in the **Product Offering Characteristics** tab to make further changes.


**Related topics**  


[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md)

