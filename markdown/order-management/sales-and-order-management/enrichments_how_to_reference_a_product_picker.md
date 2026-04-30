---
title: Referencing a product picker
description: You can reference a product picker in the On BOM, Pricing, and Validation enrichments by modifying your enrichment script.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Setting up enrichments and rules scripting, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Referencing a product picker

You can reference a product picker in the On BOM, Pricing, and Validation enrichments by modifying your enrichment script.

Product pickers are available for reference in On BOM, Pricing, and Validation Enrichments.

When referencing a product picker in any of these scenarios, use the `pkr.<Product Picker varname>` notation in your enrichment script. As an example, the following snippet iterates over the options in `somePicker` and creates a map where each record's option value and quantity are stored.

```
var quantityMap = new Map();
pkr.somePicker.data.forEach((row) => {
	quantityMap.set(row.value, row.quantity);
	}
);
```

If you intend to use the Pricing enrichment to dynamically set prices for the product picker options, be sure to enable this feature on the product picker. To do this, in the product picker administration page, click the cog to open the Product Picker Settings dialog. Then, turn on **Enable for Pricing Enrichment**.

![Product Picker Settings](../images/cpq-product-picker-enable-for-pricing-enrichment.png)

In the related blueprint's Picklist Extension Pricing enrichment, your script will work as follows:

```
pleRequest.forEach((option) => {
	if (quantityMap.has(option.optionValue)) {
		option.productId = option.optionValue;
		option.price = blah; // complete this to suit your use case
	}
});
```

