---
title: SAP S4 HANA OData spoke
description: The SAP S4 HANA OData spoke is built by Bristlecone, Inc. Manage items, journals, procurements, and transactions in the SAP S4 HANA OData account from your ServiceNow instance.Also reuse this short description in the release notes.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 7
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SAP S4 HANA OData spoke

The SAP S4 HANA OData spoke is built by Bristlecone, Inc. Manage items, journals, procurements, and transactions in the SAP S4 HANA OData account from your ServiceNow® instance.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP S4 HANA OData spoke v1.11.0 is the latest version.

## Supported versions

This spoke was tested with SAP S/4HANA version 2023.

## Spoke requirements

-   SAP S4 HANA OData account
-   Configure the value of this system property:

    **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: This property serializes JSON objects and ensures that the data is in the required format. Specify the number of bytes as per your requirement. For more information, see [Workflow Studio system properties](https://www.servicenow.com/docs/access?context=flow-designer-system-properties&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Scheduled jobs

The SAP S4 HANA OData spoke is shipped with the **Generate Token and Cookie** scheduled job.

**Generate Token and Cookie**: This scheduled job is run every 26 minutes, which creates a token and cookie.

**Note:** The Fetch Token action depends on this scheduled job.

## Spoke actions

The SAP S4 HANA OData spoke provides actions to automate SAP S4 HANA OData tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_sqf_bdx_gzb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Contract Management

</td><td>

Create Contract

</td><td>

Creates a new purchase contract in SAP S4 HANA with one or more items. Validates the payload before submission.

</td></tr><tr><td>

Look up Contracts Stream

</td><td>

Retrieves details of all items across purchase contracts from SAP S4 HANA.

</td></tr><tr><td rowspan="2">

Sourcing Management

</td><td>

Create Sourcing Request

</td><td>

Creates a request for quotation in SAP S4 HANA by setting header details.

</td></tr><tr><td>

Look up Sourcing Requests Stream

</td><td>

Retrieves the header details of all the requests for quotations from SAP S4 HANA.

</td></tr><tr><td rowspan="2">

Catalog Management

</td><td>

Create Material

</td><td>

Creates a material record in SAP S4 HANA by setting the required header details.

</td></tr><tr><td>

Delete Material

</td><td>

Deletes the material record for the specified product number from SAP S4 HANA.

</td></tr><tr><td rowspan="15">

Primary Data Management

</td><td>

Look up Company Codes Stream​

</td><td>

Retrieves details of all the available company codes.​

</td></tr><tr><td>

Look up Currencies Stream​

</td><td>

Retrieves details of all the available currencies.

</td></tr><tr><td>

Look up Business Partners Stream

</td><td>

Retrieves business partner's data fields of all the available records in the system.

</td></tr><tr><td>

Look up FX Rates Stream​

</td><td>

Retrieves details of all the currency foreign exchange rates.​

</td></tr><tr><td>

Look up Cost Centers Stream​

</td><td>

Retrieve details of all the cost centers.​

</td></tr><tr><td>

Look up GL Accounts in Chart of Accounts Stream​

</td><td>

Retrieves the details of all general ledger accounts available in your system.​

</td></tr><tr><td>

Look up Chart of Accounts Stream​

</td><td>

Retrieves details of the available charts of accounts.

</td></tr><tr><td>

Look Up Plant Addresses Stream​

</td><td>

Retrieves details of the specified plant address master.​

</td></tr><tr><td>

Look up Purchasing Organizations Stream​

</td><td>

Retrieves details of all the purchasing organizations.​

</td></tr><tr><td>

Look up Payment Terms Stream​

</td><td>

Retrieves all the details of the payment terms.​

</td></tr><tr><td>

Look up Purchase Group Stream​

</td><td>

Retrieves details of the specified purchasing group master.

</td></tr><tr><td>

Look up Material Groups Stream

</td><td>

Retrieves the materials groups stream synchronously.

</td></tr><tr><td>

Look up Base Unit of Measure Stream

</td><td>

Retrieves the list of entries from unit of measure text.

</td></tr><tr><td>

Look up Business Partner Addresses Stream​

</td><td>

Retrieves business partner address data fields of all the available records in your SAP S4 HANA OData account.

</td></tr><tr><td>

Look up Materials Stream​

</td><td>

Retrieves details of all general data of product master.

</td></tr><tr><td rowspan="2">

Utility Management

</td><td>

Look up Last Run Date

</td><td>

Retrieves the last run date and time of the flow.

</td></tr><tr><td>

Fetch Token​

</td><td>

Retrieves the CSRF \(Cross-Site Request Forgery\) token and cookie for other spoke actions.**Note:** This action is run every 6 hours through the Generate Token and Cookie scheduled job and update the system properties.

</td></tr><tr><td rowspan="10">

Purchase Order Management

</td><td>

Update Purchase Order Line

</td><td>

Updates the item details of an item in a purchase order using the Purchase Order Number and Purchase Order Item.

</td></tr><tr><td>

Update Purchase Order for ASN

</td><td>

Updates the item details in a purchase order.

</td></tr><tr><td>

Update Purchase Order

</td><td>

Updates the header details for the specified purchase order number.

</td></tr><tr><td>

Look up Purchase Orders Stream

</td><td>

Retrieves general details of the specified product master.

</td></tr><tr><td>

Create Non Purchase Order Invoice

</td><td>

Creates a supplier invoice using, for example, the company code, the invoice gross amount, and the invoicing party.

</td></tr><tr><td>

Cancel Purchase Order Line

</td><td>

Deletes an item in a purchase order for the specified purchase order number and item number.

</td></tr><tr><td>

Create Purchase Order

</td><td>

Creates a purchase order with the specified details.

</td></tr><tr><td>

Create Line Item on Existing Purchase Order

</td><td>

Creates a line item in the existing purchase order with the header and item details passed in the request body.

</td></tr><tr><td>

Look up Purchase orders Stream

</td><td>

Retrieves details of all purchase orders and the related items.

</td></tr><tr><td>

Look up Purchase order Line Items Stream

</td><td>

Retrieves details of all purchase order line items.

</td></tr><tr><td rowspan="3">

Payment Management

</td><td>

Authorize Payment

</td><td>

Removes payment blocks that are set at the time of document creation.

</td></tr><tr><td>

Look up Payment Term

</td><td>

Retrieves details of the payment terms.

</td></tr><tr><td>

Look up Payments and Payment Status Stream

</td><td>

Retrieves payment information such as transaction currency, customer, payment status, accounting document and posting date.

</td></tr><tr><td rowspan="5">

Receipt Management

</td><td>

Create Service Goods Receipt

</td><td>

Creates service goods receipt in SAP S4 HANA OData.

</td></tr><tr><td>

Cancel Goods Receipt

</td><td>

Cancels the material document for the specified material document number and material document year.

</td></tr><tr><td>

Create Goods Receipt

</td><td>

Creates a material document compost by header and item for a specific business process.

</td></tr><tr><td>

Create Receipt for Advance Shipment Notification

</td><td>

Creates a material document with a header and item for a business process.

</td></tr><tr><td>

Look up Receipt

</td><td>

Retrieves the receipt details for the specified material document and other material document details.

</td></tr><tr><td rowspan="3">

Invoice Management

</td><td>

Create Invoice

</td><td>

Creates a supplier invoice based on the specified details, such as, company code, invoice gross amount, and invoicing party

</td></tr><tr><td>

Cancel Invoice

</td><td>

Delete a supplier invoice that hasn't been posted using the supplier invoice and the fiscal year.

</td></tr><tr><td>

Look up Invoices Stream

</td><td>

Retrieves general data of supplier master.

</td></tr><tr><td rowspan="3">

Shipment Management

</td><td>

Create Advance Shipment Notification

</td><td>

Creates an inbound delivery based on the specified purchase order.

</td></tr><tr><td>

Look up Advance Shipment Notification

</td><td>

Retrieves the advance shipment notification details for the specified delivery document number.

</td></tr><tr><td>

Look up Ship-to-Plant Addresses Stream

</td><td>

Retrieves the plant address details.

</td></tr><tr><td rowspan="12">

Supplier Management

</td><td>

Create Supplier

</td><td>

Creates a supplier.

</td></tr><tr><td>

Delete Supplier Bank Account

</td><td>

Deletes the bank data for the specified business partner number and bank identification number.

</td></tr><tr><td>

Look up Suppliers Stream​

</td><td>

Retrieves details of the specified supplier master.

</td></tr><tr><td>

Update Business Partner Address

</td><td>

Updates business partner address data of the record identified by address ID and business partner number.

</td></tr><tr><td>

Update Supplier Company

</td><td>

Updates the supplier company data by using the Supplier and Company Code fields.

</td></tr><tr><td>

Update Business Partner Bank

</td><td>

Updates bank data of the business partner record identified by business partner number and bank identification.

</td></tr><tr><td>

Update Supplier​

</td><td>

Updates the details of the specified supplier.

</td></tr><tr><td>

Update Supplier Fax Number

</td><td>

Updates the fax number by using Address ID.

</td></tr><tr><td>

Update Supplier Email Address

</td><td>

Updates email address by using Address ID.

</td></tr><tr><td>

Update Supplier Phone Number

</td><td>

Updates business partner mobile or telephone address data of the record identified by Address ID.

</td></tr><tr><td>

Create Company Code for Existing Supplier

</td><td>

Creates a company code for an existing supplier.

</td></tr><tr><td>

Create Bank Details for Existing Supplier

</td><td>

Creates new business partner bank data linked to business partner.

</td></tr></tbody>
</table>## Spoke module

The SAP S4 HANA OData spoke adds a SAP S4 HANA OData module to your ServiceNow instance.

|Module|Description|
|------|-----------|
|**Remote Table** &gt; **Purchase Orders**|Retrieves all the existing purchase orders in SAP S4 HANA OData.|
|**Inbound flow** &gt; **Purchase Orders**|Lists the most recent changes in purchase order status between the most recent successful runtime and the present runtime.|
|**Inbound flow** &gt; **Last Successful Execution**|Lists the last successful execution details of the flows.|

## Spoke flow

The SAP S4 HANA OData spoke adds the following flow.

|Flow|Description|
|----|-----------|
|Sample Look up Purchase Orders Flow|Retrieves the list of most recent changes in purchase order status between the most recent successful runtime and the present runtime.|

## Spoke subflow

The SAP S4 HANA OData spoke adds the following subflow.

|Subflow|Description|
|-------|-----------|
|Sample Create Purchase Order Subflow|Searches if a purchase order exists and creates a purchase order when no results are found.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

