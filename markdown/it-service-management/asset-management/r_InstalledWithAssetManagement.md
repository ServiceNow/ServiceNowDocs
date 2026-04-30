---
title: Installed with Asset Management
description: Several tables, user roles, UI policies, script includes, client scripts, and business rules are installed with Asset Management.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [Asset Management, IT Service Management]
---

# Installed with Asset Management

Several tables, user roles, UI policies, script includes, client scripts, and business rules are installed with Asset Management.

Demo data is available with asset management. The demo data provides information such as users, assets, and individual stockrooms.

## Tables

Asset Management includes the following tables.

<table id="table_q2k_3xf_jq"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Asset \[alm\_asset\]

</td><td>

Stores general, financial, and contractual information about assets.

</td></tr><tr><td>

Asset Entitlement \[alm\_entitlement\_asset\]

</td><td>

Enables ServiceNow to categorize the Asset Entitlement table and enforce how entitlements behave.

</td></tr><tr><td>

Consumable \[alm\_consumable\]

</td><td>

Stores data about consumable assets \(previously known as parts\).

</td></tr><tr><td>

Default Stockroom \[alm\_user\_stockroom\]

</td><td>

Stores the relationship between a user and their default stockroom.

</td></tr><tr><td>

Fixed Assets \[alm\_fixed\_assets\]

</td><td>

Stores fixed assets, which are containers that can hold multiple assets.

</td></tr><tr><td>

Fixed asset to asset \[m2m\_fixed\_asset\_to\_asset\]

</td><td>

Stores associations between fixed assets and assets.

</td></tr><tr><td>

Hardware \[alm\_hardware\]

</td><td>

Stores general, financial, and contractual information about hardware assets.

</td></tr><tr><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Stores entitlements that permit users or machines to use a software license.

</td></tr><tr><td>

Software License \[alm\_license\]

</td><td>

Stores general, financial, and contractual information about software license assets.

</td></tr><tr><td>

Stock Rule \[alm\_stock\_rule\]

</td><td>

Transfers stock or sends an email message to the asset manager when a specified asset drops below a set threshold.

</td></tr><tr><td>

Stockroom \[alm\_stockroom\]

</td><td>

Stores information about stockrooms.

</td></tr><tr><td>

Stockroom Model \[alm\_m2m\_stockroom\_model\]

</td><td>

Tracks all models that have ever been stocked in a stockroom. This table is automatically populated.

</td></tr><tr><td>

Stockroom Type \[alm\_stockroom\_type\]

</td><td>

Stores general information about stockroom types.

</td></tr><tr><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Contains data about transfer orders, including the state and stockrooms.**Note:** The inventory\_user, asset, or procurement\_user role can only access the reports. You must activate the Procurement \(com.snc.procurement\) plugin for the inventory\_user, asset, and procurement\_user roles.

</td></tr><tr><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Contains data about individual assets being shipped with a transfer order.

</td></tr><tr><td>

User Entitlement \[alm\_entitlement\_user\]

</td><td>

Enables ServiceNow to categorize the User Entitlement table and enforce how entitlements behave.

</td></tr></tbody>
</table>## User roles

Asset Management includes the following user roles.

<table id="table_cck_nyf_jq"><thead><tr><th>

Role

</th><th>

Contains roles

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

asset \(Asset Manager\)

</td><td>

-   category manager
-   contract manager
-   financial mgmt user
-   inventory user
-   procurement user

</td><td>

-   Manage hardware and consumable assets \(\[alm\_hardware\] and \[alm\_consumable\]\).
-   Asset manager can’t edit asset records that are created and updated automatically, but can read and delete the asset records when needed.
-   Create requests.
-   Create and delete stock information.
-   Access to requests, purchase orders, and base system catalog tasks.

</td></tr><tr><td>

inventory\_admin

</td><td>

inventory user

</td><td>

-   Create and delete stock information.
-   Edit stock rules, stockrooms, and stockroom types.

</td></tr><tr><td>

inventory\_user

</td><td>

none

</td><td>

-   Access stock information.
-   Create and manage transfer orders.

</td></tr><tr><td>

sam

</td><td>

-   contract manager
-   model manager
-   financial mgmt user

</td><td>

-   Create, edit, change, and manage software licenses.
-   Edit the Software model field on a [Discovery models and software installations](https://www.servicenow.com/docs/access?context=c_DiscoveryModels&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).
-   Approve a model. Has full control of the Software Asset Management application.
-   Controls the Software Asset Management IBM PVU Process Pack, if activated.

</td></tr></tbody>
</table>## UI policies

Asset Management includes the following UI policies.

<table id="table_l1r_4zf_jq"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide asset tag and serial num

</td><td>

\[alm\_asset\]

</td><td>

Hides the asset tag when the asset is pre-allocated and the quantity is greater than 1.

</td></tr><tr><td>

Hide/show parent stockroom on Stockroom Replenish

</td><td>

\[alm\_stock\_rule\]

</td><td>

Shows the Parent stockroom field only when the Restocking option field is set to Stockroom.

</td></tr><tr><td>

Make allocated to and assigned to required.

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Makes the Allocated to and Assigned to fields required.

</td></tr><tr><td>

Make substatus read-only when not required

</td><td>

\[alm\_asset\]

</td><td>

Sets the Substatus to read-only if the State is On order, In use, Consumed, or In maintenance.

</td></tr><tr><td>

Model bundle field hidden but present for UI Policy conditions purposes

</td><td>

\[alm\_asset\]

</td><td>

Hides the Model Bundle field. Exists on page only for use by UI policies and client scripts.

</td></tr><tr><td>

Pre-allocated constraints

</td><td>

\[alm\_asset\]

</td><td>

Hides unneeded fields and related lists when the asset is pre-allocated.

</td></tr><tr><td>

Quantity readonly until model and category qualify the asset and are not bundle

</td><td>

\[alm\_asset\]

</td><td>

Sets the Quantity field to read-only for assets that aren’t consumable, software, or pre-allocated. Quantity is also read-only if the model or model category fields are empty.

</td></tr><tr><td>

Show 'Assigned to'

</td><td>

\[alm\_asset\]

</td><td>

Shows the Assigned to field if the State field is notOn order, In stock, or In transit.

</td></tr><tr><td>

Show 'Reserved for'

</td><td>

\[alm\_asset\]

</td><td>

Shows the Reserved for field if the State field is On order, In stock, or In transit.

</td></tr><tr><td>

Show 'Stockroom'

</td><td>

\[alm\_asset\]

</td><td>

Shows the Stockroom field if either of the following conditions is true:-   The State field is In stock and Substate isn’t Pre-allocated.
-   The Substate is Pre-allocated and Parent is empty.

</td></tr></tbody>
</table>## Script includes

Asset Management includes the following script includes.

|Name|Description|
|----|-----------|
|AssetandCI|Code for creating and managing the relationship between asset and CI records.|
|AssetAndCISynchronizer|Synchronization code between asset and CI records.|
|AssetUtils|Utility functions for asset management. Also checks if a license can be merged and then merges licenses if requirements are met.|
|AssetUtilsAJAX|AJAX-based utility functions for asset management. Call the AssetUtils script include from a client-side UI action.|
|Consumables|Code to change \(for example, consume, split, and merge\) consumables.|
|FixedAssetUtils|Methods for rolling up fixed asset costs.|
|PortalFilters|Filters used in the My Assets portal.|
|PreAllocatedAssets|Code to change pre-allocated assets.|
|StockRuleFilters|Reference qualifier code for filtering options on reference fields on stock rules.|
|StockRuleTransfer|Transfer order creation code for when stock rules are triggered.|
|TransferOrderDateTimeAjax|Date comparison utility for transfer orders.|
|TransferOrderFilters|Reference qualifier code for reference field filtering options on transfer orders.|
|TransferOrderFinder|Finds an appropriate transfer order to put a transfer order line into.|
|TransferOrderHelper|Function that checks if a transfer order has multiple transfer order lines.|
|TransferOrderLineFilters|Reference qualifier code for reference field filtering options on transfer order lines.|
|TransferOrderReceiver|Code for receiving a transfer order line.|
|TransferOrderReturn|Code for returning a transfer order line.|
|TransferOrderStageHandler|Code for changing transfer order stages and transfer order line stages.|
|TransferOrderStageHelper|Helper method to get numeric stages for transfer orders and transfer order lines.|

## Client scripts

Asset Management includes the following client scripts.

<table id="table_m1b_pcg_jq"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Correct substatus

</td><td>

\[alm\_asset\]

</td><td>

Updates the Substatus field when the Status field is modified.

</td></tr><tr><td>

Ensure no negative quantity

</td><td>

\[alm\_asset\]

</td><td>

Clears the Quantity field when set to less than 1.

</td></tr><tr><td>

Error on pre-allocated substatus

</td><td>

\[alm\_consumable\]

</td><td>

Prevents Substatus field from being set to be Pre-allocated for consumable assets. Also displays an error message.

</td></tr><tr><td>

Error on pre-allocated substatus

</td><td>

\[alm\_license\]

</td><td>

Prevents Substatus field from being set to be Pre-allocated for license assets. Also displays an error message.

</td></tr><tr><td>

Null out allocated\_to

</td><td>

\[alm\_entitlement\]

</td><td>

Does the following when the Assigned to field is set:-   Clears the Allocated to field and makes it not required.
-   Makes the Assigned to field required.

</td></tr><tr><td>

Null out assigned\_to

</td><td>

\[alm\_entitlement\]

</td><td>

Does the following when the Allocated to field is set:-   Clears the Assigned to field and makes it not required.
-   Makes the Allocated to field required.

</td></tr><tr><td>

Salvage must be less than cost

</td><td>

\[alm\_asset\]

</td><td>

Displays a warning if a salvage value greater than the cost of an asset is entered.

</td></tr><tr><td>

Set Cost of the Asset

</td><td>

\[alm\_asset\]

</td><td>

Populates the Cost field when the Model field is set.

</td></tr><tr><td>

Set Loc/CC/Dep/Com from assigned to

</td><td>

\[alm\_asset\]

</td><td>

Populates the Location, Cost center, Department, and Company fields when the Assigned to field is set.

</td></tr><tr><td>

Set Location from stockroom

</td><td>

\[alm\_asset\]

</td><td>

Populates the Location field when the Stockroom field is set.

</td></tr><tr><td>

Update From Location from Stockroom

</td><td>

\[alm\_transfer\_order\]

</td><td>

Populates the From location field when the From stockroom field is set.

</td></tr><tr><td>

Update Model and Quantity based on Asset

</td><td>

\[alm\_transfer\_order\_line\]

</td><td>

Populates the Model field when the Asset field is set. If the asset is a pre-allocated asset, this client script also populates the Quantity field.

</td></tr><tr><td>

Update To Location from Stockroom

</td><td>

\[alm\_transfer\_order\]

</td><td>

Populates the To location field when the To stockroom field is set.

</td></tr><tr><td>

Update UI on load and model change

</td><td>

\[alm\_transfer\_order\_line\]

</td><td>

Runs checks, and updates the user interface, when the transfer order line form is loaded and when a model is selected.

</td></tr><tr><td>

Validate Delivery by Date

</td><td>

\[alm\_transfer\_order\]

</td><td>

Validates that the delivery date is in the future.

</td></tr><tr><td>

Verify Stock Available

</td><td>

\[alm\_transfer\_order\_line\]

</td><td>

Verifies that stock exists to fulfill the quantity requested.

</td></tr><tr><td>

Verify Stock Available \(Stockroom\)

</td><td>

\[alm\_transfer\_order\_line\]

</td><td>

Verifies that stock exists to fulfill the quantity requested when the From stockroom value changes.

</td></tr></tbody>
</table>## Business rules

Asset Management includes the following business rules.

<table id="table_rjq_j2g_jq"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocated more licenses than rights

</td><td>

Software License \[alm\_license\]

</td><td>

Prevents creation or update of a license if the number of licenses allocated is larger than the total rights.

</td></tr><tr><td>

Asset Retirement

</td><td>

Asset \[alm\_asset\]

</td><td>

Clears the Assigned to, Stockroom, and Reserved for fields and sets the retirement date to the current time when the asset is retired.

</td></tr><tr><td>

Automatically Change TOL State

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

If a transfer order has the same From stockroom and To stockroom and it’s a personal stockroom, this business rule:-   Sets the transfer order line Stage to Delivered.
-   Sets the asset Substate to Reserved.

 If a transfer order has the same From stockroom and To stockroom and it isn’t a personal stockroom, this business rule:

-   Sets the transfer order Stage to Received.
-   Sets the asset Substate to Pending transfer.

</td></tr><tr><td>

Build bundle components on Insert

</td><td>

Asset \[alm\_asset\]

</td><td>

Creates assets for the components related to a bundle if the model of the created asset is a bundle.

</td></tr><tr><td>

Clear Assigned To on update

</td><td>

Asset \[alm\_asset\]

</td><td>

Clears the Assigned to field if the State field changes to On order, In stock, or In transit.

</td></tr><tr><td>

Clear fields irrelevant for preallocated

</td><td>

Asset \[alm\_asset\]

</td><td>

Clears the value of fields that are irrelevant for pre-allocated assets.

</td></tr><tr><td>

Create Asset on insert

</td><td>

Configuration Items \[cmdb\_ci\]

</td><td>

Creates a corresponding asset when a new configuration item with no asset is created.

</td></tr><tr><td>

Create asset on model change

</td><td>

Configuration Items \[cmdb\_ci\]

</td><td>

Creates a new associated asset when the Model ID field changes.

</td></tr><tr><td>

Create CI on insert

</td><td>

Asset \[alm\_asset\]

</td><td>

Creates a corresponding configuration item when a new asset with no configuration item is created.

</td></tr><tr><td>

Create Stockroom Model Relation

</td><td>

Asset \[alm\_asset\]

</td><td>

Creates a record \(if none exists\) in the Stockroom Model table indicating the stockroom that holds the model when an asset is created or updated.

</td></tr><tr><td>

Delete all Transfer Order Lines

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Deletes all related transfer order lines when a transfer order is deleted.

</td></tr><tr><td>

Ensure Entitlements do not exceed rights

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Checks that the total number of entitlements for the related license doesn’t exceed the number of rights given by the license when an entitlement is created.

</td></tr><tr><td>

GenerateAssets

</td><td>

Model Categories \[cmdb\_model\_category\]

</td><td>

Executes a scheduled script job to create assets for configuration items.

</td></tr><tr><td>

Inherit information from parent

</td><td>

Asset \[alm\_asset\]

</td><td>

Assigns some parent values to the asset when assigning a new parent to an asset.

</td></tr><tr><td>

Managed Stockroom for Vendor

</td><td>

Stock Rule \[alm\_stock\_rule\]

</td><td>

Validates that a vendor replenishing stock rule has a stockroom selected and the stockroom has an related manager with a valid email address.

</td></tr><tr><td>

Mandate allocated to or assigned to

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Makes a value in either the Allocated to field or the Assigned to field required.

</td></tr><tr><td>

Merge Records

</td><td>

Consumable \[alm\_consumable\]

</td><td>

Merges consumables that have matching fields and aren’t In Transit into one record containing the total count.

</td></tr><tr><td>

Null out asset on insert and stay

</td><td>

Configuration Items \[cmdb\_ci\]

</td><td>

Clears the Asset field on insert when the field includes an asset that has a CI.

</td></tr><tr><td>

Null out Ci on insert and stay

</td><td>

Asset \[alm\_asset\]

</td><td>

Nulls out the asset field so a new asset is created for the CI when an insert is performed on an existing CI.

</td></tr><tr><td>

Populate reserved for field

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

If the transfer order line has an related request line, this business rule populates the related asset's Reserved for field with the appropriate information from the request line.

</td></tr><tr><td>

Push Status to Asset/Consumable

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Changes the corresponding asset to reflect the current state of transit when a transfer order line moves to another state.

</td></tr><tr><td>

Release Asset on TOL cancel/delete

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Places the corresponding asset back into stock and unsources the part requirement when a transfer order line in the draft state is canceled or deleted.

</td></tr><tr><td>

Rollup TOL cancellation to TO

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Signals to the corresponding transfer order that the transfer order line has been canceled.

</td></tr><tr><td>

Salvage value must be less than cost

</td><td>

Asset \[alm\_asset\]

</td><td>

Prevents saving an asset record if the salvage value is greater than the cost.

</td></tr><tr><td>

Sanity check on pre-allocated

</td><td>

Asset \[alm\_asset\]

</td><td>

Prevents creation or update of pre-allocated assets if they don’t satisfy the conditions to be pre-allocated.

</td></tr><tr><td>

Set Class

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Sets the class for this entitlement depending on the entitlement is assigned or allocated.

</td></tr><tr><td>

Set Transfer Order Type

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Sets the type of the transfer order depending on whether there’s a related service order or work order task.

</td></tr><tr><td>

Sync model category

</td><td>

Product Models \[cmdb\_model\]

</td><td>

When the model category changes, this business rule creates assets if they didn’t previously exist for configuration items associated with the model.

</td></tr><tr><td>

Transfer Order Stockroom Rules

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Prevents the From stockroom field from being changed if the transfer order has multiple transfer order lines.

</td></tr><tr><td>

Transition reserved to assigned

</td><td>

Asset \[alm\_asset\]

</td><td>

Populates the Assigned to field with the value from the Reserved for field when the asset is in the appropriate state.

</td></tr><tr><td>

Trickle information down to components

</td><td>

Asset \[alm\_asset\]

</td><td>

Updates components of an asset to reflect any changes that have been made to the asset record.

</td></tr><tr><td>

Update Asset fields on change

</td><td>

Configuration Items \[cmdb\_ci\]

</td><td>

Synchronizes fields so changes made on the Configuration Item form trigger the same update on the corresponding Asset form, ensuring consistent reporting. You must update statuses on the Asset form.

</td></tr><tr><td>

Update CI fields on change

</td><td>

Asset \[alm\_asset\]

</td><td>

Synchronizes fields so changes made on the Asset form trigger the same update on the corresponding Configuration Item form, ensuring consistent reporting.

</td></tr><tr><td>

Update location as needed

</td><td>

Asset \[alm\_asset\]

</td><td>

Updates the location of the asset, if the asset is set to a new stockroom or assigned to a new user.

</td></tr><tr><td>

Validate Field Agent Type

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Ensures that you don’t create a stockroom of the type Field Agent without Work Management or Field Service Management activated. Allows for only one personal stockroom per user.

</td></tr><tr><td>

Validate TOL and check availability

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Validates changes made to the transfer order line and checks the availability of the assets to be transferred in the specified stockroom.

</td></tr><tr><td>

Validate transfer order

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Validates that the Delivery by date isn’t earlier than the current date.

</td></tr><tr><td>

Validate Unique Users

</td><td>

Default Stockroom \[alm\_user\_stockroom\]

</td><td>

Prevents the creation of multiple records with the same user.

</td></tr><tr><td>

Verify Entitlement \(Allocated\)

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Ensures that the allocation of the entitlement follows the allocation condition on the license when a condition exists.

</td></tr><tr><td>

Verify Entitlement \(Assigned\)

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Ensures that the assignee of the entitlement follows the assignment condition on the license when a condition exists.

</td></tr><tr><td>

Verify Entitlements \(Allocated\)

</td><td>

Software License \[alm\_license\]

</td><td>

Ensures that the allocations of all the license's entitlements follow the allocation condition on the license when a condition exists.

</td></tr><tr><td>

Verify Entitlements \(Assigned\)

</td><td>

Software License \[alm\_license\]

</td><td>

Ensures that the assignees of all the license's entitlements follow the assignment condition on the license when a condition exists.

</td></tr><tr><td>

Verify Not Field Agent

</td><td>

Default Stockroom \[alm\_user\_stockroom\]

</td><td>

Verifies that the selected default stockroom isn’t of the Field Agent type.

</td></tr></tbody>
</table>**Parent Topic:**[Asset Management](../concept/c_AssetManagement.md)

