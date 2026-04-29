---
title: Configure the products card variables
description: Configure the variables in the product card.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure variables, Setup, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure the products card variables

Configure the variables in the product card.

## Before you begin

Role required: sn\_telecom\_c360.admin

## Procedure

1.  Navigate to **All** &gt; **Telecom Customer 360** &gt; **Guided Setup** and select **Get Started**.

2.  Select **360 Cards** &gt; **Products**.

3.  Modify the following variables.

    |Variable|Description|
    |--------|-----------|
    |Product data table|The table to retrieve product list items from. Must be the sold product table \(`sn_install_base_sold_product`\) or a child table extending from this table. Custom tables that extend from the sold product table are also supported.|
    |Product data table query|Query condition that filters the product table to the current context record. By default, products that have a parent sold product are excluded.|
    |Primary filter|The field from the product data table used as the primary filter at the top of the card. The default filter is product location.|
    |Heading field|The field to display as the heading of each product list item. The default is set to the sold product name.|
    |Subheading field|The field to display as the subheading of each product list item. The default is set to the product specification category.|
    |Product search field|The search criteria to be used to filter the list of sold products displayed.|
    |Avatar field|The field to use for the product avatar image.By default, the product model category image is displayed. If no value is specified, a default image is displayed.|


**Parent Topic:**[Configure the Telecommunications Customer 360 variables](../concept/c360-configure-variables.md)

**Related topics**  


[Products card](../concept/c360-products-card.md)

