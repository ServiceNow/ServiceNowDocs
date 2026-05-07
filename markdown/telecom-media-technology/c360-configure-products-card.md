---
title: Configure the products card variables
description: Configure the variables that control what data the products card displays and how users can search and filter sold products.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure variables, Setup, Configure, Telecommunications Customer 360, Telecommunications, Media, and Technology \(TMT\)]
---

# Configure the products card variables

Configure the variables that control what data the products card displays and how users can search and filter sold products.

## Before you begin

Role required: sn\_telecom\_c360.admin

## Procedure

1.  Navigate to **All** &gt; **Telecom Customer 360** &gt; **Guided Setup** and select **Get Started**.

2.  Select **360 Cards** &gt; **Products**.

3.  Modify the following variables.

    |Variable|Description|
    |--------|-----------|
    |Product data table|Table used to retrieve product list items. Must be the sold product table \(`sn_install_base_sold_product`\) or a child table extending from this table. Custom tables that extend from the sold product table are also supported.|
    |Product data table query|Query condition that filters the product table to the current context record. By default, products that have a parent sold product are excluded.|
    |Primary filter|Field used as the primary filter at the top of the card. Defaults to product location.|
    |Heading field|Field displayed as the heading of each product list item. Defaults to the sold product name.|
    |Subheading field|Field displayed as the subheading of each product list item. Defaults to the product specification category.|
    |Product search field|Search criteria used to filter the list of sold products displayed.|
    |Avatar field|Field used for the product avatar image. Defaults to the product model category image. If no value is specified, a default image appears.|
    |Enable search on product characteristics|Flag that enables search by product characteristics. Select this flag to enable search against product characteristic values in addition to the product search field. Search is performed against characteristic values only.|


**Parent Topic:**[Configure the Telecommunications Customer 360 variables](../concept/c360-configure-variables.md)

**Related topics**  


[Products card](../concept/c360-products-card.md)

