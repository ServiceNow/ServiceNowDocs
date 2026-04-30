---
title: Use case: Embed ServiceNow CPQ UI in an HTML page
description: Learn how to embed the ServiceNow CPQ user interface in an HTML iFrame.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [Use cases, Using ServiceNow CPQ, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Use case: Embed ServiceNow CPQ UI in an HTML page

Learn how to embed the ServiceNow CPQ user interface in an HTML iFrame.

This article provides an outline for how an admin can display the ServiceNow CPQ UI in an iframe in any HTML page. Briefly, the recipe consists of:

-   the data that the host application will pass to the host HTML page, as JSON
-   the host HTML page
-   the Content Security Policy \[CSP\] settings, adjusted on the ServiceNow CPQ server

## Configuration initialization JSON data format

To initialize the configuration, pass basic field data to the page. Here are the parameters that you can pass, represented in pretty JSON format:

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
			"Logik__Id__c": null
		},
		"optionConfigurations": {
			"Dynamic": []
		}
	},
	"layoutVarName": "someLayoutVarName"
}
```

Replace the ellipses in the above JSON with the appropriate values from the ServiceNow CPQ environment, pricebook, and product ID.

Sometimes, you may want to display a default layout that is not ordered first in the list of Blueprint layouts. To designate a starting layout with which the ServiceNow CPQ configuration page loads, pass `"layoutVarName":"<variable name of the layout to show by default>"` in the topmost level of the JSON above.

## The host HTML page

You will need to host the parent application. For security reasons, this application/host HTML page cannot be localhost. The following sample HTML is a proxy for the host page in which you intend to embed the ServiceNow CPQ UI. The page imports the easyXDM JavaScript library, which facilitates communication with the ServiceNow CPQ UI. Then, easyXDM parses the JSON input, transposes it, and passes the data to the ServiceNow CPQ page as a remote procedure call.

To process data passed from the ServiceNow CPQ UI and leverage it on this HTML page, review the values written to the browser console in the blue-colored console.log line of JavaScript below. Advanced admins can leverage this data by adding more JavaScript in this area.

Replace the `<BASE_LOGIK_URL>` placeholder with the base URL of the ServiceNow CPQ environment.

```
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<meta name="theme-color" content="#000000" />
		<meta name="description" content="Logik Configuration Wrapper" />
		<title>Logik Wrapper</title>
		<style>
			iframe {
				width:100%;
				height:92vh;
			}
		</style>
		<script type="text/javascript" src="assets/js/easyXDM/2.5.0/easyXDM.min.js"
		ssorigin="anonymous"></script>
		<!-- easyXDM and Lightning for VF for passing config data to/from Salesforce CPQ -->
		<script type="text/javascript">
		var rpc = new easyXDM.Rpc({
			remote: "<BASE_LOGIK_URL>/ui/configure",
			container: "root"
		}, {
		// method defined in ServiceNow CPQ
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
		var cfgData = {"runtimeToken":"<PLACEHOLDER>","quote":{"SBQQ__PricebookId__c":"<PLACEHOLDER"},"LGK_QueriedEditAccess__c":"<PLACEHOLDER>","LGK__FlightPath__c":"<PLACEHOLDER>"},"product":{"configuredProductId":"<PLACEHOLDER>","configurationAttributes":{"LGK__LOGIK_Id__c":""},"optionConfigurations":{"Dynamic":[]}},"layoutVarName":"<PLACEHOLDER>"};
		console.log(JSON.stringify(cfgData));
		rpc.postMessage(JSON.stringify(cfgData));
		</script>
	</head>
	<body>
		<div id="root"></div>
	</body>
</html>
```

## Content security policy settings

To embed the ServiceNow CPQ application in an iframe, you must configure it to allow the host application’s domain. Log a case with ServiceNow CPQ support, describe your intent to embed ServiceNow CPQ UI in an HTML page, and request that your ServiceNow CPQ server CSP settings be configured to accommodate the parent application’s domain URL.

## The EasyXDM library

To learn more about the easyXDM library, see [easy XDM.net](https://easyxdm.net/wp/).

**Parent Topic:**[Use cases](use-cases.md)

