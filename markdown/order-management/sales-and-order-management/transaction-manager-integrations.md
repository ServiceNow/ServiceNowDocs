---
title: Transaction Manager: Integrations
description: Use integrations to exchange data with third-party sources, including Salesforce.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 4
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Integrations

Use integrations to exchange data with third-party sources, including Salesforce.

To gather information from external data sources such as Salesforce in Transaction Manager, the admin creates integrations. Transaction Manager integrations define the information necessary to connect to a data source, extract information, and map the data into Transaction Manager. Integrations can also be used to extract information from Transaction Manager and send it to be mapped in a third-party environment.

Before an integration can be defined for Transaction Manager, the admin must first create a connection to the third-party environment, much like an external connection in the configuration environment. Connections are defined in the Utilities section of the Admin UI.

## Creating a connection

Before an integration is defined, the admin must define a connection to the third-party source for the data the integration uses.

To create a new connection, in the Utilities area of the Admin UI, click **Connections**. Then click **+ New** to display the New Connection page.

![Connections screen](../images/cpq-txn-mgr-connections.jpeg)

![New connection screen](../images/cpq-txn-mgr-connection-new.jpeg)

ionsion

On the New Connection page, name the new connection and assign a variable name. Next, choose the integration type: Salesforce or External.

If you are creating a connection to Salesforce, none of the other fields are required. ServiceNow CPQ knows how to authenticate and knows the required endpoints to use when communicating with Salesforce.

If you are creating an external integration, choose the authentication type. Supported authentication methods are None, Bearer Token, and OAuth. If you choose Bearer Token, use the Authentication Token field to provide the bearer token for the site with which you are communicating. If you choose OAuth, use the Client ID, Client Secret, and Token URL fields to provide the required OAuth information.

In the Host field, enter the URL to the third-party site with which you will be communicating.

In the Path field, enter the path to the endpoint that you are trying to access on the third-party site.

Use the Additional Headers field to add any additional header information that is required by the third-party site in order to execute the desired endpoint.

## Creating an integration

To create a new integration, click **+ Add Integration**. The New Integration window appears. Give the new Integration a name and a variable name, and click **Save**.

![Transaction screen](../images/cpq-txn-mgr-integrations.jpeg)

![New Integration screen](../images/cpq-txn-mgr-integration-new.jpeg)

The Integration Editor page opens. Continue defining the new integration by configuring the following settings:

-   **HTTP Method**: You can perform either a GET, POST, PATCH, PUT, or DELETE operation, depending on the endpoint that you are using on the third-party site.
-   **Line Item Details to Include**: Define which type of line items you will work with in the integration. Options are Selected Lines, Modified Lines, and Deleted Lines.
-   **Additional Path**: Enter the query command to execute on the third-party site. If you are connecting to Salesforce, this will probably be a SOQL query. On other platforms, it may be a standard SQL query.
-   **Timeout**: Defines the amount of time \(in milliseconds\) that the request will wait for a response before declaring an error.
-   **Async**: This toggle allows you to run the query asynchronously in the background so that the user can continue working.
-   **Headers**: Set header key-value pairs, utilize static text, header-level Transaction Manager fields using simple handlebar syntax, or a combination of both.`{{txn.fieldname}}`

![Integration screen](../images/cpq-txn-mgr-get-oppty-id.png)

Next, you need to define the connection to the endpoint. Here you choose from a list of the connections that you previously created in the Utilities area to define which third-party site to connect to for this integration.

![Integration screen](../images/cpq-txn-mgr-get-opportunity-id.jpeg)

Finally, you need to define the transformation template, which lets you map third-party data to ServiceNow CPQ fields or map ServiceNow CPQ data to third-party data source fields.

JSON is used to define the mapping, as in the following example.

```
{
  "fields": [
    {
      "variableName": "txn.custom.tXNNumber",
      "value": "{{#each records}}{{Name}}{{/each}}"
    },
    {
      "variableName": "txn.opportunity.id",
      "value": "{{#eachrecords}}{{LGK__OpportunityId__c}} {{/each}}"
    },
    {
      "variableName": "txn.custom.primaryContact",
      "value": "{{#eachrecords}}{{Contact.FirstName}}{{/each}}"
    }
  ]
}
```

This example uses Mustache syntax for the Salesforce data that was extracted from the Salesforce site. Each field mapping includes the variable name of the ServiceNow CPQ field that receives the extracted data, followed by the value that identifies the Salesforce field where the data was extracted. The `#eachredords` and `/each` nomenclature denote that each record in the query response is searched for each of the three field values in the template.

You can use the Sample Return Data area and the Transformation Result area to troubleshoot an Integration that is not working. If you perform the query in a tool like Postman, where you can see and copy the query response, you can paste the query response in the Sample Response Data area and then click **Run Transformation** below the Transformation Template area. The query response data runs through the defined transformation template, and the results of the Transformation is displayed in the Transformation Result area.

