---
title: Using the DerivedProductPriceExtensionPoint for derived pricing
description: The sn\_csm\_pricing.DerivedProductPriceExtensionPoint provides an interface with specific methods that call certain business logic for using valid source products in source and target product pairs in derived pricing.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Derived product pricing, Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Using the DerivedProductPriceExtensionPoint for derived pricing

The **sn\_csm\_pricing.DerivedProductPriceExtensionPoint**provides an interface with specific methods that call certain business logic for using valid source products in source and target product pairs in derived pricing.

The extension point has three methods:

-   `canHandleRequest(pricingEngineContext)`: Determines whether the pricing engine can handle this extension point request.
-   `getAccountLevelDerivedPricedProductsEncodedQuery(pricingEngineContext)`: Custom query for account-level sold product lookup.
-   `getQualifiedSourceTargetPairs(pricingEngineContext, sourceTargetPairs)`: Filter source-target pairs in derived pricing. This method receives an array of pair objects after rule matrix evaluation. Each pair contains:

    -   `sourceLineDetail` - The PricingEngineContextLineDetail of the source line
    -   `targetLineDetail` - The PricingEngineContextLineDetail of the target \(derived\) line
    -   `isPair` - Boolean, true by default
    To exclude a pair from calculation of the derived \(target\) product, set `pair.isPair = false` and return the modified array. If `isPair = true`, the source line price is included in the price calculation of the derived \(target\) product.


To access the extension point, navigate to **All** &gt; **Pricing** &gt; **Administration** &gt; **Pricing Extension Points** and select the `sn_csm_pricing.DerivedProductPriceExtensionPoint`.

