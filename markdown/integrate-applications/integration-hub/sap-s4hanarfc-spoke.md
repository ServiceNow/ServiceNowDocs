---
title: SAP S4 HANA RFC Spoke
description: The SAP S4 HANA RFC spoke is built by Bristlecone, Inc. Manage procurement, records, journals, and others, in SAP S4 HANA RFC account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP S4 HANA RFC Spoke

The SAP S4 HANA RFC spoke is built by Bristlecone, Inc. Manage procurement, records, journals, and others, in SAP S4 HANA RFC account from your ServiceNow® instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP S4 HANA RFC spoke v2.6.1 is the latest version.

## Supported versions

This spoke was built for SAP S4 HANA RFC 2023.

## Spoke requirements

-   Contact the admin of your SAP S4 HANA RFC account and obtain these SAP proprietary JAR files and other required files:

    -   `sapjco3.jar`.
    -   `libsapjco3.so`: If your MID Server is installed on a Linux machine, obtain this file.
    -   `sapjco3.dll`: If your MID Server is installed on a Windows machine, obtain this file.
    A JAR file, `sapConnector-1.0.jar`, is available along with the spoke to provide custom interface to interact and execute RFCs and IDocs in the SAP S4 HANA RFC account. The JAR file is installed as part of the spoke in your ServiceNow instance.

-   Copy and record the client value of the target host where the SAP S4 HANA RFC server is installed.
-   Configure the values of these system properties:
    -   **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: This property serializes JSON objects and ensures that the data is in the required format. Specify the number of bytes as per your requirement. For more information, see [Workflow Studio system\\n properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/flow-designer-system-properties.md).
    -   **glide.rest.max\_content\_length**: This property specifies the payload size. Specify the maximum payload size you want to use in your flows. The maximum value you can specify for this property is, 25 MB.
-   If you are using this spoke along with the SAP ECC IDoc, SAP S4 HANA IDoc, SAP ECC RFC spokes, during spoke upgrades, ensure that you upgrade all the spokes to their latest versions.

**Note:** To retrieve information for authorization purposes, use the Execute RFC spoke action.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SAP S/4 HANA RFC spoke provides sample flows to demonstrate automating the SAP S4 HANA RFC tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Retrieve Incoming Invoice|Retrieves the invoice data periodically. This data is displayed in the SAP S/4HANA Invoice Data module.|
|Retrieve Users by Role|Retrieves details of the users, based on the provided user role. This data is displayed in the SAP S/4HANA Users Records module.|

## Spoke actions

The SAP S/4 HANA RFC spoke provides actions to automate SAP S4 HANA RFC tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Items|Look up Material Groups|Retrieves details of the material groups.|
|Look up Materials by Plant|Retrieves details of the materials \(items\) based on plant selection criteria.|
|Look up Materials by Storage Locations|Retrieves details of the materials \(items\) based on storage location selection criteria.|
|Journals|Post Journal Entry|Posts a journal entry to a GL Account in SAP S4 HANA RFC.|
|Reverse Journal Entry|Reverses a journal entry in a GL Account in SAP S4 HANA RFC.|
|Lookups|Look up Cost Centers by Controlling Area|Retrieves details of the cost centers based on the controlling area.|
|Metadata Retrieval|Get RFC Input Schema|Dynamically retrieves the input schema for the RFC.|
|Get RFC Output Schema|Dynamically retrieves the output schema for the RFC.|
|Look up RFC Table Field Input Metadata|Dynamically retrieves the input schema from SAP S4 HANA RFC for the selected field in the RFC tables.|
|Look up RFC Table Field Output Metadata|Dynamically retrieves the output schema from SAP S4 HANA RFC for the selected field in the RFC tables.|
|Look up RFC Tables Input Metadata|Dynamically retrieves the tables input schema for the RFC from SAP S4 HANA RFC.|
|Procurement|Authorize Payment|Creates an authorize payment document in SAP S/4 HANA - RFC.|
|Create Fixed Asset|Creates a fixed asset in SAP S4 HANA RFC.|
|Create Goods Receipt|Creates a goods receipt document in SAP S4 HANA RFC.|
|Create Invoice|Creates an invoice document in SAP S4 HANA RFC.|
|Cancel Invoice|Cancels an invoice document in SAP S/4HANA RFC.|
|Cancel Goods Receipt|Cancels a goods receipt document in SAP S/4HANA - RFC.|
|Create Non Purchase Order Invoice|Creates a non purchase order invoice document in SAP S4 HANA – RFC.|
|Create Purchase Order|Creates a purchase order in SAP S4 HANA RFC.|
|Create Service Goods Receipt|Creates a service goods receipt document in SAP S/4HANA - RFC.|
|Create Vendor|Creates a vendor in SAP S/4HANA - RFC.|
|Look up Asset Category|Retrieves details about the specified asset from SAP S/4HANA - RFC.|
|Look up Invoices|Retrieves details of the invoices from SAP S/4 HANA - RFC.|
|Look up Purchase Order Attachments|Retrieves details of the Purchase Order attachment from SAP S/4HANA RFC.|
|Look up Invoices by Date|Retrieves details of the invoices based on entry date.|
|Look up Purchase Orders and Purchase Order Lines|Retrieves details of the Purchase Orders and Purchase Order Lines from SAP S/4 HANA - RFC.|
|Look up Receipts|Retrieves details of the receipts from SAP S/4HANA RFC.|
|Look up Vendors|Retrieves vendors details from SAP S/4HANA - RFC.|
|Look up Advance Shipment Notices|Retrieves Advance Shipment Notices in SAP S/4HANA - RFC.|
|Look up Payment Status for Invoice|Retrieves the payment status for invoice from SAP S/4HANA - RFC.|
|Update Purchase Order|Updates details of the specified purchase order.|
|Update Vendor|Updates details of a vendor in SAP S/4HANA - RFC.|
|Records Management|Execute RFC|Executes an RFC from the available list for create, update, or read operation.|
|Execute RFC For Look up Operations|Executes an RFC from the available list.|
|Transfer Order|Create Transfer Order and Line Items|Creates a transfer order in SAP S/4HANA - RFC.|
|Look up Transfer Order and Line Items|Retrieves transfer orders from SAP S/4HANA - RFC.|
|Utility|Create Table Field Metadata|Envelops user inputs for the selected table field of the given BAPI in an object.|
|Finance Management|Create Asset|Create an asset in SAP S4 HANA - RFC with the provided details.|
|Sales Order|Create Sales Order|Creates a sales order in SAP S/4HANA - RFC.|
|Look up Sales Order|Retrieves sales order details from SAP S/4HANA - RFC.|
|Look up Sales Orders|Retrieves sales orders based on given customer number from SAP S/4HANA - RFC.|
|Update Sales Order|Updates details of the given sales order in SAP S/4HANA - RFC.|
|Bills and Payments|Look up Bill Details By ID|Retrieves bill details for the given document ID from SAP S/4HANA - RFC.|
|Look up Outstanding Balance|Retrieves outstanding balance of a customer from SAP S/4HANA - RFC.|
|Look up Payments|Retrieves pending payments of the customer from SAP S/4HANA - RFC.|
|Customer Management|Look up Customer Information|Retrieves customer information for the given company code and customer number from SAP S/4HANA - RFC.|
|Inventory \(or\) Sales|Look up Inventory of Parts|Retrieves inventory for the given plant and material from SAP S/4HANA-RFC.|

## Spoke module

The SAP S/4 HANA RFC spoke adds the SAP S4 HANA RFC Spoke application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|SAP S/4 HANA - RFCs|Displays the list RFCs. Some RFCs are provided along with spoke. You can create additional RFCs as per your requirement. The Execute RFC action uses these records as an input.|
|SAP S/4 HANA Flow Executions|Displays the dates on which the Retrieve Incoming Invoice flow is executed. After you set up the SAP S4 HANA RFC spoke, create a record to specify the date up to which you want to retrieve the invoice data. For more information, see [Set up the SAP S4 HANA RFC spoke](../task/setup-saphana-rfc.md).|
|SAP S/4 HANA Invoice Data|Displays details of the invoice data. Customize and execute the default flow, Retrieve Incoming Invoice to retrieve the invoice data.|
|SAP S/4 HANA Users Records|Displays details of the users, based on their user role. Customize and execute the default flow, Retrieve Users by Role to retrieve the user information.|

## Spoke user roles

The SAP S4 HANA RFC provides the sn\_sap\_s4\_hana\_rfc.SAP\_S4\_HANA\_RFC\_Spoke\_Admin user role to control access to data. Users with the sn\_sap\_s4\_hana\_rfc.SAP\_S4\_HANA\_RFC\_Spoke\_Admin role have access to the spoke tables.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

## MID Server requirements

These actions use Remote Function Call \(RFC\) protocol \(SAP Proprietary protocol – SAP Standard Interface\), which can run on an instance or MID Server. Use the connection record associated with SAP S4 HANA RFC spoke alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md)

**Note:**

-   If the MID Server is installed on a Linux machine, perform the configurations as outlined in [Set up the SAP S4 HANA RFC spoke](../task/setup-saphana-rfc.md).
-   If the MID Server is installed on a Windows machine, no configurations are needed.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

