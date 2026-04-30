---
title: Change request and change task forms
description: The change request forms enable you to request a change.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 16
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Change request and change task forms

The change request forms enable you to request a change.

<table id="table_lh3_c13_1yb"><thead><tr><th>

Change model

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add cable

</td><td>

Change model to create a change task for adding a card. To learn more, see the add card form in [Change request and change task forms](change_request_forms.md).

</td></tr><tr><td>

Add Card

</td><td>

Change model to create a change request for adding an interface card. To learn more, see the add card form in [Change request and change task forms](change_request_forms.md).

</td></tr><tr><td>

Create inventory equipment

</td><td>

Change model to create a change request for creating inventory equipment. To learn more, see the create equipment form in [Change request and change task forms](change_request_forms.md).**Note:** To see the compute and create logical connection form, see [Compute and Create Logical Connection form](../reference/compute-and-create-logical-connection-form.md).

</td></tr><tr><td>

Create logical connection

</td><td>

Change model to create a change request for creating a logical connection. To learn more, see the [Change request and change task forms](change_request_forms.md).**Note:**

-   To update or revise a logical connection CI, see [Revise a configuration item using design and assign](revise-a-configuration-item.md).
-   To modify logical connection endpoints, see [Modify logical connection endpoints model](../task/create-a-change-request-by-using-modify-logical-connection-endpoints-model.md).

</td></tr><tr><td>

Create physical connection

</td><td>

Change model to create a change request for creating a physical connection. To learn more, see [Change request and change task forms](change_request_forms.md).**Note:**

-   To update or revise a physical connection CI, see [Revise a configuration item using design and assign](revise-a-configuration-item.md).
-   To modify physical connection endpoints, see [Modify physical connection endpoints](../task/create-a-change-request-by-using-modify-physical-connection.md).

</td></tr><tr><td>

Create Rack/Cabinet

</td><td>

Change model to create a change request for creating and visualizing a rack or cabinet. To learn more, see [Change request and change task forms](change_request_forms.md).

**Note:**

1.  For creating a rack or cabinet, ensure that the following exist:

    -   A model in equipment holder model with **Model categories** as **Equipment Rack**.
    -   A relationship in network model relationships with the **Relationship type** as **Rack to Slot**.
    -   A template in the inventory template where the **inventory model** has a rack model.
A rack is created based on the selected rack model in the template, and the rack slots are created based on the rack template.

2.  To add equipment to a rack, see [Create a change request from Network Inventory Workspace](../task/create_a_change_request_in_tni.md).

</td></tr><tr><td>

Add equipment to Rack/cabinet

</td><td>

Change model to add a new or existing equipment to a rack. To learn more, see [Change request and change task forms](change_request_forms.md).

</td></tr><tr><td>

Remove Equipment or Shelf from Rack/Cabinet

</td><td>

Change model to remove an equipment or a shelf from a rack or cabinet slot. To learn more, see [Change request and change task forms](change_request_forms.md).**Note:** Shelf cannot be removed if it is related to any equipment.

</td></tr><tr><td>

IP address allocation

</td><td>

Change model to create a change request for IP address allocation. To learn more, see the IP address allocation form in [Change request and change task forms](change_request_forms.md).

</td></tr><tr><td>

Phone number allocation

</td><td>

Change model to create a change request for a phone number allocation. To learn more, see the Manage phone number form in [Change request and change task forms](change_request_forms.md).

</td></tr></tbody>
</table>|Fields|Description|
|------|-----------|
|Order task|Specifies the fulfillment task generated from the service order to provision the GPON broadband service. This task is used to track and complete the technical fulfillment activities associated with the order.|
|Location|Specifies the physical network location where the GPON access infrastructure is installed.|
|Customer Site|Network site.|
|ONT equipment template|Equipment template.|
|Splitter|Equipment.|
|Splitter port|Port interface.|
|Pon Network Path|Pon logical connection.|
|ISPN VLAN|ISPN VLAN logical connection.|
|ISP EVPN VPWS|ISP EVPN VPWS logical connection.|
|IP Version|IP version.|
|Number of IP Addresses|Total number of IP addresses.|
|Start IP Address|Starting IP address.|

<table id="table_kcb_vqp_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Change request number.

</td></tr><tr><td>

Requested by

</td><td>

User who has requested the change. This field is available in the Change Requests list view so that you can see who requested a particular change.

</td></tr><tr><td>

Category

</td><td>

Category of this change request. Select **Other** if your category isn’t in the list.

</td></tr><tr><td>

Service

</td><td>

Business service that you want to make available for this change request.

</td></tr><tr><td>

Service offering

</td><td>

Service option that consists of one or more service commitments that uniquely define the level of service. You can select the different levels of performance and features for a service through service offerings. You must select a service to filter the available service offerings.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the change applies to.

</td></tr><tr><td>

Priority

</td><td>

Priority of this change request.

</td></tr><tr><td>

Risk

</td><td>

Risk level for the change.Select one of the following options:

-   **High**
-   **Moderate**
-   **Low**

</td></tr><tr><td>

Impact

</td><td>

Measure of the effect of a change on the business processes.

</td></tr><tr><td>

Short description

</td><td>

Summary of the change.

</td></tr><tr><td>

Description

</td><td>

Description of the change in detail.

</td></tr><tr><td>

Model

</td><td>

Change model that is associated with the Telecommunications Network Inventory change request. After selecting the change model tile, the associated model appears in this field. You can also manually select one of the following options:

 -   **Add Interface Card**

Change model that is used to add an interface card in an equipment slot.

-   **Create Inventory Equipment**

Change model that is used to add equipment when using an inventory template in a site or equipment holder.

-   **Create Logical Connection**

Change model that is used to create a logical connection between two network interfaces.

-   **Create Physical Connection**

Change model that is used to create a physical connection between two network interfaces.

-   **Emergency**

Change model that is used for the Telecom Network Inventory emergency changes.

-   **GPON Broadband Service**

Change model that is used to fulfill a Gigabyte Passive Optical Network \(GPON\) broadband order request.

-   **Normal**

Change model that is used for the Telecommunications Network Inventory normal changes.


 **Note:** These change models are available in the **Changes** &gt; **All** &gt; **New** window.

</td></tr><tr><td>

State

</td><td>

Current state of this change request, New, or closed.

</td></tr><tr><td>

Assignment group

</td><td>

Group working on the change request.

</td></tr><tr><td>

Assigned to

</td><td>

User that the change is assigned to. If an assignment rule applies, the change is automatically assigned to the appropriate user or group.-   New
-   Design In Progress
-   Design Review
-   Design Complete

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Planned start date|Projected start date for the implementation. The planned start date can be the current date or a future date. The default value for this field is the current date. To change the planned start date, select the calendar icon ![Calendar icon.](../image/calendar-icon.png) and select a new date.|
|Planned end date|Projected end date for the implementation. The planned end date must be after the planned start date. The default value for this field is one day after the planned start date. To change the planned end date, select the calendar icon ![Calendar icon.](../image/calendar-icon.png) and select a new date.|
|CAB required|Option that designates if this change request requires a Change Advisory Board \(CAB\) approval before implementation.|
|CAB date|CAB approval date for the implementation.|
|Actual start date|Actual start date for the implementation. The actual start date can be on or before the planned start date.|
|Actual end date|Actual end date for the implementation. The actual end date can be before the planned start date but not before the actual start date.|
|CAB delegate|User who attends the Change Advisory Board \(CAB\) meeting to describe the change.|
|CAB recommendation|Notes or recommendations that are related to the CAB meeting.|

|Field|Description|
|-----|-----------|
|Watch list|User who gets the notifications about the change request. Add the names of the users who receive notifications and can view the watch topic.|
|Additional comments \(Customer visible\)|Option that designates if the work notes need to be shared with the user who requested the change.|
|Work notes|Work notes for the change request.|
|Work notes list|Users who can get the notification about the work notes.|

<table id="table_bf4_xqp_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Close code

</td><td>

Close code that best describes the reason you’re closing this change request. Select one of the following options:-   **Successful**
-   **Unsuccessful with issues**
-   **Unsuccessful**

</td></tr><tr><td>

Close notes

</td><td>

Any additional notes that describe the outcome of closing this change request.

</td></tr></tbody>
</table><table id="table_ubz_xqp_wxb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Change task identification number.

</td></tr><tr><td>

Change request

</td><td>

Change request number under which this change task was created.

</td></tr><tr><td>

Configuration item

</td><td>

Configuration item \(CI\) that the change is applied to.

</td></tr><tr><td>

Request type

</td><td>

Request type. Depending on your selection, the record producer form under the task attributes gets updated. This field represents the type of change request. Select any one of the following:-   **Revise CI**

This type of request definition enables you to select a CI that you want to revise and clones the selected CI details and related items. The **Configuration item** field is automatically updated with the cloned CI name having suffix as revised.

All the changes made to the CI are now applied to the cloned CI. Also, both original and duplicated CIs can be found under **Affected CIs** tab. To customize the cloning process, see [../task/clone-and-revise-a-ci.md](../task/clone-and-revise-a-ci.md).

-   **Add cable**

This type of request definition enables you to create a cable record.

-   **Add Card**

This type of request definition enables you to select a site and equipment model when you add interface cards. To learn more about equipment instantiation, see [Design and assign](telecommunications-circuit-design-resource-assignment.md).

-   **Create equipment**

This type of request definition enables you to select a network site and an inventory template for equipment instantiation. If you want to place your equipment inside a rack, you can select an equipment holder.

-   **Create Physical Connection and Create Logical Connection**

These types of request definitions have similar sets of site and equipment selection fields for the physical or logical connections between your start \(A\) and end \(Z\) locations. You can only select those interfaces that are associated with the designated equipment model for the A-start and Z-end interfaces.

For the instantiation of physical or logical connections, you must select a physical connection model or a logical connection model, depending on the type of connection that you want to create between the two sites. For a logical connection, this internal code creates a CI record, and additional path elements.

-   **Logical connection - Path compute**

This type of request definition has a set of site and equipment fields for start and end locations.

For initiation of the path compute of the logical connection, you must select logical connection model. To learn more, see [Compute and Create Logical Connection form](../reference/compute-and-create-logical-connection-form.md).

-   **Modify members of a topology**

This type of request definition enables you to create a cable record. o learn more about modifying a network topology record, see [Add or remove a member to network topology record](../task/modify-network-topology-record-design-assign.md).

-   **IP Address Allocation**

This type of request definition enables you to instantiate an IP address allocation and assign new services to the IP addresses. To learn more, see IP address allocation form in [Change request and change task forms](change_request_forms.md).

-   **Phone Number Allocation**

This type of request definition enables you to instantiate a phone number allocation. You can allocate, de-allocate, and create numbers that are provided externally. To learn more, see the Manage phone number form in [Change request and change task forms](change_request_forms.md).


</td></tr><tr><td>

Short description

</td><td>

Short description for this order task.

</td></tr><tr><td>

Description

</td><td>

Description of this order task.

</td></tr><tr><td>

State

</td><td>

State of this change task. Select one of the following options:-   **Pending**

Task is waiting for an action from the user.

-   **Open**

No action is taken on this task yet.

-   **In Progress**

Task processing is in progress.

-   **Closed**

Change task is complete.

-   **Canceled**

Change task has been canceled.


</td></tr><tr><td>

Assignment group

</td><td>

Name of the group that is responsible for this task. Select the search icon \(![Search icon.](../image/search.png)\) to select a group from the list.

</td></tr><tr><td>

Assigned to

</td><td>

Depending on the selected group, the users who are assigned to the list are shown. Select the search icon \(![Search icon.](../image/search.png)\) to see the list of users.

</td></tr><tr><td>

Work notes

</td><td>

Free-form work order note text.

</td></tr><tr><td>

Update

</td><td>

Option to save changes that you made to the order task.

</td></tr><tr><td>

Close Task

</td><td>

Option to change the state of the order task to **Closed**.

</td></tr><tr><td>

Delete

</td><td>

Option to delete this order task.

</td></tr></tbody>
</table><table id="table_tsw_yl4_ktb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Inventory template

</td><td>

Name of the inventory template for the equipment model. The instantiation process uses it to generate a network asset instance in the designated network site.**Note:**

-   Depending on the selected inventory template, a list of the optional templates appears at the bottom of the form.
-   When you select an optional template, the current template values are overwritten.
-   This field is applicable only for Create inventory equipment.

</td></tr><tr><td>

Equipment holder

</td><td>

Name of the telco equipment holder. Select a rack or a cabinet where the equipment can be installed.**Note:**

-   The **Telco equipment holder** field lists all racks and cabinets.
-   This field is applicable only for Create inventory equipment.

</td></tr><tr><td>

Network site

</td><td>

Name of the network site in which the process is instantiating the equipment.

</td></tr><tr><td>

Rack/Cabinet template

</td><td>

Template name of the rack template where you want to add all the slots to.

**Note:**

-   Based on the selected **Rack template**, **Stockroom location**, and **Asset** the slots, network sites, and related network sites are added.
-   This field is applicable only for Create rack.

</td></tr><tr><td>

Stockroom Location

</td><td>

Name of the stockroom location where the asset is located.

 To learn more, see [Telecommunications Network Inventory integration with Hardware Asset Management](integration-with-hardware-asset-management.md).

</td></tr><tr><td>

Asset

</td><td>

Name of the asset that is associated with this record.

 To learn more, see [Telecommunications Network Inventory integration with Hardware Asset Management](integration-with-hardware-asset-management.md).

</td></tr></tbody>
</table><table id="table_z1z_g4v_4xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation Type

</td><td>

Type of operation. Select one of the following options:-   **Create IP network subnet**: Creates a network subnet with a CIDR value.

**Note:** For the IP network subnet creation, the Create IP Subnetwork flow action is initiated. To learn more, see [Create IP subnetwork function](create_ip_subnetwork.md).

-   **Convert CIDR to IP addresses**: Converts a single or multiple CIDRs to IP addresses and stores them in an IP address allocation.

**Note:** For the CIDR-to-IP address conversion, the CIDR-to-IP range flow action is initiated. To learn more, see [CIDR to IP range function](cidr_to_ip_range.md).


</td></tr><tr><td>

Name

</td><td>

Name for this IP allocation.

</td></tr><tr><td>

IP pool

</td><td>

Parent pool of this IP address allocation.

</td></tr><tr><td>

IP network subnet CIDR

</td><td>

CIDR value.

</td></tr><tr><td>

Managed Network

</td><td>

IP address or allocation that you can select and assign a network to.

</td></tr><tr><td>

Owned by configuration item

</td><td>

Configuration item that owns this allocation.

</td></tr><tr><td>

IP network subnet

</td><td>

Network subnet that you searched for and selected to convert its CIDR-to-IP addresses. **Note:** This field is used only for converting the CIDR-to-IP address.

</td></tr></tbody>
</table><table id="table_rgv_w4f_4xb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Action that you can select:-   **Allocate**: Allocates the numbers from a block
-   **De-allocate**: De-allocates the numbers. The status of the numbers is changed to Quarantine.

**Note:** When you select this action, you must select an allocation or the selected numbers that you want to deallocate. This action results in changing the status to Quarantine.

-   **Ported-in**: Includes the numbers that are moved from another operator. The numbers are stored in a telephone number allocation of telephone numbers only.

**Note:** Multiple allocations get created if the numbers aren’t in a series of numbers. Also, by default, the numbers are changed to the assigned or the ported-in status.

-   **Create**: Creates the phone number allocation for the numbers that are assigned to an external telephone block. You’re assigning the numbers to a network inventory-based phone number allocation.

</td></tr><tr><td>

Service

</td><td>

Service for these numbers. The selected service gets assigned to the numbers.**Note:** Ensure that you’ve created a service for this phone number. To learn more, see [Manage your network functions](services.md).

</td></tr><tr><td>

Quantity

</td><td>

Total number of required phone numbers.**Note:** This field disappears for a deallocated action.

</td></tr><tr><td>

Phone number allocation

</td><td>

Available number allocations that are based on the provided information that you enter. You can select a phone number allocation for your line number.

</td></tr><tr><td>

Line number

</td><td>

Enter your required line number in xxxx-xxxx or xxx-xxx or xxx, xxx-xxx format.**Note:** Multiple telephone number allocations are created if the line number isn’t in a series of numbers. Also, the status of these numbers gets updated to either assigned or ported-in and the availability is No.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](telecommunications-network-inventory-reference.md)

**Related topics**  


[Instantiating inventory using design and assign](instantiate-asset-using-template-relationship-model.md)

