---
title: Enable pricing in the ServiceNow Quote Experience
description: Enable pricing in ServiceNow Quote Experience to integrate natively with Sales CRM Pricing Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-pricing-quote-experience.html
release: brazil
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 2
breadcrumb: [Pricing in the ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Enable pricing in the ServiceNow Quote Experience

Enable pricing in ServiceNow Quote Experience to integrate natively with Sales CRM Pricing Management.

## Before you begin

Role required: admin

Before you enable pricing, confirm that:

-   You have access to CPQ Administration to import and export the quote blueprint.
-   Complete the CPQ setup. For more information, see [Setting up CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/setup-cpq-integrator.md)

## About this task

Pricing Management is a ServiceNow® capability that Quote Experience can integrate with. When pricing is enabled, quote and line pricing fields are populated by the Pricing Management service. For more information, see [Pricing in the ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-in-quote-experience.md).

## Procedure

1.  Install the [Price Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-management.md) plugins.

    For more information, see [Install Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/install-price-management.md).

2.  Submit a support ticket requesting the required tenant setting configurations for your instance.

    1.  transaction.oneQuoting.pricing.enabled to 'TRUE'
    2.  transaction.oneQuoting.pricing.integration.type to 'productized'
3.  In CPQ Administration, export and import the quote blueprint.

    The blueprint deployment creates and stores the pricing field mappings, which are read at run time.


## Result

Pricing is enabled for the blueprint. Quote and line pricing fields are populated by the Pricing Management service, and users can reprice quotes manually or automatically.

## What to do next

To configure how and when quotes are repriced:

-   To configure the Reprice event action, see [Transaction events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-events.md).
-   To configure automatic repricing per stage, see [Quote transaction stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-stages.md).
-   To surface the **Reprice** action and the pricing-state column on the quote layout, see [Quote transaction layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/quote-tm-layouts.md).

