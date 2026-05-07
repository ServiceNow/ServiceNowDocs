---
title: Integrating CPQ
description: Learn how CPQ connects with downstream systems and UI frameworks—visualization engines \(CDS, kBridge, Threekit\), eCommerce storefronts \(Shopify, headless\), and Salesforce \(CPQ, B2B Commerce, Base Package\)—to deliver real-time, guided configuration, pricing, and ordering at scale.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Sales Customer Relationship Management]
---

# Integrating CPQ

Learn how CPQ connects with downstream systems and UI frameworks—visualization engines \(CDS, kBridge, Threekit\), eCommerce storefronts \(Shopify, headless\), and Salesforce \(CPQ, B2B Commerce, Base Package\)—to deliver real-time, guided configuration, pricing, and ordering at scale.

With integrations, you can:

-   Visualize configurations in real time using 2D/3D viewers \(CDS, kBridge, Threekit\).
-   Transact in your commerce stack via Shopify or headless storefronts with draft orders or add-to-cart flows.
-   Sell through Salesforce with CPQ/B2B Commerce, launch the CPQ Configurator from Product2, and persist configuration data to Salesforce objects for quoting and amendments.

## Integration categories at a glance

|Category|Primary purpose|Where it’s configured|Typical data flow|
|--------|---------------|---------------------|-----------------|
|Visualization \(CDS, kBridge, Threekit\)|Show 2D/3D product visuals that react to user selections|Blueprint → Layout \(CSV/Editor\)|CPQ fields/sets → viewer \(1-way\); optional viewer → CPQ \(2-way\)|
|eCommerce \(Shopify, Headless\)|Embed configurator on product/content pages; create carts or draft orders|Shopify app + CPQ runtime client|Storefront → CPQ → cart/draft order|
|Salesforce \(Base, CPQ, B2B Commerce\)|Launch/configure from Product2, write BOM/field data, amendments|Salesforce package + CPQ Settings|Quote/Cart ↔ CPQ runtime; optional persistence to CLI/CFD|

Limits and behaviors \(visualization\):

-   Sets and product pickers: up to 25 indices/options sent to the viewer
-   Active set index: can be published to the viewer when using set repeaters
-   Two-way sync: supported for CDS and kBridge \(fields; sets require a listener field + parsing rule\)
-   Threekit supports one-way from CPQ; pair with set repeater guidance where applicable

**Related topics**  


[Integrating CPQ with visualization tools](logik-io-integration-wtih-visualization-tools.md)

[CPQ integration with Salesforce B2B Commerce](logik_io_integration_with_salesforce_b2b_commerce.md)

[Request provisioning of an SFDC org with a CPQ environment](../task/cpq-request-provisioning-of-an-sfdc-org-with-a-servicenow-cpq-environment.md)

