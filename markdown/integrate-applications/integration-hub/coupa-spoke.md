---
title: Coupa Spoke
description: Manage business spend and automate approval, contract, inventory, purchase order, requisition, supplier, and user management in Coupa from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Coupa Spoke

Manage business spend and automate approval, contract, inventory, purchase order, requisition, supplier, and user management in Coupa from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Coupa spoke v4.15 is the latest version.

## Supported versions

This spoke was built for Coupa version stable\_v4.2.0, but may be compatible with later versions.

## Spoke requirements

Create an API key in your Coupa instance and record the API key for later use. See [Coupa documentation](https://success.coupa.com/Support/Docs) for information about creating API key.

## Spoke user roles

The following user roles are available with the spoke:

-   Coupa Admin \(sn\_coupa\_spoke.Coupa Admin\): Users with this role have access to both, **My Current Approvals** and **Contracts** modules.
-   Coupa Approval User \(sn\_coupa\_spoke.Coupa Approval User\): Users with this role have access only to the **My Current Approvals** module
-   Coupa Contract User \(sn\_coupa\_spoke.Coupa Contract User\): Users with this role have access only to the **Contracts** module.

## Spoke module

The Coupa spoke adds a Coupa application to your ServiceNow instance. The Coupa application supports Coupa Approval User and Coupa Contract User roles. You can access the Coupa application from the ServiceNow instance on your Now Mobile app.

**Note:** Make sure that Coupa Login attribute and the user ID of ServiceNow instance match before using the **My Current Approvals** module.

The Coupa application has the following modules.

|Module|Description|
|------|-----------|
|My Current Approvals|Displays the list of approvals in Coupa for a user.|
|Contracts|Displays a list of contracts in Coupa.|

## Available sample conversational subflows

Install Now Assist for Conversational Spokes and start using the conversational ability of Integration Hub spokes. For more information, see [Now Assist in Conversational Spokes](../../integrationhub/concept/conv-spokes-na.md).

|Conversational subflow|Description|
|----------------------|-----------|
|Look up Suppliers - Sample|Retrieves the specified supplier in Coupa using the Coupa query.|
|Look up Purchase Orders - Sample|Retrieves the specified purchase order in Coupa using the Coupa query.|
|Look up Contracts - Sample|Retrieves the specified contract records in Coupa using the Coupa query.|
|Look up Receipts - Sample|Retrieves the specified receipts in Coupa using the Coupa query.|
|Look up Invoices - Sample|Retrieves details of the specified invoices in Coupa.​|
|Look up Approvals - Sample|Retrieves details of approvals in Coupa.|
|Look up Requisitions - Sample|Retrieves the specified requisitions in Coupa using the Coupa query.|

## Spoke actions

The Coupa spoke provides actions to automate approval, contract, inventory, invoice, catalog item, purchase order, requisition, supplier, and user management when events occur in ServiceNow. Available actions include:

<table id="table_mtz_54v_vjb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="6">

Approval Management

</td><td>

Approve Approval Request

</td><td>

Approves the required approval request in Coupa.

</td></tr><tr><td>

Look up Approval Details by Approval ID

</td><td>

Retrieves the details of the required approval in Coupa.

</td></tr><tr><td>

Look up Approval

</td><td>

Looks up an approval record in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Approval By Requisition ID

</td><td>

Looks up the required approval record in Coupa using its Requisition ID.

</td></tr><tr><td>

Look up Approvals Stream

</td><td>

Retrieves details of approvals in Coupa.

</td></tr><tr><td>

Reject Approval Request

</td><td>

Rejects the required approval request in Coupa.

</td></tr><tr><td>

Catalog Management

</td><td>

Create Item

</td><td>

Creates an item in Coupa.

</td></tr><tr><td rowspan="2">

Contract Management

</td><td>

Create Contract

</td><td>

Creates contract with the provided details in Coupa.

</td></tr><tr><td>

Look up Contracts Stream

</td><td>

Looks up the required contract records in Coupa using the Coupa query.

</td></tr><tr><td rowspan="8">

Primary Data Management

</td><td>

Look up Addresses Stream

</td><td>

Retrieves the address details from Coupa.

</td></tr><tr><td>

Look up Conversion Rates Stream

</td><td>

Retrieves details of the conversion rates in Coupa.

</td></tr><tr><td>

Look up Currencies Stream

</td><td>

Retrieves details of currencies in Coupa.

</td></tr><tr><td>

Look up Legal Entities Stream

</td><td>

Retrieves details of the legal entities in Coupa.

</td></tr><tr><td>

Lookup Cost Centers Stream

</td><td>

Retrieves details of the cost centers in Coupa.

</td></tr><tr><td>

Look up Advanced Shipment Notices Stream After Updated Date

</td><td>

Retrieves details of advance shipment notices after filtering by the specified updated at field in Coupa.

</td></tr><tr><td>

Look up Advance Shipment Notice by Purchase Order Line ID

</td><td>

Retrieves details of the advance shipment notice for the specified purchase order line ID.

</td></tr><tr><td>

Look up Advanced Shipment Notices by Purchase Order Line ID Stream

</td><td>

Retrieves details of all advance shipment notices for the specified purchase order line ID.**Note:** This is a data stream action.

</td></tr><tr><td rowspan="9">

Inventory Management

</td><td>

Create Goods Receipt

</td><td>

Creates a goods receipt record in Coupa.

</td></tr><tr><td>

Create Receipt

</td><td>

Creates a receipt in Coupa.**Note:** Ensure that description has the exact item name. When you want to access the item name in a flow, use the description data pill.

</td></tr><tr><td>

Get Receipt Fields

</td><td>

Retrieves the list of fields in the Coupa Receipts table.**Note:** This is a metadata action and doesn't make an API call to Coupa.

</td></tr><tr><td>

Look up Advanced Shipment Notices After Updated Date

</td><td>

Retrieves the details of the advance shipment notices after the updated date in Coupa.

</td></tr><tr><td>

Look up Advance Shipment Notice By Purchase Order Line ID

</td><td>

Look up an advance shipment notice by purchase order line ID in Coupa.

</td></tr><tr><td>

Look up Receipt

</td><td>

Looks up the required receipt in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Receipt Details by Receipt ID

</td><td>

Retrieves details of the required receipt.

</td></tr><tr><td>

Look up Receipts Stream

</td><td>

Looks up the required receipts in Coupa using the Coupa query.

</td></tr><tr><td>

Void Receipt

</td><td>

Makes the required receipt void.

</td></tr><tr><td rowspan="5">

Invoice Management

</td><td>

Create Invoice

</td><td>

Creates an invoice with the provided details in Coupa.

</td></tr><tr><td>

Update Invoice

</td><td>

Updates the details of the specified invoice in Coupa.

</td></tr><tr><td>

Void Invoice

</td><td>

Makes the required invoice void.

</td></tr><tr><td>

Look up Invoices Stream

</td><td>

Retrieves details of the required invoices in Coupa.​

</td></tr><tr><td>

Look up Invoice Payments Details Stream

</td><td>

Retrieves information about the required invoice payment details in Coupa.

</td></tr><tr><td rowspan="2">

Item Management

</td><td>

Look up Items Stream

</td><td>

Looks up the required items in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Item

</td><td>

Looks up the required item in Coupa using the Coupa query.

</td></tr><tr><td rowspan="9">

Purchase Order Management

</td><td>

Cancel Purchase Order

</td><td>

Cancels the required purchase order in Coupa.

</td></tr><tr><td>

Close Purchase Order

</td><td>

Closes the required purchase order in Coupa.

</td></tr><tr><td>

Create Fixed Assets

</td><td>

Creates fixed assets with the specified details in Coupa.

</td></tr><tr><td>

Create Purchase Order

</td><td>

Creates a purchase order in Coupa.

</td></tr><tr><td>

Look up PO Line by Line ID

</td><td>

Retrieves details of a purchase order line in Coupa.

</td></tr><tr><td>

Look up Purchase Order

</td><td>

Looks up the required purchase order in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Purchase Orders Stream

</td><td>

Looks up the details of the purchase orders in Coupa that you specify using the Coupa query.

</td></tr><tr><td>

Revise Purchase Order

</td><td>

Revises or updates the purchase order in Coupa.

</td></tr><tr><td>

Update Purchase Order Status in Coupa

</td><td>

Updates status of the required purchase order in Coupa.

</td></tr><tr><td rowspan="6">

Requisition Management

</td><td>

Create Draft Requisition

</td><td>

Creates a requisition in Coupa with its status as Draft.

</td></tr><tr><td>

Create Requisition

</td><td>

Creates a requisition with the status as Pending Approval or Pending Buyer Action.

</td></tr><tr><td>

Get Requisition Fields

</td><td>

Retrieves the list of fields in the Coupa Requisitions table.**Note:** This is a metadata action and doesn't make an API call to Coupa.

</td></tr><tr><td>

Look up Requisition

</td><td>

Looks up the required requisition in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Requisitions Stream

</td><td>

Looks up the required requisitions in Coupa using the Coupa query.

</td></tr><tr><td>

Update Requisition

</td><td>

Updates an existing requisition in Coupa.

</td></tr><tr><td rowspan="4">

Sourcing Management

</td><td>

Award Purchase

</td><td>

Awards a purchase in Coupa. To award a purchase, you can specify the quote request ID and the quote supplier ID as inputs.

</td></tr><tr><td>

Create Sourcing Event

</td><td>

Creates a sourcing event in Coupa.

</td></tr><tr><td>

Look up Sourcing Quote Response Stream

</td><td>

Looks up the quote response in Coupa based on the quote request ID that you specify. You can also specify other criteria such as the limit of records that the response returns, and the offset.

</td></tr><tr><td>

Look up Sourcing Events Stream

</td><td>

Retrieves details of the required sourcing event in Coupa.

</td></tr><tr><td rowspan="7">

Supplier Management

</td><td>

Look up Supplier

</td><td>

Looks up the required supplier in Coupa using the Coupa query.

</td></tr><tr><td>

Create Supplier

</td><td>

Creates a supplier in Coupa.

</td></tr><tr><td>

Deactivate Supplier

</td><td>

Deactivates the specified supplier in Coupa.

</td></tr><tr><td>

Update Supplier

</td><td>

Updates details of the specified supplier in Coupa.

</td></tr><tr><td>

Look up Product Catalogs Stream

</td><td>

Retrieves the product catalogs in Coupa.

</td></tr><tr><td>

Look up Suppliers Stream

</td><td>

Retrieves list of suppliers in Coupa using the query.

</td></tr><tr><td>

Look up Suppliers Payment Stream

</td><td>

Retrieves details of the required supplier payments in Coupa.

</td></tr><tr><td rowspan="3">

User Management

</td><td>

Look up User

</td><td>

Looks up the required user in Coupa using the Coupa query.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Looks up the required users in Coupa using the Coupa query.

</td></tr><tr><td>

Reset User Password

</td><td>

Resets password of the required user in Coupa.

</td></tr></tbody>
</table>**Note:** Remote tables are created when the Coupa spoke is activated. Users are cautioned against directly modifying schema or inserting data in these tables.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

Available AI agents include:

|AI Agent|Description|
|--------|-----------|
|Coupa sourcing management AI agent|Manages sourcing data \(that is, looks up sourcing event streams, creates new sourcing events\) in Coupa.|
|Coupa approval management AI agent|Manages approvals \(that is, looks up approvals, retrieves approval details\) in Coupa.|
|Coupa requisition management AI agent|Manages requisition \(that is, looks up operations to retrieve requisition data\) in Coupa.|
|Coupa purchase order management AI agent|Manages purchase orders \(that is, closes purchase orders, retrieves detailed purchase order information, and creates fixed assets\) in Coupa.|
|Coupa invoice management AI agent|Manages invoices \(that is, creates invoices, retrieves invoice details, and queries payment details\) in Coupa.|
|Coupa inventory management AI agent|Manages inventories \(that is, looks up receipt details, manages advanced shipment notices, and creates goods receipts\) in Coupa.|
|Coupa supplier management AI agent|Manages supplier information \(that is, creates, retrieves supplier and product catalog information\) in Coupa.|
|Coupa item management AI agent|Manages items \(that is, look up items and retrieve item streams\) in Coupa.|
|Coupa primary data management AI agent|Manages primary data \(that is, looks up conversion rates, cost centers, currencies, and legal entities\) in Coupa.|
|Coupa user management AI agent|Manages users \(that is, reset user passwords, look up individual user details, and retrieve streams of user data\) in Coupa.|
|Coupa catalog management AI agent|Creates a catalog item in Coupa.|
|Coupa contract management AI agent|Manages contracts \(that is, looks up or creates a contract\) in Coupa.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see Find AI agents.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

