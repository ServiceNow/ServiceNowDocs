---
title: SAP ECC RFC Spoke
description: The SAP ECC RFC spoke is built by Bristlecone, Inc. Manage items, journals, procurements, and others, in SAP ECC RFC account from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP ECC RFC Spoke

The SAP ECC RFC spoke is built by Bristlecone, Inc. Manage items, journals, procurements, and others, in SAP ECC RFC account from your ServiceNow® instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP ECC RFC spoke v2.9.4 is the latest version.

## Supported versions

This spoke was built for these SAP ECC RFC versions and the spoke is compatible with versions listed below:

-   SAP application version where spoke is developed: SAP EHP8 for ERP6.0
-   Compatible SAP application versions: SAP ECC6.0 Base pack until latest SAP EHP8 for ERP6.0
-   SAP JCo: 3.0.20 or later

## Spoke requirements

-   Contact the admin of your SAP ECC RFC account and obtain these SAP proprietary JAR files and other required files:

    -   `sapjco3.jar`.
    -   `libsapjco3.so`: If your MID Server is installed on a Linux machine, obtain this file.
    -   `sapjco3.dll`: If your MID Server is installed on a Windows machine, obtain this file.
    A JAR file, `sapConnector-1.0.1.jar` , is available along with the spoke to provide custom interface to interact and execute RFCs and IDocs in the SAP ECC RFC account. The JAR file is installed as part of the spoke in your ServiceNow instance.

-   Copy and record the client value of the target host where the SAP ECC RFC server is installed.
-   Configure the values of these system properties:
    -   **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: This property serializes JSON objects and ensures that the data is in the required format. Specify the number of bytes as per your requirement. For more information, see Workflow Studio system\\n properties.
    -   **glide.rest.max\_content\_length**: This property specifies the payload size. Specify the maximum payload size you want to use in your flows. The maximum value you can specify for this property is, 25 MB.
-   If you are using this spoke along with the SAP ECC IDoc, SAP S4 HANA IDoc, SAP S4 HANA RFC spokes, during spoke upgrades, ensure that you upgrade all the spokes to their latest versions.

    **Note:** If you are upgrading the spoke from an earlier version, make sure to restart the MID server.


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SAP ECC RFC spoke provides sample flows to demonstrate automating the SAP ECC RFC tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Retrieve Users By Role|Retrieves details of the SAP ECC RFC users with the specified role. The user details can be accessed by navigating to **SAP ECC RFC Spoke** &gt; **SAP ECC Users**.|
|Retrieve Incoming Invoice|Retrieves details of the incoming SAP ECC RFC invoices. The invoice details can be accessed by navigating to **SAP ECC RFC Spoke** &gt; **SAP ECC Invoices Data**.|
|Create Sales Order and Look up Status|Creates a sales order and retrieves the status information.|
|Create Cost Center|Demonstrates how to use the Execute RFC and Create Table Field Object actions.|

## Spoke actions

The SAP ECC RFC spoke provides actions to automate SAP ECC RFC tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_o3f_np4_xmb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Items

</td><td>

Look up Material Groups

</td><td>

Retrieves the list of material groups from your SAP ECC RFC account.

</td></tr><tr><td>

Look up Materials By Plant

</td><td>

Retrieves the list of materials \(items\) based on plant selection criteria.

</td></tr><tr><td>

Look up Materials by Storage Location

</td><td>

Retrieves the list of materials \(items\) based on the storage location selection criteria.

</td></tr><tr><td rowspan="2">

Journals

</td><td>

Post Journal Entry

</td><td>

Posts a journal entry to a GL account in your SAP ECC RFC account.

</td></tr><tr><td>

Reverse Journal Entry

</td><td>

Reverses a journal entry in a GL account in your SAP ECC RFC account.

</td></tr><tr><td>

Lookups

</td><td>

Look up Cost Centers by Controlling Area

</td><td>

Retrieves cost centers based on the controlling area from your SAP ECC RFC account.

</td></tr><tr><td rowspan="7">

Metadata Retrieval

</td><td>

Look up RFC Input Schema

</td><td>

Retrieves the input schema for the RFC, from SAP ECC RFC dynamically.

</td></tr><tr><td>

Look up RFC Output Schema

</td><td>

Retrieves the output schema from SAP ECC RFC dynamically, for the selected RFC.

</td></tr><tr><td>

Look up RFC Table Field Input Metadata

</td><td>

Dynamically retrieves the input schema from SAP ECC RFC, for the selected field in the RFC tables.

</td></tr><tr><td>

Look up RFC Table Field Output Metadata

</td><td>

Dynamically retrieves the output schema from SAP ECC RFC, for the selected field in the RFC tables.

</td></tr><tr><td>

Look up RFC Tables Input Metadata

</td><td>

Dynamically retrieves the tables input schema for the RFC, from SAP ECC RFC.

</td></tr><tr><td>

Look up RFC Input Metadata

</td><td>

Dynamically retrieves the input schema for the RFC, from SAP ECC – RFC.

</td></tr><tr><td>

Look up RFC Output Metadata

</td><td>

Dynamically retrieves the output schema from SAP ECC - RFC, for the selected RFC.

</td></tr><tr><td rowspan="21">

Procurement

</td><td>

Authorize Payment

</td><td>

Creates an authorize payment document in SAP ECC RFC.

</td></tr><tr><td>

Create Fixed Asset

</td><td>

Create a fixed asset in SAP ECC RFC.

</td></tr><tr><td>

Create Service Goods Receipt

</td><td>

Creates a Service goods receipt document in SAP ECC - RFC.

</td></tr><tr><td>

Create Goods Receipt

</td><td>

Creates a goods receipt document in SAP ECC RFC.

</td></tr><tr><td>

Create Invoice

</td><td>

Creates an invoice in SAP ECC RFC.

</td></tr><tr><td>

Cancel Invoice

</td><td>

Cancels an invoice document in SAP ECC - RFC.

</td></tr><tr><td>

Cancel Goods Receipt

</td><td>

Cancels a goods receipt document in SAP ECC - RFC.

</td></tr><tr><td>

Create Non Purchase Order Invoice

</td><td>

Creates a non purchase order invoice document in SAP ECC – RFC.

</td></tr><tr><td>

Create Purchase Order

</td><td>

Creates a purchase order in SAP ECC RFC.

</td></tr><tr><td>

Create Vendor

</td><td>

Creates a vendor in SAP ECC RFC.

</td></tr><tr><td>

Update Vendor

</td><td>

Updates details of a vendor in SAP ECC RFC.

</td></tr><tr><td>

Look up Asset Category

</td><td>

Retrieves details of the specified asset from SAP ECC - RFC.

</td></tr><tr><td>

Look up Invoices

</td><td>

Retrieves details of the specified invoice from SAP ECC - RFC.

</td></tr><tr><td>

Look up Invoices By Date

</td><td>

Retrieves invoices from SAP ECC RFC based on the provided date.

</td></tr><tr><td>

Look up Purchase Orders and Purchase Order Lines

</td><td>

Retrieves details of the purchase order and purchase order lines from SAP ECC - RFC.

</td></tr><tr><td>

Look up Purchase Order Attachments

</td><td>

Retrieves the details of the purchase order from SAP ECC - RFC.

</td></tr><tr><td>

Look up Receipts

</td><td>

Retrieves the details of the receipts from SAP ECC - RFC.

</td></tr><tr><td>

Look up Vendors

</td><td>

Retrieves vendors details from SAP ECC - RFC.

</td></tr><tr><td>

Look up Advance Shipment Notices

</td><td>

Retrieves details of the advance shipment notices in SAP ECC - RFC.

</td></tr><tr><td>

Look up Payment Status for Invoice

</td><td>

Retrieves the payment status for invoice from SAP ECC - RFC.

</td></tr><tr><td>

Update Purchase Order

</td><td>

Updates an existing purchase order in SAP ECC RFC

</td></tr><tr><td rowspan="2">

Records Management

</td><td>

Execute RFC

</td><td>

Executes an RFC from the available list for the create, update, or read operations.

</td></tr><tr><td>

Execute RFC for Look up Operations

</td><td>

Executes an RFC from the available list of read operations.

</td></tr><tr><td rowspan="3">

Bills and Payment

</td><td>

Look Up Bill Details By ID

</td><td>

Retrieves bills based on sales order from SAP ECC RFC.

</td></tr><tr><td>

Look Up Outstanding Balance

</td><td>

Retrieves outstanding balance of a customer from SAP ECC RFC.

</td></tr><tr><td>

Look Up Payments

</td><td>

Retrieves pending payments of the customer from SAP ECC RFC.

</td></tr><tr><td>

Customer

</td><td>

Look Up Customer Info

</td><td>

Retrieves customer information based on company code and customer from SAP ECC RFC.

</td></tr><tr><td rowspan="2">

Transfer Order

</td><td>

Create Transfer Order and Line Items

</td><td>

Creates a transfer order in SAP ECC - RFC.

</td></tr><tr><td>

Look up Transfer Order and Line Items

</td><td>

Retrieves transfer orders from SAP ECC - RFC.

</td></tr><tr><td>

Utility

</td><td>

Create Table Field Object

</td><td>

Envelops user inputs for the selected table field of given BAPI in an object.

</td></tr><tr><td>

Inventory \(or\) Sales

</td><td>

Look Up Inventory of Parts

</td><td>

Retrieves inventory for the plant and material from SAP ECC RFC.

</td></tr><tr><td>

Finance Management

</td><td>

Create Asset

</td><td>

Creates an asset in SAP ECC - RFC with the provided details.

</td></tr><tr><td rowspan="4">

Sales Order

</td><td>

Create Sales Order

</td><td>

Creates a sales order in SAP ECC RFC.

</td></tr><tr><td>

Look Up Sales Order

</td><td>

Retrieves sales order details from SAP ECC RFC.

</td></tr><tr><td>

Look Up Sales Orders

</td><td>

Retrieves sales orders based on customer from SAP ECC RFC.

</td></tr><tr><td>

Update Sales Order

</td><td>

Updates details of the required sales order in SAP ECC RFC.

</td></tr></tbody>
</table>## Spoke modules

The SAP ECC RFC spoke adds the SAP ECC RFC Spoke application to your instance and includes these modules:

<table id="table_q3f_np4_xmb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAP ECC Flow Executions

</td><td>

Displays the last successful execution date of the Retrieve Incoming Invoice flow.Before the first flow execution, you must create a record in this module to specify the date from which the incoming invoice details should be fetched.

</td></tr><tr><td>

SAP ECC Invoices Data

</td><td>

Displays the records retrieved by the Retrieve Incoming Invoice flow.

</td></tr><tr><td>

SAP ECC RFCs

</td><td>

Displays the list of BAPIs. The Execute RFC action and Execute RFC for Look up Operations actions uses this as input.**Note:** Value of Operation Type is used to specify the kind of operation BAPI is expected to do. If the operation is read, the operation will be available in both Execute RFC for Look up Operations and Execute RFC actions. If the operation is write, the operation is only available for Execute RFC action as input.

</td></tr><tr><td>

SAP ECC Users

</td><td>

Displays details of the SAP ECC RFC users. The Retrieve Users By Role flow retrieves details of the users with the specified role.

</td></tr></tbody>
</table>## Spoke user roles

The SAP ECC RFC spoke provides user roles to control access to data.

-   Users with the sn\_sap\_ecc\_rfc\_spo.SAP\_ECC\_RFC\_Spoke\_Admin role have access to the spoke tables.
-   Users with the sn\_sap\_ecc\_rfc\_spo.SAP\_ECC\_RFC\_Spoke\_Read role can view data in the SAP ECC RFCs table and module.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the SAP ECC RFC spoke](../task/setup-sap-ecc-rfc.md#).

## MID Server requirements

These actions use Remote Function Call \(RFC\) protocol \(SAP Proprietary protocol – SAP Standard Interface\), which can run on an instance or MID Server. Use the connection record associated with the SAP ECC RFC spoke alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md)

**Note:**

-   If the MID Server is installed on a Linux machine, perform the configurations as outlined in [Configure MID Server for the SAP ECC RFC spoke](../task/setup-sap-ecc-rfc.md#).
-   If the MID Server is installed on a Windows machine, no configurations are needed.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

