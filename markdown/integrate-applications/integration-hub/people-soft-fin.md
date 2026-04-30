---
title: Oracle Peoplesoft Financial Spoke
description: Manage finances and procurement in the Oracle Peoplesoft Financial instance from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Peoplesoft Financial Spoke

Manage finances and procurement in the Oracle Peoplesoft Financial instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Peoplesoft Financial spoke v1.0.7 is the latest version.

## Supported versions

-   PeopleSoft FSCM 9.2 Update Image 37
-   PeopleTools 8.58.05
-   Oracle Database 19.3.0.0
-   Elasticsearch 7.0.0
-   Kibana 7.0.0
-   Oracle Linux 7.8x
-   Oracle Database version above 12.2.0.0
-   PeopleTools above 8.56

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Remote Tables \(com.glide.script.vtable\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow IntegrationHub Action Step - XML Parser \(com.glide.hub.action\_step.xmlparser\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Oracle Peoplesoft Financial spoke provides a sample flow, Create PO, to demonstrate automating the PO creation. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The Oracle Peoplesoft Financial spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|BU and Vendor Validation|Validates if a vendor or business unit exists in Oracle Peoplesoft Financial.|
|Create PO After BU Validation|Validates a business unit before creating a purchase order using that business unit.|
|Polling Suppliers|Retrieves details of the daily suppliers based on the mentioned polling frequency and creates or updates records in PSFT data table based on Vendor ID.|

## Spoke actions

The Oracle Peoplesoft Financial spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Finance|Create Bulk Journals|Creates bulk journals.|
|Create Invoice|Creates an invoice in Oracle Peoplesoft Financial.|
|Get Business Unit By Business Unit ID|Retrieves details of the specified business unit.|
|Get Department By Department ID|Retrieves the department cost center details of the specified department.|
|Get Gl Account Details|Retrieves details of the specified GI account.|
|Get Item Details|Retrieves details of the items, based on the input criteria.|
|Lookup AP Invoice Line|Retrieves the AP invoice line details of the specified voucher.|
|Lookup AP Invoice Header|Retrieves details of the AP invoice headers, based on the input criteria.|
|Lookup Business Units|Retrieves details of the business units, based on the input criteria.|
|Lookup Currency Rate|Retrieves details of the currency market rate, based on the input criteria.|
|Lookup Departments|Retrieves details of the departments, based on the input criteria.|
|Lookup Gl Balance|Retrieves details of the GI balance, based on the input criteria.|
|Lookup Invoice Payment Status|Retrieves the list of invoice statuses, based on the input criteria.|
|Procurement|Cancel PO|Cancels the specified PO.|
|Create Bid Event|Creates a bid event in the specified business unit.|
|Create Bulk Assets|Creates assets with the provided details.|
|Create Bulk Goods Receipts|Creates good receipts with the provided details.|
|Create PO|Creates a PO with the provided details.|
|Create Vendor|Creates a vendor with the provided details.|
|Get Ship To Location By Ship To ID|Retrieves all the ship to locations details, based on the input Ship to ID.|
|Get Supplier By Vendor ID|Retrieves the supplier details based on the input Vendor ID.|
|Lookup Fixed Assets|Retrieves details of all the fixed assets, based on the input criteria.|
|Lookup Advance Shipment Receipts|Retrieves details of the advance shipment receipts, based on the input criteria.|
|Lookup Bid Event|Retrieves details of all the bid events, based on the input criteria.|
|Lookup PO Header|Retrieves details of the PO header, based on the input criteria.|
|Lookup PO Line|Retrieves details of the PO line, based on the input criteria.|
|Lookup Ship To Locations|Retrieves list of all the ship to locations, based on the input criteria.|
|Lookup Suppliers|Retrieves details of all the suppliers, based on the input criteria.|
|Update PO|Updates details of the PO.|
|Utility|||
|Process Trigger|Triggers the specified process.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle Peoplesoft Financial spoke](../task/setup-pplsoftfin-spoke.md).

## MID Server requirements

To use these actions, your instance must have a MID Server set up and configured to use SOAP. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md). For more information about the MID Server, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

