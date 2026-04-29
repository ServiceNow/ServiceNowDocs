---
title: Scripting: How to populate set values
description: View a detailed example of how to use an On Configure/Reconfigure blueprint enrichment script to load field values into a set.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Scripting: How to populate set values

View a detailed example of how to use an On Configure/Reconfigure blueprint enrichment script to load field values into a set.

This article demonstrates how to use an “On Configure/Reconfigure” blueprint enrichment script to load field values into a set.

This example shows making a SOQL call to Salesforce using an external connection to get the last names of all of the account contacts and preloading them into a set for further configuration.

## Prerequisites

To complete this example you need:

-   Enrichments enabled in your CPQ instance
-   External connections enabled in your CPQ instance
-   A set created and associated with the blueprint
-   A text field associated with the set

## External connection: SOQL call

In the CPQ Admin screen, find the external connections under Utilities.

![Admin screen](../images/cpq-admin-external-connections.png)

1.  Set the integration type to Salesforce.
2.  Define the SOQL query to make. In this example, we are retrieving all the contacts that are associated with a particular account and storing the last name.

SOQL query:

```
SELECT LastName FROM Contact WHERE AccountId = '{{accId}}'
```

## On Configure/Reconfigure script

In the blueprint, navigate to the enrichments area, and add the script to the “On Configure/Reconfigure” enrichment.

```
let setData = []; // initialize the set data as an empty array

//if initializing, default in setData
if (cfgRequest.demoset_swc.data == []) {
	const inp = {"accId":"0015f000006lRKcAAM" }; // Hardcoded accountId, could be mapped in from a field
	const response = Salesforce.getSetInit_swc(inp); // SELECT LastName FROM Contact WHERE AccountId = '{{accId}}'
	const contactList = response.body.records;
	if (contactList.length > 0) {
		for (var contact of contactList) {
			let elem = {"textTest_swc":{"value": contact.LastName } }; // set the field value
			setData.push(elem); // add to the setData array
		}
		// after looping through all the contacts/previous set data, add them to the set
		cfgRequest.demoset_swc.set("data",setData);
	}
}

return cfgRequest;
```

## Script walkthrough

![Admin screen](../images/cpq-script-populate-set-values.png)

1.  The setData array is initialized as an empty array \(line 1\).
2.  Check whether the set already has data in it, either from the API payload or from a previous configuration \(line 3\).
3.  Define the inputs for the query to Salesforce \(line 5\). In this example, the account ID is hard coded but could be passed from a field or mapped from a twin field on the quote. Make the SOQL query to Salesforce by using the external connection that was defined, then save the response \(line 6\) and get the records array \(line 7\).
4.  If the call returned records \(line 8\), loop over the records \(line 9\) and set the field value of “textTest\_swc” to the contact LastName \(line 10\). Finally, add the new set element to the setData array \(line 11\).
5.  After looping through the contacts, add all of the setData to the set, “demoSet\_swc”, in the configuration request \(line 14\).
6.  Finally, return the updated configuration request \(line 18\).

To reuse this script, make changes to the following lines:

1.  Line 5: Update the account ID \(0015f000006lRKcAAM\) to a new value, or twin a field from the quote.
2.  Line 6: Update the name of the Salesforce connection.
3.  Line 10: Update the field name \(textTest\_swc\) to a field in the set that you are using.
4.  Line 16: Update the set name \(demoset\_swc\) to the name of the set that you are using.

## Setting data from an external connection each configuration

If instead you want defaulted data to overwrite whatever the user had entered in the previous configuration, delete the `if` clause in line 4.

If you want only certain fields in the set to overwrite user-edited fields, but you want to keep other fields between configurations, you must reference the set indexes explicitly:

```
cfgRequest.[setName].data[i].set("fieldName",{"value":"fieldValue"});
```

Replace the following to use in your enrichment:

-   `setName`: The variable name of your set
-   `fieldName`: The variable name of your field
-   `i`: An existing index at which you would like to determine the fieldʼs value
-   `fieldValue`: The value you would like to set for the field

**Note:** To ensure that you are not referencing an empty data array, this call must occur after the set default code in the enrichment script. Otherwise, it will cause a null reference error upon initialization.

You also must guarantee that the index you are referencing in the data exists. Including a check for the length of the set data array is a good way to guarantee that it exists. See the following example.

```
if (cfgRequest.setTest.data.length >= 1) {
     cfgRequest.setTest.data[0].set("setTestNumberField",{"value":cardNumber});
     cfgRequest.setTest.data[0].set("setTestSingleSelect picklist",{"value":"set option 1"});
}
```

Notice that while the `length` function returns “1”, the index is “0”, because indexes are referenced starting at 0 as the first index.

## Configuration experience

[Use Case: Using the Init enrichment to Populate set values](https://www.youtube.com/watch?v=RrhdFJEvT8U)

