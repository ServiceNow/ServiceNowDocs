---
title: Create a ServiceNow Quote Experience integration
description: Create an integration in ServiceNow Quote Experience to define the connection, settings, and field mapping that exchanges data between a quote and an external system in CPQ.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-integration.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Integrations, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a ServiceNow Quote Experience integration

Create an integration in ServiceNow Quote Experience to define the connection, settings, and field mapping that exchanges data between a quote and an external system in CPQ.

## Before you begin

A connection to the target environment must exist before you create an integration. For more information, see [Create a connection for ServiceNow Quote Experience calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-a-connection.md).

Role required: admin

## About this task

Integrations define how ServiceNow Quote Experience exchanges data with external systems. Each integration specifies the HTTP operation, which lines to include, how to authenticate via a connection, and how to map external data to CPQ fields using a transformation template. Integrations are assigned to stages and events to trigger them during the quote lifecycle.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transactions** &gt; **Integrations**

2.  Select **+ Add Integration**.

3.  Enter a name and verify the variable name, then select **Save**.

    The variable name is set in camel case from the name you enter. To use a custom variable name, select the pencil icon to the right of the **Variable Name** field before saving.

    The Integration Editor opens.

4.  Configure integration settings
5.  In the **HTTP Method** field, select the operation to perform on the third-party endpoint.

    -   Select **GET** to retrieve data from the external system.
    -   Select **POST** to send new data to the external system.
    -   Select **PATCH** to partially update a record on the external system.
    -   Select **PUT** to replace a record on the external system.
    -   Select **DELETE** to remove a record on the external system.
6.  In the **Line Item Details to Include** field, select which quote lines the integration works with.

    -   Select **Selected Lines** to operate on the lines the user has selected.
    -   Select **Modified Lines** to operate on lines that have changed in the current session.
    -   Select **Deleted Lines** to operate on lines that have been removed from the quote.
7.  In the **Additional Path** field, enter the query command to execute on the third-party site.

    For Salesforce connections, this is typically a SOQL query. For other platforms, it may be a standard SQL query.

8.  In the **Timeout** field, enter the number of milliseconds the request waits for a response before declaring an error.

9.  Enable the **Async** toggle to run the integration in the background so the user can continue working while the request executes.

10. In the **Headers** area, configure the headers to include with the request.

    Three approaches are available and can be combined.

    -   **ServiceNow Quote Experience field values** — Reference transaction-level field values in a header using handlebar \(Mustache\) syntax: `{{txn.fieldname}}`. For example, `{{txn.account.id}}` passes the account ID from the quote header into the request header.
    -   **Static key-value pairs** — Enter fixed header keys and values directly, such as an authorization token or a content type override.
    -   **Combined** — Mix static values and field references in the same header configuration.
11. In the connection selector, choose the connection to the target environment from the list of previously created connections.

    Connections are created in the Utilities area. If the required connection does not appear, create it first. For more information, see [Create a connection for ServiceNow Quote Experience calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configure-a-connection.md).

12. Define the transformation template
13. In the **Transformation Template** area, enter the JSON that maps external data to CPQ fields, or maps CPQ data to external system fields.

    The template uses JSON with Mustache \(handlebar\) syntax to extract values from the external response. Each object in the `fields` array contains a `variableName` \(the CPQ field that receives the data\) and a `value` \(the expression that identifies the external field to extract from\). Use `{{#each records}}` and `{{/each}}` to iterate over records in the query response.

    The following example maps three Salesforce fields to CPQ transaction fields.

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

    In this example, each `variableName` is a CPQ field that receives the extracted value. The `{{#each records}}` / `{{/each}}` block iterates over each record in the query response and extracts the named Salesforce field.

14. To verify the transformation template before saving, paste a sample query response into the **Sample Return Data** area, then select **Run Transformation** below the Transformation Template area.

    To obtain sample response data, run the same query in a tool such as Postman where you can view and copy the full response, then paste it into the **Sample Return Data** area.

    The query response data runs through the transformation template and the mapped output is displayed in the **Transformation Result** area. If the result does not match the expected field values, review the template syntax and field variable names.

15. Select **Save**.

    The integration is saved and available to assign to stages and events.


## What to do next

Assign the integration to an event or a stage to trigger it during the quote lifecycle.

-   To assign to an event, see [Create an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-custom-event.md).
-   To assign to a stage, see [Create a quote transaction stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-stage.md).

