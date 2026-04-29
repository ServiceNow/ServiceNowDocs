---
title: Nested bundling in Salesforce CPQ
description: Enable nested bundling in Salesforce CPQ to support complex product hierarchies and configurations.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Nested bundling in Salesforce CPQ

Enable nested bundling in Salesforce CPQ to support complex product hierarchies and configurations.

With some additional configuration, CPQ now supports sending back a nested bundle structure from CPQ to Salesforce CPQ. This allows you to take advantage of the BOM hierarchy built in CPQ and have it reflected in the Salesforce CPQ Quote Line Editor \(QLE\).

## Setup in Salesforce

To enable support for nested bundles, additional setup steps must be completed in the Salesforce CPQ Package settings. These steps require Salesforce CPQ package version 242 \(Spring 2023\) or later.

1.  Navigate to Setup &gt; Installed Packages &gt; Salesforce CPQ, and then click **Configure**.

    ![Setup in Salesforce](../images/cpq-layout-number-field-props-sf-settings.png)

2.  On the Additional Settings tab, check the box to enable **Nested Bundles for External Configurator**.
3.  Click **Save** to save the changes.

Products that may have other products below them in the BOM hierarchy should be marked as Logik Enabled in the Product2 record in Salesforce. This is the same as setting up configurable products to work with CPQ. The products also need to have a pricebook entry in the pricebook used for the quote if they are going to be created as quote lines.

The following video explains setting up nested bundle structures in CPQ and Salesforce CPQ:

[Nested Bundles Demo](https://www.youtube.com/watch?v=3EBOPNW_Gds)

## Setup in CPQ

After completing the Salesforce CPQ package setting steps, reach out to CPQ support and log a case to have nested bundling enabled in your CPQ instance. As with any larger change, the recommendation would be to start in a dev or test environment and validate that it is working as expected before enabling it in production.

In CPQ, the BOM hierarchy is defined through the parentProduct and uniqueIdentifier fields on items in the bill of materials. This hierarchy in the product list is reflected in the Salesforce CPQ quote line editor.

## Limitations

Nested bundles from external configurators are limited to four levels, including the topmost parent. This means you can nest products up to three levels deep inside a CPQ configuration.

**Note:** Trying to add the same product to two dynamic nested bundles via an external configurator in Salesforce CPQ results in an "Attempt to de-reference a null object" error.

For example, suppose Product X is nested inside both the Nested Child 1 dynamic feature and the Nested Child 2 dynamic feature, when both are children of the Parent dynamic feature. This configuration results in the error.

