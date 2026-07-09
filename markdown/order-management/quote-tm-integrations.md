---
title: Quote transaction integrations
description: Integrations connect ServiceNow Quote Experience to external data sources, enabling the exchange of data between quotes and third-party systems such as Salesforce in ServiceNow CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-integrations.html
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Configuring Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Quote transaction integrations

Integrations connect ServiceNow Quote Experience to external data sources, enabling the exchange of data between quotes and third-party systems such as Salesforce in ServiceNow CPQ.

ServiceNow Quote Experience integrations define the information needed to connect to an external data source, extract data from it, and map that data into ServiceNow Quote Experience fields. Integrations can also extract data from ServiceNow Quote Experience and send it to a third-party environment. Before an integration can be defined, the administrator must first create a connection to the target environment.

## Connection types

ServiceNow Quote Experience supports two connection types.

-   **Salesforce**

    Connects to a Salesforce environment. No additional authentication details are required — ServiceNow CPQ handles authentication and knows the required endpoints automatically.

-   **External**

    Connects to any third-party site. Supported authentication methods are None, Bearer Token, and OAuth. For Bearer Token, provide the authentication token. For OAuth, provide the Client ID, Client Secret, and Token URL. Also requires the Host URL, the Path to the endpoint, and any additional headers required by the third-party site.


## Integration settings

When creating an integration, the following settings are available in the Integration Editor.

-   **HTTP Method**

    The operation to perform: GET, POST, PATCH, PUT, or DELETE, depending on the endpoint being used.

-   **Line Item Details to Include**

    Defines which line items the integration works with: Selected Lines, Modified Lines, or Deleted Lines.

-   **Additional Path**

    The query command to execute on the third-party site. For Salesforce connections, this is typically a SOQL query. For other platforms, it may be a standard SQL query.

-   **Timeout**

    The time in milliseconds that the request waits for a response before declaring an error.

-   **Async**

    When enabled, runs the query asynchronously in the background so the user can continue working while the integration executes.

-   **Headers**

    Static text or ServiceNow Quote Experience header field values can be included in headers using handlebar syntax: `{{txn.fieldname}}`. Static key-value pairs can also be set, or both methods can be combined.


## Transformation template

The transformation template defines the mapping between third-party data and ServiceNow CPQ fields. It uses JSON with Mustache \(handlebar\) syntax for dynamic field extraction. The following example maps Salesforce fields to ServiceNow Quote Experience fields.

```
{
  "fields": [
    {
      "variableName": "txn.custom.tXNNumber",
      "value": "{{#each records}}{{Name}}{{/each}}"
    },
    {
      "variableName": "txn.opportunity.id",
      "value": "{{#each records}}{{LGK__OpportunityId__c}}{{/each}}"
    },
    {
      "variableName": "txn.custom.primaryContact",
      "value": "{{#each records}}{{Contact.FirstName}}{{/each}}"
    }
  ]
}
```

Use the **Sample Return Data** and **Transformation Result** areas to test and troubleshoot an integration. Paste the query response from a tool such as Postman into the Sample Return Data area and select **Run Transformation** to verify that the mapping produces the expected output.

