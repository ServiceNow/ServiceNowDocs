---
title: Quote line unique IDs
description: You can assign unique IDs to quote lines in Salesforce.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Quote line unique IDs

You can assign unique IDs to quote lines in Salesforce.

CPQ passes the unique identifier of a product in CPQ back to the Unique Line ID field on the quote line in Salesforce, allowing users to assign unique IDs to specific quote lines in Salesforce. This allows users to reference the Unique Line ID field \(LGK\_UniqueId\_c\) after the quote line has been created if a unique identifier was included in the product action in CPQ.

![Product action](../images/cpq-salesforce-quote-line-unique-id.png)

![Quote line details](../images/cpq-quote-line-unique-id.png)

## Prerequisites

Have the Logik Extension for CPQ package version 2.2 or later installed on the org.

Add the Unique Line ID field to the quote line page layout through Setup&gt;Object Manager&gt;Quote Line&gt;Page Layouts.

Assign a unique identifier to a product in CPQ using a simple or advanced product action.

## How to use

For simple product actions, assign the product unique identifier in the product action. \(See the screenshot above.\)

For advanced product actions, assign the ProductList.uniqueIdentifer in your product action script. For example, if using a set, you can leverage the set index in order to assign a unique ID to each product added from the set:

```
ProductList.id ="<yourProductCodeOrId>";
ProductList.uniqueIdentifier = cfg.<yourSetFieldForProduct> + set.<yourSetVariableName>.index;
return ProductList;
```

Use cases include ramping deals, such as subscription-based pricing that applies discounts based on the length of the contract. Although the same product, discounts are applied in year 2 or 3 with a unique ID for the same product name. Another use case would be multiple copies of the same product on quote, with different product extended data.

## Use case: Adding extended data to identical product code products in SFDC using flows

Out of the box, the Configuration Line Item to Quote Line flow created by CPQ is set up to write the extended information of each product to its respective quote line in the BOM Data field.

![Quote line user interface](../images/cpq-quote-line-bom-data.png)

As configured, the flow checks only whether the configuration ID and the product ID match and return only the first record. This causes the BOM data for the child lines to be identical if the product IDs are identical.

If you are using the unique ID attribute, you can add another condition to the "Get Records" section of the flow that checks for the Configuration Line Item field "LGK\_UniqueId\_c" being equal to the unique line ID object on the quote line:

![Edit GET records](../images/cpq-quote-line-edit-get-records.png)

This correctly writes the BOM data to each unique child line with the correct extended information.

