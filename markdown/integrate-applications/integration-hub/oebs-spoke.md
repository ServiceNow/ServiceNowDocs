---
title: Oracle EBS Spoke
description: Manage sales orders, procurement, finance, customers, ledgers, and so on, in the Oracle EBS instance from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle EBS Spoke

Manage sales orders, procurement, finance, customers, ledgers, and so on, in the Oracle EBS instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** The packages should be redeployed when you are upgrading to the Oracle EBS spoke v1.1 from Oracle EBS spoke v1. For more information, see [Set up the Oracle EBS spoke](../task/setup-oebs-spoke.md#).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle EBS spoke v1.13.4 is the latest version.

## Supported versions

This spoke was built for these versions, but may be compatible with later versions.

-   Operating system version: Red Hat Enterprise Linux release 8.9 \(Ootpa\)
-   Oracle database version: 12.1.0.2.0
-   Oracle E-Business Suite application tier version: 12.2.12
-   Oracle WebLogic Server version: 10.3.6.0.171017 PSU
-   Oracle WebTier version: 11.1.1.9
-   Oracle Forms and Reports: 10.1.2.3

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Oracle EBS spoke provides a sample flow, Look up Daily Rates to demonstrate automating tasks. The flow runs daily and retrieves the Daily Currency Exchange Rates from Oracle EBS for the current date and saves the details in your ServiceNow instance.

## Spoke subflows

The Oracle EBS spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|AP Invoices - Create Interface Entries|Creates interface entries of AP Invoices in Oracle EBS.|
|AP Invoices - Get Processing Details|Retrieves the concurrent program status and other details from Oracle EBS.|
|Fetch AP invoice details|Retrieves the AP invoice details from Oracle EBS.|
|Fixed Assets - Create Interface Entries|Creates interface entries of fixed assets in Oracle EBS.|
|Fixed Assets - Get Processing Details|Retrieves the concurrent program status and other details from Oracle EBS.|
|Get Journal Posted Status|Retrieves the current status of a GL journal header.|
|Goods Receipts - Create Interface Entries|Creates interface entries of Goods Receipts in Oracle EBS.|
|Goods Receipts - Get Processing Details|Retrieves the concurrent program status and other details from Oracle EBS.|
|Purchase Orders - Create Interface Entries|Creates interface entries of purchase orders in Oracle EBS.|
|Purchase Orders - Get Processing Details|Retrieves the concurrent program status and other details from Oracle EBS.|

## Spoke actions

The Oracle EBS spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_jlv_4bn_mpb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Approval Management

</td><td>

Approve or Reject Approval Request

</td><td>

Approves or rejects the specified approval request in Oracle EBS.

</td></tr><tr><td>

Cancel Approval

</td><td>

Cancels the specified approval request in Oracle EBS.

</td></tr><tr><td rowspan="10">

Finance

</td><td>

Create AP Invoice - Run Concurrent Program

</td><td>

Runs the concurrent program that imports invoice data from the interface table to the base table of Oracle EBS.

</td></tr><tr><td>

Get AP Invoice

</td><td>

Retrieves details of the required AP invoice.

</td></tr><tr><td>

Get Fixed Asset

</td><td>

Retrieves details of the required fixed asset.

</td></tr><tr><td>

Get Vendor

</td><td>

Retrieves details of the required vendor.

</td></tr><tr><td>

Get Vendor Site

</td><td>

Retrieves details of the required vendor site.

</td></tr><tr><td>

Import Fixed Asset - Run Concurrent Program

</td><td>

Runs the concurrent program that imports the fixed asset data from the interface table to base table of Oracle EBS.

</td></tr><tr><td>

Look up AR Invoices

</td><td>

Retrieves details of the AR invoices.

</td></tr><tr><td>

Look up Daily Rate

</td><td>

Retrieves details of the specified daily rate based on the input criteria.

</td></tr><tr><td>

Look up Legal Entity

</td><td>

Retrieves details of a the required legal entity.

</td></tr><tr><td>

Look up Ship To Locations

</td><td>

Retrieves details of the required shipped locations based on the input criteria.

</td></tr><tr><td rowspan="2">

Inventory Management

</td><td>

Submit Inventory - Run Concurrent Program

</td><td>

Submits an inventory item CC program.

</td></tr><tr><td>

Update Inventory Items

</td><td>

Updates details of the inventory items.

</td></tr><tr><td rowspan="7">

Invoice Management

</td><td>

Authorize Payment - Apply Hold

</td><td>

Applies hold on the specified authorized payment invoices in Oracle EBS.

</td></tr><tr><td>

Authorize Payment - Release Hold

</td><td>

Releases hold on the specified authorized payment invoices in Oracle EBS.

</td></tr><tr><td>

Cancel Invoice

</td><td>

Cancels an invoice in Oracle EBS.

</td></tr><tr><td>

Create AP Invoice

</td><td>

Creates an Accounts Payable \(AP\) invoice in Oracle EBS. **Note:** The internal name of the latest version of the action is create\_ap\_invoice\_v3. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Look up AP Invoices

</td><td>

Retrieves an Accounts Payable \(AP\) invoice details from Oracle EBS.

</td></tr><tr><td>

Look up Invoice Payment Status

</td><td>

Retrieves the invoice payment status from Oracle EBS.

</td></tr><tr><td>

Submit Invoice - Run Concurrent Program

</td><td>

Submits an invoice - run concurrent program in Oracle EBS.

</td></tr><tr><td rowspan="14">

Journal Ledger

</td><td>

Create Journals

</td><td>

Creates a journal.

</td></tr><tr><td>

Get GL Journal Batch

</td><td>

Retrieves details of the required GL journal batch.

</td></tr><tr><td>

Get GL Journal Header

</td><td>

Retrieves details of the required GL journal header.

</td></tr><tr><td>

Get GL Ledger

</td><td>

Retrieves details of the required GL ledger.

</td></tr><tr><td>

Get GL Subledger Account

</td><td>

Retrieves details of the required GL subledger account.

</td></tr><tr><td>

Import Journals - Run Concurrent Program

</td><td>

Runs the concurrent program that imports journals data from the interface table to the base table of Oracle EBS.

</td></tr><tr><td>

Look up GL Balance

</td><td>

Retrieves details of the required GL balance based on the input criteria.

</td></tr><tr><td>

Look up GL Balances

</td><td>

Retrieves details of the required GL balance based on the input query.

</td></tr><tr><td>

Look up GL Code Combinations

</td><td>

Retrieves details of the required GL code combinations based on the input query.

</td></tr><tr><td>

Look up GL Journals

</td><td>

Retrieves details of the required GL journals based on the input criteria.

</td></tr><tr><td>

Look up GL Ledgers

</td><td>

Retrieves details of the required GL ledgers based on the input criteria.

</td></tr><tr><td>

Look up GL Subledger Accounts

</td><td>

Retrieves details of the required GL subledger accounts based on the input criteria.

</td></tr><tr><td>

Post Journals - Run Concurrent Program

</td><td>

Runs the concurrent program that posts the unposted journals.

</td></tr><tr><td>

Reverse Journals - Run Concurrent Program

</td><td>

Runs the concurrent program that reverses the posted journals.

</td></tr><tr><td rowspan="4">

Master

</td><td>

Create Item

</td><td>

Creates an item.

</td></tr><tr><td>

Look up Cost Center

</td><td>

Retrieves details about the required cost center.

</td></tr><tr><td>

Look up Item

</td><td>

Retrieves details about the required item.

</td></tr><tr><td>

Look up Item Category

</td><td>

Retrieves details about the required item category.

</td></tr><tr><td rowspan="7">

Utility Actions

</td><td>

Generate Input Payload With Crossreference

</td><td>

Generates array type input payload for Create Actions from subflow input payload while assigning configured cross-reference field with the ServiceNow ID\(s\).

</td></tr><tr><td>

Get Additional EBS Fields

</td><td>

Retrieves list of fields which can be further used as a dynamic template or dynamic object, based on an input string, Action Internal Name.

</td></tr><tr><td>

Get Records

</td><td>

Retrieves data from any Oracle EBS module using an SQL query.

</td></tr><tr><td>

Look up Common Object Details

</td><td>

Retrieves the common details of the object specified.

</td></tr><tr><td>

Look up Concurrent Program Status

</td><td>

Retrieves the status of a concurrent request.

</td></tr><tr><td>

Parse OEBS Record Details

</td><td>

Converts the JSON output of 'Get Records' Action into structured Object format.

</td></tr><tr><td>

Wait for Request Completion

</td><td>

Waits until the status of the request completes.

</td></tr><tr><td rowspan="2">

Transfer Order Management

</td><td>

Create Transfer Order

</td><td>

Creates a transfer order with the specified details.

</td></tr><tr><td>

Look up Transfer Orders

</td><td>

Retrieves details of the required transfer orders.

</td></tr><tr><td rowspan="3">

Procurement

</td><td>

Create Goods Receipts

</td><td>

Creates a goods receipt.

</td></tr><tr><td>

Get Advance Shipment Notice

</td><td>

Retrieves details of the required advance shipment notice.

</td></tr><tr><td>

Look up Advance Shipment Notices

</td><td>

Retrieves details of multiple advance shipment notices based on the input query.

</td></tr><tr><td rowspan="3">

Asset Management

</td><td>

Create Asset

</td><td>

Creates an asset with the specified details.

</td></tr><tr><td>

Look up Asset Categories Stream

</td><td>

Retrieves the details of the look up asset categories.

</td></tr><tr><td>

Submit Asset - Run Concurrent Program

</td><td>

Returns the concurrent status of the specified asset in Oracle EBS.

</td></tr><tr><td rowspan="4">

Bills and Payments

</td><td>

Look up Bill Details

</td><td>

Retrieves details of the required bills.

</td></tr><tr><td>

Look up Outstanding Balances

</td><td>

Retrieves details of the required outstanding balances.

</td></tr><tr><td>

Look up Payment Details

</td><td>

Retrieves details of the required payments.

</td></tr><tr><td>

Look up Payment Status

</td><td>

Retrieves status of the required payments.

</td></tr><tr><td rowspan="9">

Customer

</td><td>

Create Customer Account

</td><td>

Creates a customer account.

</td></tr><tr><td>

Create Customer Account Role

</td><td>

Creates a customer account role.

</td></tr><tr><td>

Create Customer Contact

</td><td>

Creates a customer account contact.

</td></tr><tr><td>

Create Customer Relation

</td><td>

Creates a customer relation record.

</td></tr><tr><td>

Create Person

</td><td>

Creates a person record.

</td></tr><tr><td>

Look up Customer Accounts

</td><td>

Retrieves details of the required customer accounts.

</td></tr><tr><td>

Look up Customer Contacts

</td><td>

Retrieves the required customer contacts.

</td></tr><tr><td>

Update Customer Account

</td><td>

Updates details of the required customer account.

</td></tr><tr><td>

Update Customer Contact

</td><td>

Updates details of the required customer contact.

</td></tr><tr><td rowspan="2">

Sales Order

</td><td>

Look up Sales Order Status Stream

</td><td>

Retrieves status details of the required sales orders.

</td></tr><tr><td>

Look up Sales Order Stream

</td><td>

Retrieves details of the required sales orders.

</td></tr><tr><td rowspan="2">

Contract Management

</td><td>

Create Contract

</td><td>

Creates a contract in Oracle EBS.

</td></tr><tr><td>

Create Contract - Run Concurrent Program

</td><td>

Retrieves the concurrent status of contract in Oracle EBS.

</td></tr><tr><td rowspan="8">

Purchase Order Management

</td><td>

Cancel Purchase Order

</td><td>

Cancels the purchase order.

</td></tr><tr><td>

Create Blanket Release

</td><td>

Creates blanket release in Oracle EBS.**Note:** The internal name of the latest version of the action is create\_blanket\_release\_v2. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Create Blanket Release - Run Concurrent Program

</td><td>

Retrieves the concurrent status of blanket release in Oracle EBS.

</td></tr><tr><td>

Create Blanket Purchase Agreement

</td><td>

Creates a blanket purchase agreement.**Note:** The internal name of the latest version of the action is create\_blanket\_purchase\_agreement\_v2. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Create Purchase Order

</td><td>

Creates purchase orders in Oracle EBS.**Note:** The internal name of the latest version of the action is create\_purchase\_order\_v3. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Create Purchase Order - Run Concurrent Program

</td><td>

Runs the concurrent program that imports the purchase order data from the interface table to the base table of Oracle EBS.

</td></tr><tr><td>

Update Blanket Purchase Agreement

</td><td>

Updates the details of the specified blanket purchase agreement.**Note:** The internal name of the latest version of the action is update\_blanket\_purchase\_agreement\_v2. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Update Purchase Order

</td><td>

Updates the purchase order in Oracle EBS.**Note:** The internal name of the latest version of the action is update\_purchase\_order\_v3. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td rowspan="5">

Receipt Management

</td><td>

Cancel PO Goods Receipt

</td><td>

Cancels the purchase order \(PO\) goods receipt.**Note:** The internal name of the latest version of the action is create\_po\_goods\_receipt\_v2. To use it, you must install the latest version of the spoke from the ServiceNow store.

</td></tr><tr><td>

Create Goods Receipt - Run Concurrent Program

</td><td>

Creates a good receipt in concurrent program mode.

</td></tr><tr><td>

Create PO Goods Receipt

</td><td>

Creates a Purchase Order \(PO\) goods receipt in Oracle EBS.

</td></tr><tr><td>

Look up PO Receipts

</td><td>

Retrieves purchase order \(PO\) receipts from Oracle EBS.

</td></tr><tr><td>

Update PO Goods Receipt

</td><td>

Updates a Purchase Order \(PO\) goods receipt in Oracle EBS.

</td></tr><tr><td rowspan="12">

Supplier Management

</td><td>

Create Bank Account

</td><td>

Creates a bank account.

</td></tr><tr><td>

Create Supplier

</td><td>

Creates a supplier in Oracle EBS.

</td></tr><tr><td>

Create Supplier Site

</td><td>

Creates a supplier site in Oracle EBS.

</td></tr><tr><td>

Deactivate Supplier

</td><td>

Deactivates the specified supplier in Oracle EBS.

</td></tr><tr><td>

Deactivate Supplier Site

</td><td>

Deactivates the specified supplier site in Oracle EBS.

</td></tr><tr><td>

Look up Bank Accounts Stream

</td><td>

Retrieves the supplier bank account details.

</td></tr><tr><td>

Look up Supplier Sites Stream

</td><td>

Retrieves the supplier site details from Oracle EBS.

</td></tr><tr><td>

Look up Suppliers Stream

</td><td>

Retrieves the supplier details from Oracle EBS.

</td></tr><tr><td>

Update Bank Account

</td><td>

Updates the specified bank account in Oracle EBS.

</td></tr><tr><td>

Update Supplier

</td><td>

Updates the specified supplier details in Oracle EBS.

</td></tr><tr><td>

Update Supplier Site

</td><td>

Updates the specified supplier site details in Oracle EBS.

</td></tr><tr><td>

Void Supplier Bank Account

</td><td>

Makes the supplier bank account as void.

</td></tr><tr><td rowspan="14">

Primary Data Management

</td><td>

Look up Attachments

</td><td>

Retrieves the file attachments related to purchase order, supplier, and other specified details from Oracle EBS.

</td></tr><tr><td>

Look up Currencies

</td><td>

Retrieves currency details from Oracle EBS.

</td></tr><tr><td>

Look up GL Accounts Stream

</td><td>

Retrieves GL account details from Oracle EBS.

</td></tr><tr><td>

Look up GL Cost Centers Stream

</td><td>

Retrieves the cost center details from Oracle EBS.

</td></tr><tr><td>

Look up GL Daily Rates

</td><td>

Retrieves GL Daily Rate details from Oracle EBS.

</td></tr><tr><td>

Look up GL Ledgers

</td><td>

Retrieves Ledger details from Oracle EBS.

</td></tr><tr><td>

Look up GL Legal Entities

</td><td>

Retrieves GL Legal Entity details from Oracle EBS.

</td></tr><tr><td>

Look up HR Locations Stream

</td><td>

Retrieves the details of HR locations from Oracle EBS.

</td></tr><tr><td>

Look up Inventory Items Stream

</td><td>

Retrieves the inventory item details from Oracle EBS.

</td></tr><tr><td>

Look up Item Categories Stream

</td><td>

Retrieves the item category details from Oracle EBS.

</td></tr><tr><td>

Look up Operating Units

</td><td>

Retrieves Operating Unit details from Oracle EBS.

</td></tr><tr><td>

Look up Payment Terms

</td><td>

Retrieves payment term details.

</td></tr><tr><td>

Look up Purchase Groups

</td><td>

Retrieves Purchasing Group details from Oracle EBS.

</td></tr><tr><td>

Look up Purchasing Organizations

</td><td>

Retrieves Purchasing Organization details from Oracle EBS.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Oracle EBS spoke](../task/setup-oebs-spoke.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the Oracle EBS alias to configure where actions run as well as set MID Server selection attributes. For more information about running actions on the MID Server, see [Integration steps](../../integrationhub/concept/integration-steps.md).

**Note:** If your Oracle EBS instance is only accessible on a private network, you must use MID Server.

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

