---
title: Set up a configurable product in a Salesforce-integrated environment
description: Configure a Salesforce product to use external configuration with ServiceNow blueprints when using current Salesforce Managed Package installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/cpq-set-up-a-configurable-product-in-a-salesforce-integrated-environment.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up configurable products, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up a configurable product in a Salesforce-integrated environment

Configure a Salesforce product to use external configuration with ServiceNow blueprints when using current Salesforce Managed Package installations.

## Before you begin

Role required: admin

## About this task

If your CPQ SF Managed Package was installed in June 2022 or later, follow these steps to associate a configurable product with a blueprint.

**Note:** If your CPQ SF Managed Package was installed before June 2022, see [Set up a configurable product in legacy Salesforce environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-set-up-a-configurable-product-in-a-salesforce-integrated-environment-older-managed-package.md).

## Procedure

1.  On the Salesforce Products tab, locate the Product2 record to connect to a CPQ configuration experience \(blueprint\).

2.  Associate the Product with a Price Book entry.

    The amount can be $0.00, but a value must be entered.

3.  Set the product to **Active** and **Enabled**, then select **Save**.

4.  On the SFDC Products tab, select the list view to Logik View.

5.  Locate the Product Name of the Product2 record created in step 3, then select the **Click Here** link under View Logik Setup column.

6.  Select **Associate Blueprint**.

7.  Select the desired blueprint, then select **Save**.


**Related topics**  


[Set up a configurable product in a headless environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/cpq-set-up-a-configurable-product-in-a-headless-environment.md)

[Set up blueprints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/blueprints_101.md)

