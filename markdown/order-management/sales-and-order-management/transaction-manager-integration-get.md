---
title: Transaction Manager: Integration - GET
description: Learn how to access data from a third-party application such as Salesforce by using the GET integration.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Integration - GET

Learn how to access data from a third-party application such as Salesforce by using the GET integration.

This article describes how to retrieve the Salesforce opportunity ID, together with transaction details including the account name, opportunity name, shipping address, and billing address, and write them into CPQ transaction fields. This pattern is relevant to any integration that requires CPQ to request data from a third party.

## Goal: End-user \(buyside\) flow

We begin by opening a Transaction Manager transaction in Salesforce. Then, by clicking **Get SF Data** in the buyside UI, we trigger the Get SF Data event. This event initiates several integrations that connect to Salesforce, extracting the relevant transaction data \(opportunity ID, opportunity name, shipping address, billing address, account ID, and account name\) and populating the corresponding fields in the buyside UI.

In the buyside transaction UI, click **Get SF Data**.

![Get SF Data](../images/cpq-txn-mgr-integration-get-1.png)

Notice that the details are all populated.

![Transaction stages](../images/cpq-txn-mgr-integration-get-2.png)

![Get SF Data](../images/cpq-txn-mgr-integration-get-3.png)

The rest of this article lists the steps in CPQ to create the integrations that get the data from Salesforce.

## Administration setup: Prerequisites

This guide assumes a CPQ environment with Transaction Manager features enabled, as well as installation of the Logik Transaction Manager Integration Extension on a corresponding Salesforce environment. To view the installation instructions, see [Installing the Salesforce Transaction Manager Integration Package extension](installing-the-salesforce-transaction-manager-integration-package-extension.md).

## CPQ: Add a connection

A connection record contains the data required to initiate a Transaction Manager Integration. This includes authentication details, host URL, path, and headers. To view a connection record, in CPQ Admin, go to **Utilities**, and then click **Connections**.

![Add a Connection](../images/cpq-txn-mgr-integration-get-add-connection.png)

For information about adding a connection, see the "Creating a Connection" section in [Transaction Manager: Integrations](transaction-manager-integrations.md). For the purposes of this article, we use a connection to a Salesforce environment.

## CPQ: Add the integration

1.  Open CPQ Admin and go to the Integrations section.
2.  Click **Add Integration**. Create a new integration using any suitable name. In this example, we use the name "Get Oppty Id".

    ![Add Integration](../images/cpq-txn-mgr-integration-get-add-opp-1.png)

    ![Add Integration](../images/cpq-txn-mgr-integration-get-add-opp-2.png)

    The integration details page shown above includes the following sections:

    -   Integration settings
    -   Request Transformation
    -   Connection to Endpoint
    -   Response Transformation
    Details about these sections follow.


-   Integration settings:

    -   HTTP method: GET
    -   Path: `/services/data/vXX.X/query/?q=SELECT+Name,+LGK__OpportunityId__c FROM+LGK__Transaction__c+WHERE+LGK__ID__c='{{txn.id}}'`

        The GET request retrieves the **Name** and **LGK\_\_OpportunityId\_\_c** fields from the **LGK\_\_Transaction\_\_c** object in Salesforce, filtering by the transaction ID “txn.id” in the **LGK\_\_ID\_\_c** field.

        In the path, `<vXX.X>` is the latest composite graph version. You can check for the latest version [here](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_graph.htm).

    -   Line Item Details to Include: Selected Lines
    -   Timeout: 2000 ms
    ![Add Integration](../images/cpq-txn-mgr-integration-get-add-opp-3.png)

    Click **Next**.

-   Request Transformation: Not required when we are building a GET Integration.
-   Connection to Endpoint: For this example, we are querying **Salesforce**. If you are setting up an integration with another system, select the appropriate connection.

    ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-4.png)

    Click **Next**.

-   Response Transformation: See this sample response transformation template.

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
        }
      ]
    }
    ```


## New integration: Retrieve opportunity details

Create another integration to get additional details through **txn.opportunity.id**.

Now that we have the opportunity ID, the next step in the integration involves using it as a reference to retrieve additional details from the opportunity and to populate the relevant LGK transaction fields.

![Admin transaction](../images/cpq-txn-mgr-integration-get-retrieve-opp-1.png)

-   Integration settings:

    -   HTTP method: GET
    -   Path: `GET /services/data/vXX.X/query?q=SELECT Id,Name,Owner.Username,AccountId,Account.Name,Account.BillingAddress,Account.ShippingAddress FROM Opportunity WHERE Id='{{txn.opportunity.id}}'`

        This query retrieves fields from an Opportunity record in Salesforce, based on the unique ID of the opportunity. It also retrieves related account details, such as the account's name, billing address, and shipping address. The query returns data for a specific opportunity identified by **\{\{txn.opportunity.id\}\}**.

        To get the field details from Salesforce, click **Setup** &gt; **Object Manager** &gt; **Opportunity** &gt; **Fields &amp; Relationships**.

        ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-2.png)

    -   Line Item Details to Include: Selected Lines
    -   Timeout: 2000 ms

        ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-3.png)

    Click **Next**.

-   Request Transformation: not required when building a GET integration.
-   Connection to Endpoint:

    Select **Connection to Endpoint**. For this example, we are querying Salesforce. If you are setting up an integration with another system, select the appropriate connection.

    ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-4.png)

    Click **Next**.

-   Response Transformation: The following JSON snippet defines how to populate variables defined in additional path by iterating over a collection of `records`.

    For **txn.custom.opportunity**, it extracts the **Name** field from each record, while for **txn.custom.billToAddress**, it extracts and concatenates the **Account.BillingAddress.street,Account.BillingAddress.city,Account.BillingAddress.state,Account.BillingAddress.postalCode** field. The Handlebars **\{\{\#each\}\}** loop is used to process each record, and the resulting values depend on the system's handling, either as concatenated strings or arrays of values.

    ```
    {
      "fields": [
        {
          "variableName": "txn.custom.opportunity",
          "value": "{{#each records}}{{Name}}{{/each}}"
        },
        {
          "variableName": "txn.account.id",
          "value": "{{#each records}}{{AccountId}}{{/each}}"
        },
        {
          "variableName": "txn.custom.accountName",
          "value": "{{#each records}}{{Account.Name}}{{/each}}"
        },
        {
          "variableName": "txn.custom.quoteNumber",
          "value": "{{#each records}}{{QuoteNumber}}{{/each}}"
        },
        {
          "variableName": "txn.custom.billToAddress",
          "value": "{{records.[0].Account.BillingAddress.street}}{{records.[0].Account.BillingAddress.city}}{{records.[0].Account.BillingAddress.state}}{{records.[0].Account.BillingAddress.postalCode}}"
        },
        {
          "variableName": "txn.custom.shipToAddress",
          "value": "{{records.[0].Account.ShippingAddress.street}}{{records.[0].Account.ShippingAddress.city}}{{records.[0].Account.ShippingAddress.state}}{{records.[0].Account.ShippingAddress.postalCode}}"
        }
      ]
    }
    ```


Trigger the integration when the end user clicks a button. You can now click **Events** to create a new event or to select an existing one. In this case, we use the Get SF Data event \(a button in the UI\) to connect to the integrations we previously created.

![Admin transaction](../images/cpq-txn-mgr-integration-get-retrieve-opp-5.png)

Click **Add New Action**.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-6.png)

Click **Integrations**.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-7.png)

Search for and add the "Get Oppty Id" integration.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-8.png)

Click **Save**. Then, click **Add New Action** and add "retrieveSFOptyData".

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-9.png)

Click the up and down arrows next to the action items to arrange them in the desired order. \(Here, we are selecting "Get Oppty Id", followed by "Retrieve SF Opty Data", to fetch the opportunity ID and retrieve relevant data.\)

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-10.png)

Click **Save**, and deploy the changes.

We have discussed how integrations can be added with events. Integrations can also be configured at the stage level. To do so, navigate to **Stages** &gt; **Edit Settings** &gt; **Add New Action** &gt; **Integration**.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-11.png)

## Troubleshooting

When configuring integrations, it is crucial to ensure that the sequence of integrations is set up correctly to retrieve accurate details. The order of execution plays a significant role in maintaining data consistency and alignment.

To achieve this, follow these steps:

1.  Fetch the opportunity ID: The opportunity ID serves as the key reference for linking related data. This step is essential because the transaction details you retrieve later are directly associated with a specific opportunity.
2.  Fetch the transaction ID through opportunity details: Use the opportunity ID to fetch the transaction ID. Because each transaction is linked to a particular opportunity, this approach ensures that you accurately associate the correct transaction with its corresponding opportunity.

By following this order, you can maintain the integrity of the integration and ensure that the data flow remains seamless and reliable.

**Related topics**  


[Transaction Manager: Integration - POST](transaction-manager-integration-post.md)

