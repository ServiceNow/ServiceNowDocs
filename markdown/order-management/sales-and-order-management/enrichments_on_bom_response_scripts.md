---
title: The On BOM Response enrichment
description: You can use this enrichment to work with ProductList items whenever there is an update to the bill of materials.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The On BOM Response enrichment

You can use this enrichment to work with ProductList items whenever there is an update to the bill of materials.

The On BOM Response enrichment is enabled by default in environments and can be used to manipulate items in the ProductList whenever there is an update to the bill of materials \(BOM\).

**Note:** The ServiceNow CPQ environment must include rules with product actions, or there will be nothing for the enrichment to loop through.

![BOM response](../images/cpq-enrichments-on-bom-response.png)

In the following sample, the On BOM Response enrichment loops through products and changes the price of a product.

```
//Loop over products and change price of a product
let dealProduct = cfg.blueMoonSelected;
if (dealProduct == true) {
        for(var prod of ProductList) {
                let price = prod.price * .8;
                prod.price = price;
        }
}
```

On BOM Response enrichments may request external REST services via GET or POST.

In the following sample script, the On BOM Response enrichment uses an external connection to query a powerPricing API with customer data. With the customer-specific rate data retrieved from the service, the enrichment adjusts the pricing of existing ProductList records.

```
var powerInputs = {"membershipCode":cfg.eCMembershipCode, "icp":cfg.eCICPNumber};
let powerResponse = External.powerPricing(powerInputs);
let dailyCharge = 0; let ratesArr = [];

if(powerResponse.status == 200) {
	for(var record of powerResponse.body) {
		if(record.chargeType == cfg.expectedUsage) {
			dailyCharge = record.dailyCharges;
			ratesArr = record.rates;
		}
	}
	for(var prod of ProductList) {
		if(prod.id=="electricBillEstimator") {
			let addedPrice = dailyCharge * cfg.serviceDurationInDays;
			prod.price = addedPrice;
		}
			if(prod.id=="Standard Rate" || prod.id=="Low Rate") {
			prod.price = dailyCharge;
		}
	}
	for(var rateVal of ratesArr) {
		ProductList.id = "Additional Charge Per KWH: " + rateVal.name;
		ProductList.quantity = 1;
		ProductList.bomType = "Manufacturing";
		ProductList.orderNumber = 2;
		ProductList.price = rateVal.rate;
		ProductList.notes = rateVal.measure;
		ProductList.parentProduct = "electricBillEstimator";
		ProductList.next();
	}
}

return ProductList;
```

## The difference between the rules engine BOM and the enriched BOM

There are two versions of the BOM during runtime: the rules engine BOM, which is based on the results of product rules during runtime, and the enriched BOM, which is the result of the BOM enrichment.

The BOM enrichment's ProductList object \(referenced in the script\) is the result of the rules engine BOM, not the enriched BOM. This is to make sure there are no infinite loops. Suppose that the script were to reference its own ProductList that it returns, and the script were set up to increase the price of certain objects by a percentage on BOM update. In this case, the next time the contents of the BOM were updated, the price increase would happen again and again.

To prevent this situation, the enriched BOM is not referenced by any rule or enrichment other than the validation enrichment's ProductList. While this makes sure that the BOM enrichment can function outside the rules engine, it also means that if a condition is met in the BOM enrichment, those conditions can be met again the next time the BOM is updated, because any change to the BOM in the BOM enrichment script that stops that condition will not be referenced.

With external connections, this is not a problem as long as the response is consistent. However, if the response changes when fired multiple times, such as when generating a string or saving a certain time, it will update each time the BOM is updated.

The BOM Response enrichment might be used to:

-   dynamically change the price of products in the BOM. This can be either a static or dynamic change rate, such as a shipping fee being static and taxes being dynamic.
-   change attributes of products in the BOM that are reliant on some condition in the BOM, such as the quantity of free stickers given out once $100+ of tax has been quoted.
-   remove a line item from the BOM.

