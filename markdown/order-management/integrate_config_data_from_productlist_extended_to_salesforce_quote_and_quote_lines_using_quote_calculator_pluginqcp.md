---
title: Use case: Using the Salesforce Quote Calculator plugin to integrate data from CPQ to Salesforce quotes and quote lines
description: In the CPQ Extension for Salesforce CPQ package version 1.7 or earlier, use the Salesforce Quote Calculator Plugin to parse extended information from a configuration and map it to custom fields.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Using the Salesforce Quote Calculator plugin to integrate data from CPQ to Salesforce quotes and quote lines

In the CPQ Extension for Salesforce CPQ package version 1.7 or earlier, use the Salesforce Quote Calculator Plugin to parse extended information from a configuration and map it to custom fields.

**Note:** This article applies to the CPQ Extension for Salesforce CPQ package version 1.7 or earlier. If your version is 1.8 or later, see [Use case: Configuration line item to quote line flow](use-case-configuration-line-item-to-quote-line-flow.md).

Using the extended information of the CPQ ProductList object with the Salesforce Quote Calculator plugin \(QCP\), data may be passed from CPQ into Salesforce and used to manipulate both quote and quote line information.

ProductList.extended may only be populated with an advanced product action, as shown here.

![Advance function Code](../images/cpq-productlist-extended-advanced-product-action.png)

The ProductList.extended object takes the form of a JSON object and accepts key:value pairs. In the example above, we pass through a dummy text string, “QCP Test Value”, with the newValue key. ProductList.extended can hold field values, as well as an array of JSON objects.

When this product is added to the bill of materials \(BOM\), we can view its associated info in the custom object “BOM Data”, which is held at the quote line of the configurable product.

![Code](../images/cpq-productlist-extended-bom-data.png)

To leverage this extended information, we will need to use the [Quote Calculator Plugin](https://developer.salesforce.com/docs/atlas.en-us.cpq_dev_plugins.meta/cpq_dev_plugins/cpq_dev_jsqcp_parent.htm). To start, navigate to the Custom Scripts item in Salesforce.

![Performance](../images/cpq-salesforce-custom-scripts.png)

Here, you can write a script to leverage the extended information from CPQ and use it to manipulate fields in SFDC. The following script is the sample script used in this instance.

```
export function onBeforeCalculate(quote, lines) {
	var result;
	var resultValue;
	var product_code = "headlessItem3";
	if (lines != null) {
		lines.forEach(function (line) { //Parsing all quote lines to find BOM Data object
			if(line.record["LGK__BomData__c"] != null){                        
				var configJson = JSON.parse(line.record["LGK__BomData__c"]);
				var itemsJson = configJson["items"]; //Create JSON object containing all items in BOM data
				itemsJson.forEach(function(itemsLine){ //For each item in the BOM Data
					if(itemsLine["productCode"] == product_code){ //Checking for item "headlessItem3"
						result = itemsLine["extended"]; //Parses extended information to find "newValue"
						resultValue = result["newValue"]; //Assigning keyed value of "newValue"
					}
				});
			}
		});
		lines.forEach(function (line) { //For each line in the quote
			if (line.record["SBQQ__ProductCode__c"] == product_code){ //Checking for the line item "headlessItem3"
				line.record["Test_Text__c"] = resultValue; //Setting the quote line field "Test Text" with the value of resultValue
			}
		});
    }
    return Promise.resolve();
}; 
```

Any quote fields or quote line fields referenced by the custom script must be explicitly defined in the appropriate inputs on the custom script record. Our sample script references three quote line fields: LGK\_BomData c, SBQQ\_ProductCode c, and Test\_Text c.

Once your script has been written, define it in the Salesforce CPQ settings. Follow these steps:

1.  In Setup, search for “Installed Packages” using Quick FInd.
2.  Next to “Salesforce CPQ”, click **Configure**.
3.  Select the Pricing and Calculation tab.
4.  If necessary, deselect Use Legacy Calculator.
5.  Select the Plugins tab.
6.  Define your custom script in the Quote Calculator plugin, and then click `Save`.

![Performance graph](../images/cpq-salesforce-quarterly-performance.png)

When you navigate to your quote and trigger any action that performs a calculation in SFDC \(such as clicking “Calculate”\), the Quote Calculator Plugin runs and modifies fields as designated.

**Parent Topic:**[Use cases](use-cases.md)

