---
title: Transaction Manager: Integration - POST
description: Learn how to write data to a third-party application such as Salesforce by using the POST integration.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Integration - POST

Learn how to write data to a third-party application such as Salesforce by using the POST integration.

## Prerequisites

This article assumes that you have a CPQ environment that is integrated to a corresponding Salesforce environment. Before you continue, see [Installing the Salesforce Transaction Manager Integration Package extension](installing-the-salesforce-transaction-manager-integration-package-extension.md) to complete the necessary integrations.

When the end user initiates a function that writes CPQ data back to the corresponding Salesforce transaction record, CPQ must have the Salesforce transaction’s record identifier on hand. To understand how to retrieve the Salesforce transaction ID and save it into CPQ for future use, see [Transaction Manager: Integration - GET](transaction-manager-integration-get.md).

## Salesforce setup

In this example, we write LGK data to the Salesforce fields listed below. Review the Salesforce Transaction and TransactionLine objects to ensure these fields are present.

Header fields \(Salesforce object:**LGK\_\_Transaction\_\_c**\)

-   **LGK\_\_Stage\_\_c** holds the stage of the CPQ transaction.
-   **LGK\_\_PricingExtendedNet\_\_c** is the transaction \(header-level\) net total.
-   **LGK\_\_Id\_\_c** is mapped to the **id** of the parent transaction.

Line Fields \(Salesforce object: **LGK\_\_TransactionLine\_\_c**\)

-   **LGK\_\_Quantity\_\_c**: the line-level quantity.
-   **LGK\_\_PricingList\_\_c**: the line-level list price.
-   **LGK\_\_PricingNet\_\_c**: the line net price, or discounted piece price.
-   **LGK\_\_PricingExtendedNet\_\_c**: the line net total, or extended net price \(includes quantity\).
-   **LGK\_\_ParentTransactionLineId\_\_c** checks whether **txn.line.custom.parentLineReferenceId** exists. If it does, it assigns the corresponding line's **id**; otherwise, it sets the value to **null**.
-   **LGK\_\_Product2Id\_\_c** is mapped to the **partnerId** of the product associated with the current transaction line.

## POST integration using Composite Graph

The LGK POST integration uses the Salesforce Composite Graph API to update multiple Salesforce objects simultaneously in a single API call, allowing both header-level and line-level fields to be updated in the same request.

The Salesforce Composite Graph API enables bundling multiple operations into a single request, making it highly efficient for integrations. It allows writing to multiple Salesforce objects in a single POST call, reducing API usage, ensuring data consistency, and enabling atomic transactions—where either all operations succeed or none are applied. This simplifies integration processes and improves error handling. For more details on the Composite Graph construct, see [Composite Graph \| REST API Developer Guide \| Salesforce Developers](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_graph.htm).

Because the Composite Graph API is a core Salesforce capability, no setup is necessary. However, we introduce the concept here, before we populate a Composite Graph in the LGK POST call, described below. In the example below for POST, the integration uses the previously mentioned header-level and line-level fields in the Salesforce Setup section above, with the option for users to add or remove fields as per their requirements.

## Transaction Manager setup

The transaction ID mappings mentioned in the Salesforce Setup section help CPQ send the right line IDs to Salesforce and manage updates, deletions, and additions effectively. By mapping LGK\_\_TransactionId\_\_c to the parent transaction ID, Salesforce can link all line-level changes to the correct transaction, ensuring proper association. The LGK\_\_ParentTransactionLineId\_\_c checks for a parent line reference; if present, it assigns the corresponding line ID, ensuring that only valid lines are updated or deleted. If no reference exists, it sets the value to null. The LGK\_\_Product2Id\_\_c maps to the product’s partner ID, ensuring the correct product is linked to the line for accurate pricing and discount application. These dynamic mappings ensure that Salesforce can accurately update quantities, delete lines, and add new ones while preserving user's line-level discounts by maintaining proper associations with transaction and product data.

This integration transform requires the use of two custom line fields, **lineReferenceId** and **parentLineReferenceId**. These fields must be set up to store a variation of the **txn.line.id** and \(potentially\) **txn.line.parent.id** system fields.

## Rules

The Salesforce Composite Graph API does not support hyphens in certain identifiers, which can cause issues when sending data that includes hyphenated IDs, such as the LGK line IDs. To make the integration work, the system removes any hyphens present in the LGK line IDs before sending them to Salesforce. This ensures that the IDs comply with Salesforce's format requirements and that the integration functions correctly without errors related to invalid characters. By removing the hyphens, the system ensures that all identifiers are accepted by Salesforce, allowing the integration to process updates and other operations smoothly.

To remove hyphens by using a rule, create a determination rule action to make line-level reference Id fields Salesforce-compatible. You can add both the lineReferenceId determination action and parentLineReferenceId determination action in a single rule.

Below are two determination scripts \(transaction line level\) for how the fields should be defined.

```
// lineReferenceId Determination Action

var original = txn.line.id;
var result = "";
for (var i = 0; i < original.length; i++) {
  if (original.charAt(i) !== "-") {
	    result += original.charAt(i);
	  }
}
return result;
```

```
// parentLineReferenceId Determination Action

var original = txn.line.parent.id;
var result = "";
if (txn.line.parent.id != txn.id) {
  for (var i = 0; i < original.length; i++) {
    if (original.charAt(i) !== "-") {
        result += original.charAt(i);
      }
  }
}
return result;
```

The rule should be configured as follows, with two determination actions to handle **txn.line.custom.lineReferenceId** and **txn.line.custom.parentLineReferenceId**:

![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-rules-1.png)

![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-rules-2.png)

Add Connection

The screenshot below shows the external connection as “Salesforce” in the POST integration.

If you want to create a new connection, see the "Creating a Connection" section in [Transaction Manager: Integrations](transaction-manager-integrations.md).

![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-add-connection.png)

To POST data back to Salesforce, you need the Salesforce transaction record ID. If you have not yet set up the GET integration to fetch the transaction ID, see [Transaction Manager: Integration - GET](transaction-manager-integration-get.md).

## Add integration

1.  Navigate to the Integrations section and create a new integration.
    -   HTTP Method: POST
    -   Additional Path:**/services/data/vXX.X/composite/graph**, where **vXX.X** is the latest composite graph version. You can check for the latest version [here](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_graph.htm).
    -   Line Item Details to Include: Selected Lines
    -   Connection: Salesforce

        ![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-add-1.png)

2.  In the Request Transformation section, add this sample transaction JSON \(header and line-level fields may vary according to your preference\):

```
{
  "graphs": [
    {
      "graphId": "graph0",
      "compositeRequest": [
        {
          "method": "PATCH",
          "url" : "/services/data/v61.0/sobjects/LGK__Transaction__c/LGK__TransactionUUID__c/{{txn.id}}",
          "referenceId": "parentTransaction",
          "body": {
            "LGK__Stage__c": "{{txn.stage}}",
            "LGK__NetTotal__c": "{{txn.pricing.total}}"
          }
        }
        {{#if lines}}
				{{~#each lines~}}
				{{#if txn.line.product.partnerId}}
				,
        {
          "method": "PATCH",
          "url": "/services/data/v61.0/sobjects/LGK__TransactionLine__c/LGK__TransactionLineId__c/{{txn.line.id}}",
          "referenceId": "line_{{txn.line.custom.lineReferenceId}}",
          "body": {
            "LGK__TransactionId__c": "@{parentTransaction.id}",
            "LGK__ParentTransactionLineId__c": {{#if txn.line.custom.parentLineReferenceId}}"@{line_{{txn.line.custom.parentLineReferenceId}}.id}"{{else}}null{{/if}},
            "LGK__Product2Id__c": "{{txn.line.product.partnerId}}",
            "LGK__Quantity__c": "{{txn.line.quantity}}",
            "LGK__ListPrice__c": "{{txn.line.pricing.list}}",
            "LGK__NetPrice__c": "{{txn.line.pricing.net}}",
            "LGK__NetTotal__c": "{{txn.line.pricing.extendedNet}}"
          }
        }
        {{/if}}
		{{/each}}
		{{/if}}
      ]
    }
  ]
}
```

This transformation template is added to the Transformation Template area of the Request Transformation section as follows:

![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-add-2.png)

For more information about Handlebar syntax, see [Transaction Manager: Integrations - Handlebars syntax](transaction-manager-integrations-handlebar-syntax.md).

## Debugging the POST call

To use the Integration Admin interface to debug a POST call that is not working as expected, follow these steps:

1.  Copy the transaction ID for which the integration is not working, paste it in the small Transaction ID box, and then click **Fetch JSON**.

    ![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-debug-1.png)

    The application populates the Sample Transaction JSON box.

    ![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-debug-2.png)

2.  Click **Run Transformation**. This processes the transaction information contained in the Sample Transaction JSON input through the transformation logic and generates a result that you can test using Postman.

    For more information about setting up Postman to interface with your Salesforce org, see [Connect Postman to Salesforce](https://quickstarts.postman.com/guide/connect-postman-to-salesforce/index.html).

    ![Transaction Manager Setup](../images/cpq-txn-mgr-integration-post-debug-3.png)


**Related topics**  


[Transaction Manager: Integration - GET](transaction-manager-integration-get.md)

