---
title: Passing array variables using Salesforce external connection
description: You must use single quote strings when making a SOQL query to Salesforce.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Passing array variables using Salesforce external connection

You must use single quote strings when making a SOQL query to Salesforce.

Salesforce supports only single quote strings in a SOQL query. Therefore, the following inputs would not be recognized by Salesforce.

```
let inputs = { "productsArray": '("Tablet10", "Laptop13", "Laptop15")' }
```

Instead, use single quotes as in the following snippet.

```
let inputs = { "productsArray": "('Tablet10', 'Laptop13', 'Laptop15')" }
```

The following sample script pulls Salesforce IDs.

```
// Array of Salesforce IDs
const idList = ['0066e00001pGlTUAA0', '0066e00001pGlTTAA0', '0066e00001pGlTPAA0'];

// Create a string to pass to the SOQL IN query
// first part: "('" = opening parenthesis and single quote
// middle part: idList.join("','") = join all the Salesforce Ids with single quote, a comma and single quote
// last part: "')" = single quote and closing parenthesis
const soqlIn = "('" + idList.join("','") + "')";

// inputs to the SOQL query and calling SF connection
const inputs = {"idList": soqlIn};
const response = Salesforce.<yourExternalConnectionVariableName>(inputs);
```

**Related topics**  


[Using external connections with OAuth support](using-external-connections-with-oauth-support.md)

[Passing data from Salesforce to CPQ fields](enrichments_on_pass_data_from_salesforce_to_logik_io_fields.md)

