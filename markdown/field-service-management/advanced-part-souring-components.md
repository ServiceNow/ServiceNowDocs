---
title: Advanced Part Sourcing components
description: Several types of components are installed with the Advanced Part Sourcing feature, including tables, script includes and business rules.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Components installed with additional plugins, Reference, Field Service Management]
---

# Advanced Part Sourcing components

Several types of components are installed with the Advanced Part Sourcing feature, including tables, script includes and business rules.

## Plugin

The Field Service Advanced Parts Sourcing \(com.snc.fsm\_advanced\_parts\_sourcing\) plugin must be activated. For more information on the steps to activate a plugin, see [Activate Field Service Management](../../planning-and-policy/task/t_ActivateFieldServiceManagement.md).

## Business rules

Advanced Parts Sourcing adds the following business rules.

<table id="table_fjn_xlk_1mb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Limit number of lines in a part request

</td><td>

Part Request Line ​ \[sn\_fsm\_part\_req\_line\]

</td><td>

Limits the number of part request lines in a part request. The limit is configured in the **sn\_fsm\_parts\_src.Maximum parts in Part Request** property.

</td></tr><tr><td>

Manage requested quantity​

</td><td>

Part Request Line ​ \[sn\_fsm\_part\_req\_line\]

</td><td>

Updates the **Requested\_quantity** field in the part requirement when a part request line changes its state.

</td></tr><tr><td>

Populate or clearout from\_stockroom

</td><td>

Part Request Line ​ \[sn\_fsm\_part\_req\_line\]

</td><td>

In the part request, if all part request lines have the same **From stockroom** field value, the part request record is populated for multi-sourcing. If the value in the **From stockroom** field is different, that value is cleared.

</td></tr><tr><td>

Restrict Duplicate Entry

</td><td>

Preferred Stockroom \[sn\_fsm\_pref\_stockroom\]

</td><td>

Prevents the user from creating the duplicate record.

</td></tr><tr><td>

Set requested model same as required

</td><td>

Part Request Line \[sn\_fsm\_part\_req\_line\]

</td><td>

Sets the requested model same as required in case of non-substitute sourcing.

</td></tr><tr><td>

Update part request line

</td><td>

Requested Item Detail \[sn\_fsm\_part\_req\_ritm\_detail\]

</td><td>

Creates a RITM record and updates the part request line state to Requested when agent submits the part request.

</td></tr><tr><td>

Update part request state

</td><td>

Part Request Line \[sn\_fsm\_part\_req\_line\]

</td><td>

Updates the part request state when the part request line state changes.

</td></tr><tr><td>

Validate asset quantity and sync assets

</td><td>

Requested Item Detail \[sn\_fsm\_part\_req\_ritm\_detail\]

</td><td>

Validates that the number of assets selected matches the requested quantity. Also, synchronizes the values of selected asset IDs between the Requested Item Detail field and the Requested Item field of the RITM record.

</td></tr><tr><td>

Validate requested quantity

</td><td>

Part Request Line \[sn\_fsm\_part\_req\_line\]

</td><td>

Ensures that the requested part quantity is not more than difference between the required and reserved quantity. For example, Requested quantity &lt;= \(Required quantity - Reserved quantity\).

</td></tr><tr><td>

Validate Maximum Part Search Radius

</td><td>

Resource Schedule Attributes\[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Ensures that the value entered in the **Validate Maximum Part Search Radius** field is not less than zero.

</td></tr><tr><td>

Default requested for when WOT empty

</td><td>

Part Requirement \[sm\_part\_requirement\]

</td><td>

Sets the **Default requested** field to the logged-in user when service order task is empty.

</td></tr><tr><td>

Set creation method field

</td><td>

Part Requirement \[sm\_part\_requirement\]

</td><td>

Sets the creation method field to **user created** when empty.

</td></tr></tbody>
</table>## Script includes

Advanced Part Sourcing adds the following script includes.

|Script include|Description|
|--------------|-----------|
|FSMPartRequestUtil​|Contains utility methods to create, update, or delete a part request and part request line.|
|FSMPartSourcingUtil​|Contains utility methods to submit a single or multiple parts request.|
|FSMMultiPartsSourcingUtil|Utilities file to identify stockrooms containing all the parts with the required quantity.|
|PartRequestFilters|Sets reference qualifier filters on part request fields.|
|PartRequestLineFilters|Sets reference qualifier filters on part request line fields.|
|UserAjaxUtil|Populates the requested quantity value on a part request line for a specified part requirement.|

## Tables

Advanced part sourcing adds the following tables.

<table id="table_crw_gwj_jbb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Part Request\[sn\_fsm\_part\_request\]

</td><td>

Stores the parts destination and requesting agent details.

</td></tr><tr><td>

Part Request Line\[sn\_fsm\_part\_req\_line\]

</td><td>

Stores part source and requirement details and associates them with the part request record.

</td></tr><tr><td>

Part request line To Transfer order line M2M\[sn\_fsm\_part\_req\_line\_tol\_rel​\]

</td><td>

Stores the relationship between the part request lines that are in the Completed state with transfer order lines that are in the Delivered state.

</td></tr><tr><td>

Requested Item Detailsn\_fsm\_part\_req\_ritm\_detail​

</td><td>

Stores the sourcing details of the part request line after the user has submitted the request.

</td></tr><tr><td>

Preferred Stockroomsn\_fsm\_pref\_stockroom

</td><td>

Stores the details of the preferred stockrooms that are associated with assignment groups.

</td></tr></tbody>
</table>Advanced Part Sourcing changes the following tables.

<table id="table_nng_n3x_d5b"><thead><tr><th>

Table

</th><th>

New columns added

</th></tr></thead><tbody><tr><td>

Part requirements\[sm\_part\_requirement​\]

</td><td>

Requested for, Requested quantity, Creation method, Include substitute

</td></tr><tr><td>

Work parameters\[wm\_agent\_work\_configuration​\]

</td><td>

Maximum part search radius

</td></tr><tr><td>

Geolocation History\[geo\_history​\]

</td><td>

Latest record

</td></tr></tbody>
</table>## Properties

Advanced Part Sourcing adds the following properties.

<table id="table_ovq_jnw_b5b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Part Search Criteria

</td><td>

Sets the criteria to search parts. The stockrooms that contains the parts with the requested quantity appear per the selected search criteria.-   **Type**: choice list
-   **Default value**: No restrictions
    -   **No Restrictions**: Search all warehouse stockrooms and the personal stockrooms of peer agents.
    -   **Only Assignment Group**: Search all stockrooms of peer agents who are part of the assignment groups of the logged-in field service agent.
    -   **Only Preferred Stockrooms**: Search all preferred stockrooms of all assignment groups irrespective of the radius mentioned in the logged-in agent's profile.
-   **Location**: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Use part request approvals

</td><td>

Enables sending and receiving mobile notifications as Field Service agents request parts from peer agents.-   **Type**: Boolean
-   **Default value**: Yes
-   **Location**: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Create part requests for part requirement sourcing

</td><td>

Creates a part request when a part is added to the part requirement.-   **Type**: Boolean
-   **Default value**: Yes
-   **Location**: **Field Service** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with additional plugins for Field Service Management](components-inst-additional-plugin.md)

