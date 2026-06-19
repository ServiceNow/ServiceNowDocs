---
title: Set up a configurable product in a headless environment
description: Configure a product links a blueprint to the configuration experience in a headless environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/cpq-set-up-a-configurable-product-in-a-headless-environment.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [configurable product, headless environment, blueprint, CPQ]
breadcrumb: [Setting up configurable products, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up a configurable product in a headless environment

Configure a product links a blueprint to the configuration experience in a headless environment.

## Before you begin

Role required: admin

## About this task

In headless use cases, the configurable product links the blueprint that you created in CPQ to the configuration that launches for end users when they select the product.

## Procedure

1.  Navigate to the Products tab in the Utilities section of the CPQ navigation pane.

    \[Omitted image "cpq-products-tab.png"\] Alt text: Products tab in the Utilities section of the navigation pane

2.  Select the tab for the product that you want to configure.

3.  Upload a CSV file with the required headers and product information.

    The CSV file must include the following headers with appropriate information for your product:

    \[Omitted image "cpq-configurable-product-csv.png"\] Alt text: CSV file headers for configurable products

    If **configurable** is set to **TRUE**, the configurable product is automatically created in the CPQ environment.


