---
title: Workday Financials Spoke
description: The Workday Financials spoke is built by Bristlecone, Inc. Manage resources, business units, journals, cost centers, and so on, in Workday Financials application from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday Financials Spoke

The Workday Financials spoke is built by Bristlecone, Inc. Manage resources, business units, journals, cost centers, and so on, in Workday Financials application from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Workday Financials spoke v2.1.0 is the latest version.

## Supported versions

This spoke was built for Workday Financials SOAP API version v39.0, but may be compatible with later versions.

## Spoke requirements

To set up the integration, perform these:

1.  Register Integration System User.

    **Note:** While filling account information details, ensure that you select the **Do Not Allow UI Sessions** check box.

2.  Create a security group and assign it to the integration system user.
    1.  In **Action**, navigate to **Security Group** &gt; **Maintain Domain Permissions for Security Group** and provide these permissions:

        |Operation|Domain Security Policy|Domain Security Policies Inheriting Permission|Functional Areas|
        |---------|----------------------|----------------------------------------------|----------------|
        |Get Only|Set Up: Worktags - Business Units| |Common Financial Management Worktags|
        |Get Only|Set Up: Ledger and Book| |Common Financial Management|
        |Get and Put|Process: Journals - Core| |Financial Accounting|
        |Get Only|Process: Journals - View| |Financial Accounting|
        |Get and Put|Process: Purchase Order - Cancel| |Procurement|
        |Get Only|Process: Advance Ship Notice - View| |Procurement|
        |Get Only|Process: Supplier Invoice - New| |Supplier Accounts|
        |Get Only|Process: Request for Quotes - View| |Procurement|
        |Get Only|Set Up: Accounts| |Common Financial Management|
        |Get Only|Create: Cost Center| |Organizations and Roles|
        |Get Only|Set Up: Currency Rates| |Common Financial Management|
        |Get Only|Set Up: Currency \(Compensation functional area\)| |Core Compensation|
        |Get Only|Integration Build| |Integration|
        |Get Only|Process: Business Assets| |Business Asset Tracking|
        |Get Only|Set Up: Expense Item| |Expenses|
        |Get Only|Set Up: Purchase Item| |Procurement|
        |Get Only|Reports: Supplier| |Supplier|
        |View Only|Process: Purchase Order - Reporting| |Procurement|
        |Get and Put|Integration Event| |Integration|
        |View Only|Integration Security| |Integration|

        **Note:** Ensure that the domain security policies are activated for the security group.

    2.  Configure the business process policies of your security group and provide these permissions:

<table id="table_stn_smk_qmb"><thead><tr><th>

Operation

</th><th>

Business Process Type

</th><th>

Functional Area

</th></tr></thead><tbody><tr><td>

Initiate \(Register Asset \(Web Service\)\)

</td><td>

Asset Registration Event

</td><td>

-   Business Asset Accounting
-   Business Asset Tracking


</td></tr><tr><td>

Initiate \(Submit Purchase Order Change Order \(Web Service\)\)

</td><td>

Change Order

</td><td>

Procurement

</td></tr><tr><td>

Initiate \(Submit Purchase Order \(Web Service\)\)

</td><td>

Purchase Order Event

</td><td>

Procurement

</td></tr><tr><td>

Initiate \(Submit Receipt \(Web Service\)\)

</td><td>

Receipt

</td><td>

Procurement

</td></tr><tr><td>

Initiate \(Submit Supplier \(Web Service\)\)

</td><td>

Supplier Event

</td><td>

Supplier

</td></tr><tr><td>

Initiate \(Submit Supplier Invoice \(Web Service\)\)

</td><td>

Supplier Invoice Event

</td><td>

Supplier Accounts

</td></tr></tbody>
</table>        **Note:** Ensure that the business process security policies are activated for the security group.


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Authentication

Workday provides an open SOAP API for programmatic access to on-demand business management services. Workday SOAP APIs require basic authentication; that is, user name and password are required.

**Note:** This spokes doesn't require you to set up the connection and credential alias.

## Spoke subflows

The Workday Financials spoke provides sample subflows to demonstrate automating Workday Financials tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Create PO|Creates a purchase order record in the Purchase Order table. To use the subflow, [Set up webhook for your Workday Financials spoke](../task/setup-webhk-wd.md#).|
|Get Supplier Invoice Details|Retrieves details of the specified supplier invoice.|

## Spoke actions

The Workday Financials spoke provides actions to automate  tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_zrn_5xf_pmb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="4">

Approval Management

</td><td>

Approve Business Process

</td><td>

Approves the required business process.

</td></tr><tr><td>

Cancel Business Process

</td><td>

Cancels the required business process.

</td></tr><tr><td>

Deny Business Process

</td><td>

Denies the required business process.

</td></tr><tr><td>

Look up Approvals

</td><td>

Retrieves the approvals records from Workday and saves the details as an attachment in the Data Source table.**Note:** To use this action, you must create and configure the To Do RaaS report. For instructions, see [Configure the To Do report](../task/setup-workday-fin-spoke.md#).

</td></tr><tr><td rowspan="2">

Invoice Management

</td><td>

Void or cancel Invoice

</td><td>

Cancels the required supplier invoice.

</td></tr><tr><td>

Update Supplier Invoice

</td><td>

Updates details of the required supplier invoice.

</td></tr><tr><td rowspan="3">

Receipt Management

</td><td>

Void or Cancel Receipt

</td><td>

Cancels the required receipt.

</td></tr><tr><td>

Look up Goods Receipts Stream

</td><td>

Retrieves details of the required receipts.

</td></tr><tr><td>

Update Receipt

</td><td>

Updates details of the required receipt.

</td></tr><tr><td rowspan="3">

Requisition Management

</td><td>

Look up Requisitions Stream

</td><td>

Retrieves the requisition data.

</td></tr><tr><td>

Update Requisition

</td><td>

Updates details of the required requisition records.

</td></tr><tr><td>

Create Requisition

</td><td>

Creates requisition record with the provided details.

</td></tr><tr><td>

Purchase Order Management

</td><td>

Look up Purchase Orders and PO Lines Stream

</td><td>

Retrieves details of the required purchase orders and PO lines.

</td></tr><tr><td rowspan="3">

Primary Data Management

</td><td>

Look up Company Contact Information by ID

</td><td>

Retrieves details of the required company contact.

</td></tr><tr><td>

Look up Organizations Stream

</td><td>

Retrieves the organization data.

</td></tr><tr><td>

Look up Locations Stream

</td><td>

Retrieves details of the required locations.

</td></tr><tr><td rowspan="8">

Supplier Management

</td><td>

Look up Supplier Contracts Stream

</td><td>

Retrieves details of the supplier contracts.

</td></tr><tr><td>

Deactivate Supplier

</td><td>

Deactivates the required supplier.

</td></tr><tr><td>

Create Supplier Location

</td><td>

Creates a supplier location with the provided details.

</td></tr><tr><td>

Update Supplier Location

</td><td>

Updates details of the required supplier location.

</td></tr><tr><td>

Delete or Void Supplier Bank Account

</td><td>

Deletes the required supplier bank account or makes it void.

</td></tr><tr><td>

Create Bank Account

</td><td>

Creates a supplier bank account with the provided details.

</td></tr><tr><td>

Update Bank Account

</td><td>

Updates details of the required supplier bank account.

</td></tr><tr><td>

Update Supplier

</td><td>

Updates details of the required supplier.

</td></tr><tr><td rowspan="10">

Financial Management

</td><td>

Get Account Set By ID

</td><td>

Retrieves details of the specified account set.

</td></tr><tr><td>

Get Business Unit By ID

</td><td>

Retrieves details of the specified business unit.

</td></tr><tr><td>

Get Cost Center By ID

</td><td>

Retrieves details of the specified cost center.

</td></tr><tr><td>

Get Ledger By ID

</td><td>

Retrieves details of the specified ledger record.

</td></tr><tr><td>

Look up Account Sets

</td><td>

Retrieves details of the required account sets, based on the provided filter criteria.

</td></tr><tr><td>

Look up Business Units

</td><td>

Retrieves details of the required business units, based on the provided filter criteria.

</td></tr><tr><td>

Look up Cost Centers

</td><td>

Retrieves details of the required cost centers, based on the provided filter criteria.

</td></tr><tr><td>

Look up Fx Rates

</td><td>

Retrieves details of the required Fx rates, based on the provided filter criteria.

</td></tr><tr><td>

Look up Ledger Accounts

</td><td>

Retrieves the ledger accounts from Workday and saves the details as an attachment in the Data Source table.**Note:** To use this action, you must create and configure the Ledger Account RaaS report. For instructions, see [Configure the Ledger Account report](../task/setup-workday-fin-spoke.md#).

</td></tr><tr><td>

Look up Payments and Payment Status

</td><td>

Retrieves the payment and payment status details from Workday and saves the details as an attachment in the Data Source table.**Note:** To use this action, you must create and configure the Payment Status RaaS report. For instructions, see [Configure the Payment Status report](../task/setup-workday-fin-spoke.md#).

</td></tr><tr><td rowspan="4">

Journal Entry Management

</td><td>

Create Accounting Journal

</td><td>

Creates an accounting journal.

</td></tr><tr><td>

Look up Journals

</td><td>

Retrieves details of the required journal records, based on the provided filter criteria.

</td></tr><tr><td>

Post Accounting Journal

</td><td>

Posts an accounting journal record.

</td></tr><tr><td>

Reverse Accounting Journal

</td><td>

Reverses the specified accounting journal.

</td></tr><tr><td rowspan="3">

Metadata Retrieval

</td><td>

Get Additional Fields For Workday Finance

</td><td>

Retrieves additional fields for each action.

</td></tr><tr><td>

Get Reference ID List

</td><td>

Retrieves values of the Reference ID based on the specified reference type.

</td></tr><tr><td>

Get Access Token

</td><td>

Retrieves the access tokens for authenticating SOAP based actions using OAuth 2.0.

</td></tr><tr><td rowspan="18">

Resource Management

</td><td>

Cancel Purchase Order

</td><td>

Cancels the specified purchase order.

</td></tr><tr><td>

Create Fixed Asset Shell

</td><td>

Creates a fixed asset shell.

</td></tr><tr><td>

Create Supplier

</td><td>

Creates a supplier with the provided details.

</td></tr><tr><td>

Create Supplier Invoice

</td><td>

Creates a supplier invoice with the provided details.

</td></tr><tr><td>

Get Advanced Shipment Notice By Number

</td><td>

Retrieves details of the specified advance shipment notice.

</td></tr><tr><td>

Get Supplier By ID

</td><td>

Retrieves details of the specified supplier.

</td></tr><tr><td>

Get Supplier Invoice By ID

</td><td>

Retrieves details of the specified supplier invoice.

</td></tr><tr><td>

Look up Advanced Shipment Notices

</td><td>

Retrieves details of the required advance shipment notices, based on the provided filter criteria.

</td></tr><tr><td>

Look up Expense Items

</td><td>

Retrieves details of the required expense items, based on the provided filter criteria.

</td></tr><tr><td>

Look up Fixed Asset Details

</td><td>

Retrieves details of the required fixed assets, based on the provided filter criteria.

</td></tr><tr><td>

Look up Material Groups Stream

</td><td>

Retrieves the catalog data.

</td></tr><tr><td>

Look up Purchase Items

</td><td>

Retrieves details of the required purchase items, based on the provided filter criteria.

</td></tr><tr><td>

Look up Request For Quotes

</td><td>

Retrieves details of the required request for quotes records, based on the provided filter criteria.

</td></tr><tr><td>

Look up Supplier Invoices

</td><td>

Retrieves details of the required supplier invoices, based on the provided filter criteria.

</td></tr><tr><td>

Look up Suppliers

</td><td>

Retrieves details of the required suppliers, based on the provided filter criteria.

</td></tr><tr><td>

Submit Purchase Order

</td><td>

Submits the specified purchase order.

</td></tr><tr><td>

Submit Purchase Order Change Order

</td><td>

Submits change order associated with the specified purchase order.

</td></tr><tr><td>

Submit Receipt

</td><td>

Submits the specified receipt.

</td></tr></tbody>
</table>## Spoke module

The Workday Financials spoke adds the Workday Finance application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Connection Details|Contains information about the base URL of the Workday instance or tenant, and API version.|
|Get Business Units|Displays information about the business units. Admin should configure the sample remote table as per their requirement.|
|Purchase Orders|Displays information about the purchase orders whenever they are created in the Workday application. To retrieve this information to the ServiceNow instance, you must [Set up webhook for your Workday Financials spoke](../task/setup-webhk-wd.md#).|
|Webhook Registries|Contains records of webhooks registries. Admin should create record here [Set up webhook for your Workday Financials spoke](../task/setup-webhk-wd.md#) for the required Workday event.|

For information about setting up the spoke, see [Set up the Workday Financials spoke](../task/setup-workday-fin-spoke.md#) and [Set up webhook for your Workday Financials spoke](../task/setup-webhk-wd.md#).

