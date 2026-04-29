---
title: Use case: Embed CPQ UI in a Salesforce VisualForce page
description: Learn how to embed the CPQ user interface in a Salesforce VisualForce page.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use cases, Using CPQ, Configure, price, quote apps, Use, Sales and Order Management]
---

# Use case: Embed CPQ UI in a Salesforce VisualForce page

Learn how to embed the CPQ user interface in a Salesforce VisualForce page.

This article outlines how to display the CPQ user interface on a Salesforce VisualForce page, such as Salesforce B2B Commerce.

## Prerequisite

This example requires the easyXDM library to be loaded into Salesforce \[SFDC\]. Navigation: SFDC → Setup → Static Resources → New. Upload the [https://drive.google.com/file/d/1T0TqffMjlZcEjFke\_\_Re23NdZ\_1gWkaJ/view](https://drive.google.com/file/d/1T0TqffMjlZcEjFke__Re23NdZ_1gWkaJ/view) file. For the purposes of thisexample, set the resource name to ‘XDMFile1ʼ.

You must also set up your runtime client in the Logik Admin to have the origins for both your Salesforce domain as well as your envrionment's custom CPQ URL

## Configuration initialization data format

To initialize the configuration, basic field data needs to be passed to the page. Here are the parameters that can be passed, represented in pretty JSON format:

```
{
	"runtimeToken": "...",
	"quote": {
		"SBQQ__PricebookId__c": "...",
		"LGK__QueriedEditAccess__c": "Active",
		"LGK__FlightPath__c": "None"
	},
	"product": {
		"configuredProductId": "...",
		"configurationAttributes": {
			"LGK__Logik_Id__c": null
		},
		"optionConfigurations": {
			"Dynamic": []
		}
	},
	"layoutVarName": "someLayoutVarName"
}
```

Replace the ellipses in the above JSON with the appropriate values from your CPQ environment, pricebook, and productID.

**Note:** The script is case-sensitive. Make sure that the capitalization exactly matches the script. For example, if your script contains `"LGK__Logik_Id__c": Null` \(with a capital N\) instead of `"LGK__Logik_Id__c": null`, it could result in a `403 Forbidden—you don't have permission to access this resource` error.

## Display the default layout

Sometimes, you may want to display a specific default layout that is not ordered first in the list of Blueprint layouts. To designate a specific starting layout with the CPQ configuration page loads, pass "layoutVarName":"&lt;variable name of the layout to show by default&gt;" in the topmost level of the JSON above.

## The host VisualForce page

The following sample VisualForce code is a proxy for the host page in which you intend to embed the Logik UI. Key components:

-   The page imports the easyXDM Javascript library, which facilitates communication with the Logik UI.
-   easyXDM parses the JSON input, transposes it, and passes the data to the Logik page as a remote procedure call.

Sample VisualForce page:

```
<apex:page>
	<head>
		<apex:includeScript value=”{!$Resource.XDMFile1}”/>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<meta name="theme-color" content="#000000" />
		<meta
			name="description"
			content="Logik Configuration Wrapper"
		/>
		<title>Logik Wrapper</title>
		<style>
			iframe {
				width:100%;
				height:92vh;
			}
		</style>
		<script type="text/javascript" src="{!$Resource.XDMFile1}" crossorigin="anonymous">
		</script>
		<!-- easyXDM and Lightning for VF for passing config data to/from Salesforce CPQ -->
		<script type="text/javascript">
			var rpc = new easyXDM.Rpc({
				remote: "<BASE_LOGIK_URL>/ui/configure",
				container: "root"
			}, {
			// method defined in Logik
			remote: {
				postMessage: {}
			},

			local: {
				postMessage: function (message) {
					console.log("External Config JSON Received from iframe");
					configObj = JSON.parse(message);
					console.log(configObj);
		
					}
				}
		});

		var cfgData = {"runtimeToken":"<PLACEHOLDER>","quote":{"SBQQ__PricebookId__c":"
<PLACEHOLDER>","LGK__QueriedEditAccess__c":"<PLACEHOLDER>","LGK__FlightPath__c":"
<PLACEHOLDER>"},
"product":{"configuredProductId":"<PLACEHOLDER>","configurationAttributes":
{"LGK__LOGIK_Id__c":""},
"optionConfigurations":{"Dynamic":[]}},"layoutVarName":"<PLACEHOLDER>"};

			console.log(JSON.stringify(cfgData));
			rpc.postMessage(JSON.stringify(cfgData));
		</script>
	</head>
	<body>
		<div id="root"></div>
	</body>
</apex:page>
```

Replace the highlighted &lt;BASE\_LOGIK\_URL&gt; placeholder in the above VisualForce with the base URL of your CPQ environment.

**Note:** If you named the easyXDM library something other than XDMFile1, update the two occurrences of XDMFile1 above with the name you used for the easyXDM static resource.

Depending on what you want to do, you must also associate an action for the "Quote" button. Insert the action after the console.log\(configObj\) line.

Examples:

`//window.close();` // if you want to close the whole browser page

`//window.location = 'whereeveryouwanttoredirectto';` // if you want to redirect to another page

## The EasyXDM library

To learn more about the easyXDM library used in this topic, see [easy XDM.net](https://easyxdm.net/wp/).

**Parent Topic:**[Use cases](use-cases.md)

