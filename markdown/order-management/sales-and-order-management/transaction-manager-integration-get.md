---
title: Transaction Manager: Integration - GET
description: Learn how to access data from a third-party application such as Salesforce by using the GET integration.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-12"
reading_time_minutes: 5
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Integration - GET

Learn how to access data from a third-party application such as Salesforce by using the GET integration.

This article describes how to retrieve the Salesforce Opportunity ID and transaction details such as Account Name, Opportunity Name, Shipping Address, and Billing Address, and write them into ServiceNow CPQ Transaction fields. This pattern is relevant to any integration that requires ServiceNow CPQ to request data from a third party.

## Goal: End-user \(buyside\) flow

We begin by opening a Transaction Manager transaction in Salesforce. Then, by clicking **Get SF Data** in the buyside UI, we trigger the Get SF Data event. This event initiates several integrations that connect to Salesforce, extracting the relevant transaction data \(Opportunity ID, Opportunity Name, Shipping Address, Billing Address, Account ID, Account Name\) and populating the corresponding fields in the buyside UI.

Click **Get SF Data** in the buyside transaction UI.

![Get SF Data](../images/cpq-txn-mgr-integration-get-1.png)

Notice that the details are all populated, including Opportunity Id, Opportunity Name, Ship To Address, Bill To Address, Account Id, and Account Name.

![Transaction stages](../images/cpq-txn-mgr-integration-get-2.png)

![Get SF Data](../images/cpq-txn-mgr-integration-get-3.png)

The rest of this article will discuss the steps involved in ServiceNow CPQ to create the integrations that will get the data from Salesforce.

## Administration setup: Prerequisites

This guide assumes a ServiceNow CPQ environment with Transaction Manager features enabled, as well as installation of the [Logik Transaction Manager Integration Extension](https://logikio.atlassian.net/wiki/spaces/CS/pages/1837367311/Txn+Mgr+-+Salesforce+Integration+Package+Installation) on a corresponding Salesforce environment.

## ServiceNow CPQ: Add a connection

A connection record contains the data required to initiate a Transaction Manager Integration. This includes authentication details, host URL, path, and headers. Navigation: ServiceNow CPQ Administration → Utilities → Connections.

![Add a Connection](../images/cpq-txn-mgr-integration-get-add-connection.png)

For information about adding a connection, see the "Creating a Connection" section in [Transaction Manager: Integrations](transaction-manager-integrations.md). For the purposes of this article, we will be using a connection to a Salesforce environment.

## ServiceNow CPQ: Add the integration

1.  Open ServiceNow CPQ Admin and go to the "Integrations" section.
2.  Click **Add Integration**. Create a new integration using any suitable name. In this example, we use "Get Oppty Id".

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

        The GET request retrieves the Name and LGK\_\_OpportunityId\_\_c fields from the LGK\_\_Transaction\_\_c object in Salesforce, filtering by a specific transaction ID “txn.id” in the LGK\_\_ID\_\_c field.

        In the path, &lt;vXX.X&gt; is the latest composite graph version. You can check for the latest version [here](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/resources_composite_graph.htm).

    -   Line Item Details to Include: Selected Lines
    -   Timeout: 2000 ms
    ![Add Integration](../images/cpq-txn-mgr-integration-get-add-opp-3.png)

    Click **Next**.

-   Request Transformation: Not required when we are building a GET Integration.
-   Connection to Endpoint: For this example, we are querying “Salesforce“. If you are setting up an integration with another system, select the appropriate connection.

    ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-4.png)

    Click `Next`.

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

Create another integration to get additional details through “txn.opportunity.id”.

Now that we have the Opportunity ID, the next step in the integration involves using the Opportunity ID as a reference to retrieve additional details from the Opportunity and populate the relevant LGK transaction fields.

![Admin transaction](../images/cpq-txn-mgr-integration-get-retrieve-opp-1.png)

-   Integration settings:
    -   HTTP method: GET

        Path: `GET /services/data/vXX.X/query?q=SELECT Id,Name,Owner.Username,AccountId,Account.Name,Account.BillingAddress,Account.ShippingAddress FROM Opportunity WHERE Id='{{txn.opportunity.id}}'`

        This query retrieves fields from an Opportunity record in Salesforce, based on the unique Id of that Opportunity. It also retrieves related Account details, such as the Account's name, billing address, and shipping address. The query will return data for a specific Opportunity identified by \{\{txn.opportunity.id\}\}.

        To get the field details from salesforce, click setup ---&gt; Object Manager ----&gt; Opportunity ---&gt; Fields &amp; Relationships.

        ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-2.png)

        Line Item Details to Include: Selected lines

        Timeout: 2000 ms

        ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-3.png)

        Click Next.

-   Request Transformation: not required when building a GET integration.
-   Connection to Endpoint:

    Select Connection to Endpoint. For this example, we are querying “Salesforce“. If you are setting up an integration with another system, select the appropriate connection.

    ![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-4.png)

    Click **Next**.

-   Response Transformation: The following JSON snippet defines how to populate variables defined in additional path by iterating over a collection of `records`.

    For `txn.custom.opportunity`, it extracts the `Name` field from each record , while for `txn.custom.billToAddress`, it extracts and concatenates the `Account.BillingAddress.street,Account.BillingAddress.city,Account.BillingAddress.state,Account.BillingAddress.postalCode` field. The Handlebars `{{#each}}` loop is used to process each record, and the resulting values depend on the system's handling—either as concatenated strings or arrays of values.

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


Trigger the integration when the end-user clicks a button/event. You can now click **Events** to either create a new event or select an existing one. In this case, we will use the Get SF Data event \(which is a button on UI\) to connect to the integrations we previously created.

![Admin transaction](../images/cpq-txn-mgr-integration-get-retrieve-opp-5.png)

Click **Add New Action**.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-6.png)

Click **Integrations**.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-7.png)

Search for and add the "Get Oppty Id" integration.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-8.png)

Click **Save**. Then, click **Add New Action** and add "retrieveSFOptyData".

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-9.png)

Click the up and down arrows next to the action items to arrange them in the desired order. \(Here, we are selecting "Get Oppty Id" first, followed by "Retrieve SF Opty Data", to fetch the Opportunity ID and then retrieve all relevant data of opportunity.\)

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-10.png)

Click **Save**, and deploy the changes.

We have discussed how integrations can be added with events. Alternately, integrations can be configured at the stage level. To do so, go to Stages ---&gt; Edit Settings ---&gt; Add New Action ---&gt; Integration.

![Add Integration](../images/cpq-txn-mgr-integration-get-retrieve-opp-11.png)

## Troubleshooting

When configuring integrations, it is crucial to ensure that the sequence of integrations is set up correctly to retrieve accurate details. The order of execution plays a significant role in maintaining data consistency and alignment.

To achieve this, follow these steps:

1.  Fetch the Opportunity ID: Begin by fetching the `Opportunity Id` as it serves as the key reference for linking related data. This step is essential because the transaction details you will retrieve later are directly associated with a specific opportunity.
2.  Fetch the Transaction ID Through Opportunity Details: Once you have the `Opportunity Id`, use it to fetch the `Transaction Id`. Since each transaction is linked to a particular opportunity, this sequential approach ensures that you accurately associate the correct transaction with its corresponding opportunity.

By following this order, you can maintain the integrity of the integration and ensure that the data flow remains seamless and reliable.

