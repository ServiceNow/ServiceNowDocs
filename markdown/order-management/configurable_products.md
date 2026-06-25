---
title: Setting up configurable products
description: A configurable product links a blueprint to the configuration experience for the product. You can set up configurable products in headless environments using CSV uploads or in Salesforce-integrated environments through product associations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configurable\_products.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Setting up configurable products

A configurable product links a blueprint to the configuration experience for the product. You can set up configurable products in headless environments using CSV uploads or in Salesforce-integrated environments through product associations.

Configurable products serve as the bridge between CPQ blueprints and the configuration experiences that end users interact with. The setup process varies depending on your environment type.

## Headless environment setup

In headless environments, configurable products link blueprints to configurations that launch when end users select products. You set up configurable products by uploading a CSV file with product information through the Products tab in the Utilities section of the CPQ navigation pane. When you set the "configurable" field to TRUE in the CSV file, the configurable product is automatically created in the CPQ environment.

## Salesforce integrated environment setup

In Salesforce-integrated environments, configurable products link CPQ blueprints to Salesforce Product2 records. In the context of Salesforce CPQ, a configurable product serves as the entry point to a CPQ configuration experience. After you define the configurable product, end users see the appropriate CPQ configuration experience when they select the Product2 record from the Product Selection step in Salesforce CPQ.

The setup process depends on when your CPQ Salesforce Managed Package was installed:

-   June 2022 or later: Associate Product2 records with blueprints through the SFDC Products tab and the Associate Blueprint function.
-   Before June 2022: Enable external configuration on the Salesforce Configurable Products tab and add blueprints through the View Setup link.

Multiple Salesforce Product2 records can be linked to one blueprint, but a configurable product cannot be associated with more than one blueprint.

**Related topics**  


[Set up a configurable product in a headless environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-set-up-a-configurable-product-in-a-headless-environment.md)

[Set up a configurable product in a Salesforce-integrated environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-set-up-a-configurable-product-in-a-salesforce-integrated-environment.md)

[Set up blueprints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/blueprints_101.md)

