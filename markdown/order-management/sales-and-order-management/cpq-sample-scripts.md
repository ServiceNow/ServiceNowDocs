---
title: Sample scripts
description: View a selection of commonly requested sample scripts.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Sample scripts

View a selection of commonly requested sample scripts.

This article shows some commonly requested sample scripts. If you would like to see more examples, please send a message to [documentation@logik.io](mailto:documentation@logik.io) with your suggestions.

Sample number field determination:

```
var count64 = 0;
var count32 = 0;
var perCoreProcessing = 40; //assuming 8 processors with 5 TFlops compute
var cpu64Processing = 64*perCoreProcessing;
var cpu32Processing = 32*perCoreProcessing;
var cpu16Processing = 16*perCoreProcessing;
var remainingCompute = cfg.estPeakOps;
if(cfg.allowCPU64 == true) { //64 core allowed so divide by that
	count64 = remainingCompute/cpu64Processing;
	remainingCompute = remainingCompute%cpu64Processing;
}
if(cfg.allowCPU32 == true) {
	count32 = remainingCompute/cpu32Processing;
	remainingCompute = remainingCompute%cpu32Processing;
}
return count32;
```

Sample text field determination:

```
var retStr = "";
retStr = retStr + "64 vCPUs: " + Math.round(cfg.cpu64Count);
retStr = retStr + "\\n32 vCPUs: " + Math.round(cfg.cpu32Count);
retStr = retStr + "\\n16 vCPUs: " + Math.round(cfg.cpu16Count);
retStr = retStr + "\\n8 vCPUs: " + Math.round(cfg.cpu8Count);
retStr = retStr + "\\n1 vCPUs: " + Math.round(cfg.cpu1Count);
return retStr;
```

Sample product rule script:

```
//Base Product
var baseProductP2ID = "BP_ID";
var inputs = {"g2BaseProduct": cfg.g2BaseProduct};
var resultSet = lookup("SELECT Product2Id, ProductName FROM Dummytable WHERE ProductCode = :g2BaseProduct", inputs);
for (var row of resultSet) {
	ProductList.id = row.get("Product2Id");
	ProductList.quantity = cfg.orderQty;
	ProductList.bomType = "SALES";
	ProductList.uom = "EA";
	ProductList.level = 1;
	ProductList.notes = row.get("ProductName");
	ProductList.parentProduct = "01t5f000000uJgoAAE"; //parent product identifier. In this case top product being configured from SFDC
	baseProductP2ID = row.get("Product2Id");
	ProductList.uniqueIdentifier = baseProductP2ID; //Parent
	...SF ProductID; not req'd if this has no other children
	ProductList.next();
	break;
}
```

Sample product rule script with `for` loop:

```
//var timesReplicate = cfg.numberOfComputeClusters; //this doesn't work yet.. If it does, we will replicate that many times easier
var timesReplicate = [1,1,1,1,1,1,1,1,1,1]; //dummy 10 times loop based on 10x boolean true, Double loop for 100
for (var parentStep of timesReplicate) {
	for (var step of timesReplicate) {
		if(cfg.cpu16Count > 0) {
			ProductList.id = "01t5f000000v50CAAQ";
			ProductList.quantity=Math.round(cfg.cpu16Count);
			ProductList.notes="Provisioning " + Math.round(cfg.cpu16Count) + " number of 16 core vCPUs";
			if(cfg.sendDirectlyToProvisioning == true) {
				ProductList.bomType = "Manufacturing";
				ProductList.level = 2;
			} else {
				ProductList.bomType = "SALES";
			}
			ProductList.next();
		}
		if(cfg.cpu8Count > 0) {
			ProductList.id = "01t5f000000v50DAAQ";
			ProductList.quantity=Math.round(cfg.cpu8Count);
			ProductList.notes="Provisioning " + Math.round(cfg.cpu8Count) + " number of 8 core vCPUs";
			if(cfg.sendDirectlyToProvisioning == true) {
				ProductList.bomType = "Manufacturing";
				ProductList.level = 2;
			} else {
				ProductList.bomType = "SALES";
			}
			ProductList.next();
		}
		if(cfg.cpu32Count > 0) {
			ProductList.id = "01t5f000000v50BAAQ";
			ProductList.quantity=Math.round(cfg.cpu32Count);
			ProductList.notes="Provisioning " + Math.round(cfg.cpu32Count) + " number of 32 core vCPUs";
			if(cfg.sendDirectlyToProvisioning == true) {
				ProductList.bomType = "Manufacturing";
				ProductList.level = 2;
			} else {
				ProductList.bomType = "SALES";
			}
			ProductList.next();
		}
		if(cfg.cpu64Count > 0) {
			ProductList.id = "01t5f000000v50JAAQ";
			ProductList.quantity=Math.round(cfg.cpu64Count);
			ProductList.notes="Provisioning " + Math.round(cfg.cpu64Count) + " number of 64 core vCPUs";
			if(cfg.sendDirectlyToProvisioning == true) {
				ProductList.bomType = "Manufacturing";
				ProductList.level = 2;
			} else {
				ProductList.bomType = "SALES";
			}
			ProductList.next();
		}
		if(cfg.cpu1Count > 0) {
			ProductList.id = "01t5f000000v50SAAQ";
			ProductList.quantity=Math.round(cfg.cpu1Count);
			ProductList.notes="Provisioning " + Math.round(cfg.cpu1Count) + " number of 1 core vCPUs";
			if(cfg.sendDirectlyToProvisioning == true) {
				ProductList.bomType = "Manufacturing";
				ProductList.level = 2;
			} else {
				ProductList.bomType = "SALES";
			}
			ProductList.next();
		}
	}
}
console.log("Added line items 100 times");
return ProductList;
```

Sample array and map functions:

```
var productidArr = ["test123", "chtest123"];
var inputs = {"productids": productidArr};
var resultSet = lookup("SELECT uniqueidentifier, bomtype FROM bominformation WHERE productid IN (:productids)", inputs);

var prodTypeMap = new Map();
for (var row of resultSet) {
	prodTypeMap.set(row.get("uniqueidentifier"), row.get("bomtype"));
}
var itemTypeManuf = productidArr.every((value) => {return prodTypeMap.get(value) != "Manufacturing";});
if (isGood == false) {
	return "Sales type item found";
}
var summary = "";
productidArr.forEach((item, index) => {summary += index + " " + item + ". ";});
return summary;
```

How to pull multi-select picklist values from SFDC to twinned multi-select picklist field in CPQ in the On Configure/Reconfigure enrichment:

```
let x = (cfgRequest.yourTwinnedLogikField.value).split(";");
cfgRequest.yourTwinnedLogikField.set("value", x);
return cfgRequest;
```

How to concatenate field values into a string:

```
stringVar = "";
stringVar = stringVar.concat(cfg.varible1, cfg.variable2, cfg.variable3);
return stringVar;// returns selected values of "variable1variable2variable3"
```

How to imitate a CONTAINS function:

```
var yourVariable = "Field Value"; // Replace with your actual Field value
if (yourVariable.includes("CU")) {
	// Code you wish to execute when Field Value contains "CU"
} else if (yourVariable.includes("AL")) {
	// Code you wish to execute when Field Value contains "AL"
} else {
	// Code you wish to execute when Field Value doesn't contain "CU" or "AL"
};
```

**Related topics**  


[CPQ scripting language reference](cpq-logik-io-scripting-language-reference.md)

