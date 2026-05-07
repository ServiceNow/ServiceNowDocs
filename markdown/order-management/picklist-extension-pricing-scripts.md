---
title: The Picklist Extension Pricing enrichment
description: Use the Picklist Extension Pricing enrichment to adjust pricing according to location or other factors.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# The Picklist Extension Pricing enrichment

Use the Picklist Extension Pricing enrichment to adjust pricing according to location or other factors.

The Picklist Extension Pricing enrichment can be used to dynamically change the pricing of Field Options in designated picklist extension fields.

## Prerequisites

Submit a support case through the CPQ Support site or by emailing [support@logik.io](mailto:support@logik.io) requesting the enrichment be enabled for your environment. Please provide a use case for using the enrichment.

Picklist extension fields need to have the "Enable for enrichment" toggle turned on to be affected by the enrichment.

![Picklist extension fields](../images/cpq-enrichments-enable-for-enrichment.png)

The enrichments tab will be shown when navigating to a blueprint in the CPQ Admin.

![Picklist extension fields](../images/cpq-enrichments-in-blueprint.png)

Watch this demonstration of the Picklist Extension Pricing enrichment in action.

[PLE enrichment Script Demo](https://www.youtube.com/watch?v=deoQkQaPnX8)

## Demonstration script

The following script was used in the demonstration video.

```
let sourcesArr = [];
let componentArr = [];
let accessoryArr = [];

pleRequest.forEach(o => {
    if(o.fieldVariableName == "alternateEnergySources") {
        sourcesArr.push(o.optionValue);
        //o.price = "1000";
    }
    if(o.fieldVariableName == "alternateEnergyComponents") {
        componentArr.push(o.optionValue);
        //o.price = "900";
    }
    if(o.fieldVariableName == "alternateEnergyAccessory") {
        accessoryArr.push(o.optionValue);
        //o.price = "800";
    }
});

var sourceMap = new Map();
if(sourcesArr != null && sourcesArr.length != 0) {
    var sourceRows = lookup("Select Energy, BasePrice from AlternateEnergyPricing where Zip = :zip and Energy IN (:value)", { "zip": cfg.zipCode, "value": sourcesArr });
    for (var row of sourceRows) {
        sourceMap.set(row.get("Energy"), row.get("BasePrice"));
    }
} else {    //source PLE not part of request. So populate this map for other PLEs 
    console.log("Entered non PLE in request case");
    sourcesArr = ["Solar", "Wind", "Nuclear"];
    var sourceRows = lookup("Select Energy, BasePrice from AlternateEnergyPricing where Zip = :zip and Energy IN (:value)", { "zip": cfg.zipCode, "value": sourcesArr });
    for (var row of sourceRows) {
        sourceMap.set(row.get("Energy"), row.get("BasePrice")); 
    }
    console.log(sourcesArr);
    console.log(sourceMap);
}

var multiplierMap = new Map();
if(cfg.alternateEnergySources != "") {
    var multiplierRows = lookup("Select Group, Factor from AlternateEnergyMultiplier where Zip = :zip and Energy = :energyVal", { "zip": cfg.zipCode, "energyVal": cfg.alternateEnergySources });
    for (var row of multiplierRows) {
        multiplierMap.set(row.get("Group"), row.get("Factor"));
    }
}
let sourcePrice = sourceMap.get(cfg.alternateEnergySources);
if(sourcePrice != null) {
        pleRequest.forEach(o => {
        if(o.fieldVariableName == "alternateEnergySources") {
            o.price = sourceMap.get(o.optionValue);
        }
        if(o.fieldVariableName == "alternateEnergyComponents") {
            let compPrice = multiplierMap.get("Component");
            if(compPrice != null) {
                o.price = sourcePrice*compPrice;
            }
        }
        if(o.fieldVariableName == "alternateEnergyAccessory") {
            let multA = multiplierMap.get("Accessory");
            if(multA != null) {
                o.price = sourcePrice*multA;
            }
        }
    });
}

console.log(sourcesArr);
console.log(componentArr);
console.log(accessoryArr);
console.log(sourceMap);
console.log(multiplierMap);

return pleRequest;
```

## Sample design, use cases, and pleRequest elements

Sample enrichment script design:

1.  Loop through picklist options and store them for reference later \(pleRequest.forEach\(\)\)
2.  Get prices for options and store them \(either via table lookup or in the function itself\)
3.  Set the price for the right option \(pleRequest.forEach\(\)\)

Use cases:

-   ZIP code dependent pricing
-   Price multipliers and discounts
-   Delta pricing
-   Independent component pricing subtraction

pleRequest elements:

-   pleRequest.fieldVariableName: variable name of the picklist field
-   pleRequest.optionValue: picklist options defined in the field
-   pleRequest.productId: ID of the product in the PLE mapping
-   pleRequest.price: price to be set in the extension

Referencing elements in the `pleRequest` object is similar to referencing objects such as `ProductList`, `cfg`, and `cfgRequest`. If a variable is substituted into `pleRequest` \(either in a `for` loop or using the `forEach` function\), the element is still referenced after the variable, followed by a period.

**Related topics**  


[CPQ scripting language reference](cpq-logik-io-scripting-language-reference.md)

