---
title: Set up a configurable product in a headless environment
description: A configurable product links a blueprint to the configuration experience for the product. Learn how to set up a configurable product in a headless environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/order-management/cpq-set-up-a-configurable-product-in-a-headless-environment.html
release: zurich
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Setting up configurable products, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up a configurable product in a headless environment

A configurable product links a blueprint to the configuration experience for the product. Learn how to set up a configurable product in a headless environment.

## Before you begin

Role required: Admin

## About this task

In headless use cases, the configurable product is the link between the blueprint that you have created in ServiceNow CPQ and the configuration that launches for end users when they select the product. A Products tab appears in the Utilities section of the ServiceNow CPQ navigation pane.

\[Omitted image "cpq-products-tab.png"\] Alt text: menu

## Procedure

1.  Click the tab for the product that you want to configure.

2.  Upload a CSV file with the following headers and the appropriate information for your product.

    \[Omitted image "cpq-configurable-product-csv.png"\] Alt text: CSV file for configurable products

    If "configurable" is set to TRUE, the configurable product is automatically created in the ServiceNow CPQ environment.


