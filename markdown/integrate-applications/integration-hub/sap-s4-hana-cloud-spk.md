---
title: SAP S4 HANA Public Cloud Spoke
description: The SAP S4 HANA Public Cloud spoke is built by Bristlecone, Inc. Manage primary data, purchase orders, receipts, and suppliers in SAP S4 HANA public cloud instance from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# SAP S4 HANA Public Cloud Spoke

The SAP S4 HANA Public Cloud spoke is built by Bristlecone, Inc. Manage primary data, purchase orders, receipts, and suppliers in SAP S4 HANA public cloud instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SAP S4 HANA Public Cloud spoke v1.3 is the latest version.

## Supported versions

This spoke was built for SAP S4 HANA 2023.

## Spoke requirements

-   SAP S4 HANA Public Cloud account
-   Configure the value of this system property:

    **com.snc.process\_flow.reporting.serialized.val\_size\_limit**: This property serializes JSON objects and ensures that the data is in the required format. Specify the number of bytes as per your requirement. For more information, see [Workflow Studio system properties](https://www.servicenow.com/docs/access?context=flow-designer-system-properties&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The SAP S4HANA Public Cloud spoke provides actions to automate tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_vln_lbn_4bc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="9">

Primary Data Management

</td><td>

Look up Business Partner Addresses Stream

</td><td>

Retrieves business partner address data fields of all the available records in the system.

</td></tr><tr><td>

Look up Business Partners Stream

</td><td>

Retrieves business partner's data fields of all the available records in the system.

</td></tr><tr><td>

Look up Base Unit of Measure Stream

</td><td>

Reads a set of entries from the Unit of Measure text.

</td></tr><tr><td>

Look up Chart of Accounts Stream

</td><td>

Retrieves details of the available charts of accounts.

</td></tr><tr><td>

Look up Company Codes Stream

</td><td>

Retrieves the details related to Company Codes.

</td></tr><tr><td>

Look up Cost Centers Stream

</td><td>

Retrieve details of all cost centers.

</td></tr><tr><td>

Look up GL Accounts in Chart of Accounts Stream

</td><td>

Retrieves the details of the available General Ledger \(GL\) accounts for the chart of accounts.

</td></tr><tr><td>

Look up Material Groups Stream

</td><td>

Retrieves the materials groups stream synchronously.

</td></tr><tr><td>

Look up Materials Stream

</td><td>

Retrieves details of all general data of product master.

</td></tr><tr><td rowspan="2">

Purchase Order Management

</td><td>

Look up Purchase Orders Stream

</td><td>

Retrieves general data of the required product master.

</td></tr><tr><td>

Create Purchase Order and PO Lines

</td><td>

Creates a new purchase order with the header and item details passed in the request body.

</td></tr><tr><td rowspan="3">

Receipt Management

</td><td>

Create Receipt

</td><td>

Creates a material document by header and item for the specific business process.

</td></tr><tr><td>

Create Service Goods Receipt

</td><td>

Creates a service goods receipt in SAP S4 Hana Cloud.

</td></tr><tr><td>

Look up Receipts Stream

</td><td>

Retrieves details related to material documents.

</td></tr><tr><td rowspan="2">

Supplier Management

</td><td>

Create Supplier

</td><td>

Creates a new supplier with the provided details.

</td></tr><tr><td>

Look up Suppliers Stream

</td><td>

Retrieves general data of the supplier master.

</td></tr><tr><td rowspan="2">

Invoice Management

</td><td>

Create Invoice

</td><td>

Creates a supplier invoice using the company code, invoice gross amount, and invoicing party.

</td></tr><tr><td>

Look up Invoices Stream

</td><td>

Reads the supplier invoice data using, for example, the supplier invoice, the fiscal year, the company code, the document currency, the document date, the invoice gross amount, the invoicing party and the posting date.

</td></tr><tr><td>

Shipment Management

</td><td>

Look up Advance Shipment Notification Stream

</td><td>

Retrieves general data of the required advanced shipment notices.

</td></tr><tr><td>

Utility Management

</td><td>

Fetch Token and Cookie

</td><td>

Retrieves the CSRF \(Cross-Site Request Forgery\) token and cookie for other spoke actions.**Note:** This action runs every 6 hours through the Generate Token and Cookie scheduled job and updates the system properties.​

</td></tr><tr><td>

User Management

</td><td>

Look Up Users Stream

</td><td>

Retrieves the general data of the users present in the system. The data fetched are user ID, user name, description, email address, and so on.

</td></tr></tbody>
</table>## Spoke scheduled job

The SAP S4HANA Public Cloud spoke provides a scheduled job, Generate Token and Cookie - Cloud Spoke. This scheduled job is run every 26 minutes, which creates a token and cookie.​ The Fetch Token and Cookie spoke action depends on this scheduled job.​

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Setup the SAP S4 HANA Public Cloud spoke](../task/setup-sap-s4hana-cloud-spk.md).

