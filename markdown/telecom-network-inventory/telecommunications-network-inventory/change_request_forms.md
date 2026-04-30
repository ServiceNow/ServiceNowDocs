---
title: Change request and change task forms
description: The change request forms enable you to request a change.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 25
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
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

-   To update or revise a logical connection CI, see [Revise a configuration item](revise-a-configuration-item.md).
-   To modify logical connection endpoints, see [Create a change request by using the modify logical connection endpoints model](../task/create-a-change-request-by-using-modify-logical-connection-endpoints-model.md).

</td></tr><tr><td>

Create physical connection

</td><td>

Change model to create a change request for creating a physical connection. To learn more, see [Change request and change task forms](change_request_forms.md).**Note:**

-   To update or revise a physical connection CI, see [Revise a configuration item](revise-a-configuration-item.md).
-   To modify physical connection endpoints, see [Create a change request by using modify physical connection](../task/create-a-change-request-by-using-modify-physical-connection.md).

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

<table id="table_bqz_nww_wxb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Due date

</td><td>

Planned end date for this request.

</td></tr><tr><td>

Site A

</td><td>

Text field where you can select a source site.

</td></tr><tr><td>

Equipment A

</td><td>

Text field where you can select the source equipment.**Note:** The list is dependent on the site A that you've selected.

</td></tr><tr><td>

Interface A

</td><td>

Text field where you can select a source interface.**Note:**

-   The list is dependent on the equipment that you selected.
-   The list doesn’t display the interfaces that are marked as virtual.

</td></tr><tr><td>

Bandwidth

</td><td>

Text field where you can select a total bandwidth that transmits between the source and destination interfaces.

</td></tr><tr><td>

Start date

</td><td>

Planned start date for this request.

</td></tr><tr><td>

Site Z

</td><td>

Text field where you can select a destination site.

</td></tr><tr><td>

Equipment Z

</td><td>

Text field where you can select the destination equipment.

</td></tr><tr><td>

Interface Z

</td><td>

Text field where you can select a destination interface.**Note:** The interface Z list doesn’t display the interfaces that are marked as virtual.

</td></tr></tbody>
</table><table id="table_kcb_vqp_wxb"><thead><tr><th>

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

User that the change is assigned to. If an assignment rule applies, the change is automatically assigned to the appropriate user or group.

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

This type of request definition enables you to select a site and equipment model when you add interface cards. To learn more about equipment instantiation, see [Telecommunications design and assign](telecommunications-circuit-design-resource-assignment.md).

-   **Create equipment**

This type of request definition enables you to select a network site and an inventory template for equipment instantiation. If you want to place your equipment inside a rack, you can select an equipment holder.

-   **Create Physical Connection and Create Logical Connection**

These types of request definitions have similar sets of site and equipment selection fields for the physical or logical connections between your start \(A\) and end \(Z\) locations. You can only select those interfaces that are associated with the designated equipment model for the A-start and Z-end interfaces.

For the instantiation of physical or logical connections, you must select a physical connection model or a logical connection model, depending on the type of connection that you want to create between the two sites. For a logical connection, this internal code creates a CI record, and additional path elements.

-   **Logical connection - Path compute**

This type of request definition has a set of site and equipment fields for start and end locations.

For initiation of the path compute of the logical connection, you must select logical connection model. To learn more, see [Compute and Create Logical Connection form](../reference/compute-and-create-logical-connection-form.md).

-   **Modify members of a topology**

This type of request definition enables you to create a cable record. o learn more about modifying a network topology record, see [Modify a network topology record using design and assign](../task/modify-network-topology-record-design-assign.md).

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
</table><table id="table_o34_kwt_xxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Site

</td><td>

Site where you want to install this card.

</td></tr><tr><td>

Equipment

</td><td>

Equipment to install this card in.

</td></tr><tr><td>

Slot

</td><td>

Slot to insert this card in.

</td></tr><tr><td>

Template

</td><td>

Select a template for this card.

</td></tr><tr><td>

Stockroom location

</td><td>

Name of the stockroom location where the asset is located. To learn more, see [Telecommunications Network Inventory integration with Hardware Asset Management](integration-with-hardware-asset-management.md).

</td></tr><tr><td>

Asset

</td><td>

Name of the asset that is associated with this record. To learn more, see [Telecommunications Network Inventory integration with Hardware Asset Management](integration-with-hardware-asset-management.md).

</td></tr><tr><td>

Slot Span

</td><td>

Multiple slot selector to select multiple slots if it's required for the selected card. This field is displayed based on the selected template.**Note:** The list only shows the list of slots and sub-slots that doesn't have any card in it.

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

Service for these numbers. The selected service gets assigned to the numbers.**Note:** Ensure that you’ve created a service for this phone number. To learn more, see [Create xNF and xNF instances](services.md).

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
</table><table id="table_fwy_4xr_jzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the topology.

</td></tr><tr><td>

Topology model

</td><td>

Inventory model associated with the topology.

</td></tr><tr><td>

Bandwidth

</td><td>

Bandwidth of the topology.

</td></tr><tr><td>

Topology sites

</td><td>

Site associated with the topology. You can select multiple sites.

</td></tr><tr><td>

Topology nodes

</td><td>

Equipment \(node\) associated with the topology. You can select multiple nodes.

</td></tr><tr><td>

Root nodes

</td><td>

Root node among the topology nodes.

</td></tr><tr><td>

Topology connection type

</td><td>

Type of connection. Select one from the following:

-   **Logical Connection**
-   **Physical connection**

</td></tr><tr><td>

Topology connections

</td><td>

Connections that are associated with the topology. You can select multiple connection records.

</td></tr></tbody>
</table><table id="table_pfp_c42_nzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logical Connection Model

</td><td>

Logical connection model where this logical connection is configured.**Note:** The topology connection models are not listed if you are creating a logical connection in a change request.

</td></tr><tr><td>

Physical Connection Model

</td><td>

Physical connection model where this physical connection is configured.

</td></tr><tr><td>

Logical Connection Template

</td><td>

List of all templates based on the selected logical connection model.

</td></tr><tr><td>

Bandwidth AtoZ

</td><td>

Total bandwidth capacity from Site A to Site Z for this network connection.

</td></tr><tr><td>

Bandwidth ZtoA

</td><td>

Total bandwidth capacity from Site A to Site Z for this network connection.

</td></tr><tr><td>

A end Site

</td><td>

Starting network site where this logical connection is configured.

</td></tr><tr><td>

Z end Site

</td><td>

Ending network site where this logical connection is configured.

</td></tr><tr><td>

A end Equipment

</td><td>

Starting network equipment where this logical connection is configured.

</td></tr><tr><td>

Z end Equipment

</td><td>

Ending network equipment where this logical connection is configured.

</td></tr><tr><td>

Parent Port A

</td><td>

Network interface on which the new logical interface is representing the **Port A** of the connection.**Note:** A new logical interface is created by default based on the selected logical/physical connection model and is populated in the port A field under **Configuration** section of the logical or physical connection. The logical interface indicates the port name and number of child ports plus one of the selected port.

</td></tr><tr><td>

Parent Port Z

</td><td>

Network interface on which new logical interface is representing the **Port Z** of the connection.**Note:** A new logical interface is created by default based on the selected logical/physical connection model and is populated in the port Z field under **Configuration** section logical or physical connection. The logical interface indicates the port name and number of child ports plus one of the selected ports.

</td></tr><tr><td>

Move Overlaying Connections

</td><td>

Option to move all dependant connections of modified connection from the current Interface to the new interface. You can also update the logical connections manually by deselecting this check box.**Note:** This field is applicable only for the Modify physical connection endpoints model.

</td></tr></tbody>
</table><table id="table_fzh_ksr_nzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A end Site

</td><td>

Starting network \(Site A field\) site where this selected logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end Site

</td><td>

Ending network site \(Site Z field\) where this selected logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

A end Equipment

</td><td>

Starting network \(Site A field\) equipment where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end Equipment

</td><td>

Ending network \(Site Z field\) equipment where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

A end interface

</td><td>

Starting interface \(Site A field\) point where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Z end interface

</td><td>

Ending interface \(Site Z field\) point where this logical or physical connection is configured.**Note:** This field is auto populated based on the selected site or equipment or interface or connection.

</td></tr><tr><td>

Logical Connection

</td><td>

Select a logical connection from the list that needs modification.**Note:**

-   The list includes both logical connection and their revisions. On selecting the revision of a logical connection, the **Create Revision** check box disappears.
-   This field is auto populated based on the selected site or equipment or interface.

</td></tr><tr><td>

Physical Connection

</td><td>

Select a physical connection that needs modification from the list.**Note:**

-   The list includes both physical and their revisions. On selecting the revision of a physical connection, the **Create Revision** check box disappears.
-   This field is applicable only for physical connection modification form.
-   This field is auto populated based on the selected site or equipment or interface.

</td></tr><tr><td>

Create Revision

</td><td>

Option to enable or disable revision process.**Note:**

1.  On selecting this check box, the following occurs:
    1.  The revision process is initiated. To learn more, see [Revision, operationalization, and decommission of a Configuration Item](revision-of-a-confiuguration-item.md).
    2.  Two change tasks for modification and revision are created with the open and closed status respectively.
2.  Open the Modify Logical or Physical connection change task to start modifying the duplicated logical or physical connection and operationalize further. To learn more, see [Operationalize a configuration item](../task/operationalize-a-configuration-item.md).
3.  In the process of revision of physical connection modification, the logical connections associated with physical connection ports are updated during the operationalization process.

</td></tr></tbody>
</table><table id="table_otz_tnj_pzb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Network Site

</td><td>

Network site that contains the equipment or shelf that you want to add or remove.**Note:**

-   This field is applicable only for add equipment to a rack and remove equipment or shelf from a rack.
-   The list only displays the sites that have a rack in it.

</td></tr><tr><td>

Rack/Cabinet

</td><td>

Rack name for the equipment or shelf you want to add or remove.**Note:** This field is applicable only for adding equipment to a rack or a cabinet and removing equipment from a rack or cabinet.

</td></tr><tr><td>

Equipment / Shelf

</td><td>

Equipment or shelf to add or remove from the selected rack or cabinet.**Note:** This field is applicable only for adding equipment to a rack or cabinet and removing equipment or shelf from a rack or cabinet.

</td></tr><tr><td>

Available RUs

</td><td>

List of available rack units to place the selected equipment.**Note:**

-   The list is also based on the selected equipment's RUs.
-   This field is displayed while editing and adding equipment to a rack.

</td></tr><tr><td>

Front View

</td><td>

Front view for the selected rack or cabinet. By default, this is selected as **Yes**.**Note:**

-   Selecting **No** the equipment is placed in rear view.
-   Equipment can be mounted in a rack unit, taking up either the entire front unit or half of it.

</td></tr><tr><td>

Exclusively Used

</td><td>

By default, it is selected as **Yes**. Select **No** if you want to use the rack unit for multiple pieces of equipment. Also, on not selecting this field, you can place equipments in both the front and rear sides of the rack.**Note:**

-   On selecting yes, the selected equipment occupies both front and rear of rack units.
-   You can place multiple pieces of equipment only on a **Shelf** equipment holder type. To learn more, see [df4a7f81d9dcef27d876faa3c642b4657c3b9487.dita](../task/define-tni-equipment-holders.md).

</td></tr><tr><td>

Rack Slot

</td><td>

List of rack units that are available for the selected equipment to be mounted.**Note:**

-   The rack units for the selected equipment are automatically populated based on the **Height \(U\)** field of the model. For instance, if the field indicates that the selected equipment requires two rack units, then even though only one rack unit, RU-10, is explicitly selected, the system will automatically reserve both RU-10 and RU-11 to accommodate the equipment.
-   Make sure to select continuous rack units for an equipment.
-   If the **Height\(U\)** field is left empty, the rack slots specified here are used instead.
-   If a rack is linked to multiple network model relationships, the total number of rack slots allocated to the rack is determined by adding up the **Count** values provided for each model relationship.
-   To modify the number of rack slots, adjust the associated **Count** value and manage the excess slots accordingly. Rack slot creation and removal are unrestricted when the rack slot count is undefined.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](telecommunications-network-inventory-reference.md)

**Related topics**  


[Instantiating your network inventory by using design and assign](instantiate-asset-using-template-relationship-model.md)

