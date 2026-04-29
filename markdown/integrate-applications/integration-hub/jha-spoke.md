---
title: Jack Henry jXchange Spoke
description: Integrate ServiceNow instance with your Jack Henry jXchange account to access customer and account information.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Jack Henry jXchange Spoke

Integrate ServiceNow instance with your Jack Henry jXchange account to access customer and account information.

**Important:** Starting with the Utah release, the Financial Services Operations Integration with Jack Henry Associates \(JHA\) jXchange application has been renamed to Financial Services Operations Integration with Jack Henry jXchange.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

The current version of the Jack Henry Associates jXchange spoke is v 2.0.3.

## Spoke requirements

Ensure that you contact Jack Henry jXchange admin and have these details ready:

-   Username of your Jack Henry jXchange account.
-   Password of your Jack Henry jXchange account.
-   Valid Consumer Name.
-   Valid Consumer Product.
-   Institute Routing ID.
-   Institute Environment.
-   SOAP Connection URL.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Integration Hub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Jack Henry jXchange spoke provides sample flows to demonstrate automating tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Look up Transactions Updates|Triggers the Look up Transactions Updates subflow and retrieves the latest transactions updates.|
|Sample Get Customers Information flow|Retrieves the customer information and logs it.|

## Spoke subflows

The Jack Henry jXchange spoke provides a sample subflow, Look up Transactions Updates subflow to demonstrate retrieving the latest transactions updates. To customize the sample subflow, copy it to a new application scope.

## Spoke actions

The Jack Henry jXchange spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Customer Information Management|Look up Customer Information by ID|Retrieves customer information based on customer identifier.|
|Look up Customers Information Stream|Retrieves customer information existing on a service provider.|
|Financial Account Information Management|Look up Financial Account by Account Details|Retrieve financial account information of a customer by account details existing on a service provider.|
|Look up Financial Accounts Stream|Retrieves financial account information of customers existing on a service provider.|
|Look up Financial Transactions Stream|Retrieves financial account transactions of an account existing on a service provider.|
|Update Financial Account Deposit Balance|Updates deposit balance of a financial account existing on a service provider.|

## Spoke module

The Jack Henry jXchange spoke adds the Financial Services Operations application to your instance and includes these modules:

<table id="table_lyw_4y5_f5b"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customers

</td><td>

Retrieves and displays the customer data from your Jack Henry jXchange account. When a user navigates to, **JHA** &gt; **Remote Tables** &gt; **Customers**, the Look up Customers Information Stream action is triggered and data is retrieved.

</td></tr><tr><td>

Accounts

</td><td>

Retrieves and displays the account data from your Jack Henry jXchange account.When a user navigates to, **JHA** &gt; **Remote Tables** &gt; **Accounts**, the Look up Financial Accounts Stream action is triggered and data is retrieved.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Jack Henry jXchange spoke](../task/jha-spk-setup.md).

