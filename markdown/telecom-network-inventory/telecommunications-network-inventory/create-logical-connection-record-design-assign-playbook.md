---
title: Create a logical connection record using the Design and Assign function
description: Use the Design and Assign function to create a logical connection in the Telecommunications Network Inventory application. By creating a logical connection, you can fulfill the design request for a network service.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Design and Assign function, Use, Telecommunications Network Inventory]
---

# Create a logical connection record using the Design and Assign function

Use the Design and Assign function to create a logical connection in the Telecommunications Network Inventory application. By creating a logical connection, you can fulfill the design request for a network service.

## Before you begin

Define the inventory records, models, model relationships, templates, and template relationships for your design criteria.

Role required: sn\_ni\_core.inventory\_agent, sn\_ni\_core.network\_planning\_manager

## About this task

The Design and Assign home page lists the change requests that are in the Design in progress state. You can either select a change request from the list or create a change request to design a logical connection depending on your requirement. Completion of each activity in the playbook for the Design and Assign function creates a change task for the next activity.

After you complete each activity, the network diagram updates and displays the data. You can review the network diagram for any incompleteness and update the activities accordingly.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the design and assign icon \(![Design and Assign Icon](../image/icon-design-assign.png)\).

    The Design and Assign home page is displayed.

3.  Select **New** &gt; **Create Logical Connection**.

    A change request is created with **Design in progress** and the Design and Assign window is displayed.

4.  On the **Setup request details** card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Number|Change request number is automatically generated to instantiate a logical connection with the Design in progress state.|
    |Category|Category of this change request. Select Other if your category isn’t in the list.|
    |Priority|Priority of this change request.|
    |Short description|Summary of the design.|
    |Description|Description of the design in detail.|

5.  Select **Mark complete**.

6.  On the **Setup logical connection** card, fill in the fields.

<table id="table_g5t_gg2_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Logical connection model

</td><td>

Logical connection model where this logical connection is configured.

</td></tr><tr><td>

Bandwidth

</td><td>

Bandwidth for this logical connection. Only bandwidths compatible with the logical connection model are listed here.**Note:** Lists all bandwidths if no compatible bandwidth is available.

</td></tr><tr><td>

Network domain

</td><td>

Domain of ownership and responsibility for this network asset or connection. Select one of the following options:-   **Mobility**

Network asset that is associated with the mobility equipment domain.

-   **Telco**

Network asset that is associated with the telco equipment domain.

-   **Core**

Network asset that is associated with the core equipment domain.

</td></tr><tr><td>

Logical connection template

</td><td>

List of all templates based on the selected logical connection model.

</td></tr></tbody>
</table>7.  Select **Mark complete**.

8.  On the **Define end points** card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Start site|Originating network site for this connection.|
    |Start equipment|Originating equipment for this connection.|
    |Start interface|Originating network interface for this connection.|
    |End site|Destination network site for this connection.|
    |End equipment|Destination equipment for this connection.|
    |End interface|Destination network interface for this connection.|

9.  Select **Mark complete**.

10. On the **Assign connection element** card, select **Add** and fill in the fields to select the connection element.

    To skip this activity, select **Skip**.

<table id="table_qth_hg2_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Element type

</td><td>

Type of connection element. Select one from the list.-   Network Interface
-   Physical Connection
-   Logical Connection
-   Equipment
-   Topology


</td></tr><tr><td>

Element name

</td><td>

Connection element based on the event type that you're selected. By selecting the connection element, the Available capacity and Used capacity fields displays the capacity information of the connection element.

</td></tr><tr><td>

Model

</td><td>

Model where this connection element is configured.Only compatible models based on the model relationship are displayed.

</td></tr><tr><td>

Start Site

</td><td>

Originating network site for this connection element.**Note:** This field is available for Physical Connection and Logical Connection element types.

</td></tr><tr><td>

End Site

</td><td>

Destination network site for this connection element.**Note:** This field is available only for Physical Connection and Logical Connection element types.

</td></tr><tr><td>

Start equipment

</td><td>

Originating equipment for this connection element.**Note:** This field is available only for Physical Connection and Logical Connection element types.

</td></tr><tr><td>

End equipment

</td><td>

Destination equipment for this connection element.**Note:** This field is available only for Physical Connection and Logical Connection element types.

</td></tr><tr><td>

Route

</td><td>

Number of routes.

</td></tr><tr><td>

Sequence

</td><td>

Number of sequences.

</td></tr></tbody>
</table>11. Select **Mark complete**.

12. On the **Assign protection element** card, select **Add** and fill in the fields to select the protection element.

    To skip this step, select **Skip**.

    |Field|Description|
    |-----|-----------|
    |Start Site|Originating network site for this protection path.|
    |Start equipment|Originating equipment for this protection path.|
    |Model|Model where this protection logical connection is configured. Only compatible models based on the model relationship are displayed.|
    |End Site|Destination network site for this protection path.|
    |End equipment|Destination equipment for this protection path.|
    |Protecting logical connection|Logical connection that acts as redundancy path.|

13. Select **Mark complete**.

14. On the **Define number element** card, select **Add** and fill in the fields to select the number element.

    To skip this step, select **Skip**.

<table id="table_t5p_th2_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owned by configuration item

</td><td>

Configuration item \(CI\) that is related to the Inventory number record.

</td></tr><tr><td>

Parent number type

</td><td>

Type of inventory number parent record belongs to. Select one from the following.-   LAG
-   LAG Range
-   VLAN
-   VLAN range


</td></tr><tr><td>

Parent number range

</td><td>

Range of parent number.

</td></tr><tr><td>

Number Type

</td><td>

Type of inventory number this network inventory belongs to. Select one from the following.-   LAG
-   LAG Range
-   VLAN
-   VLAN range


</td></tr><tr><td>

Number

</td><td>

Unassigned numbers are displayed here, and you can select multiple ones.

</td></tr></tbody>
</table>15. Select **Mark complete**.

16. On the **Define IP address** card, select **Add** and fill in the fields to select the IP address.

    To skip this step, select **Skip**.

    |Field|Description|
    |-----|-----------|
    |IP pool|Parent pool of this IP address allocation.|
    |IP sub network|IP network subnet of this IP address allocation.|
    |Allocated IP address|Select the allocated IP addresses.|

17. Select **Mark complete**.

18. On the **Set attributes** card, select **Add** and fill in the fields to select the connection element.

    If you want to skip this step, select **Skip**.

<table id="table_z44_f32_ndc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name of the logical connection record. Add connection name, otherwise default name is added

</td></tr><tr><td>

Life cycle stage

</td><td>

Stage of the life cycle that this network asset is in:

-   **Deploy**

Network asset that is deployed in your network.

-   **Design**

Network asset that is being used for design purposes.

-   **End of life**

Network asset that is at the end of its useful life.

-   **Inventory**

Network asset that is an inventory item in use in the network.

-   **End of life**

Network asset that is missing and can't be located.

-   **Operational**

Network asset that is operational.

-   **Purchase**

Network asset that is in the purchase phase of its life.

</td></tr><tr><td>

Life cycle stage status

</td><td>

Status of the network asset as it relates to the life cycle stage that it is in:

-   **In Maintenance**

Network asset that is currently in maintenance.

-   **In Use**

Network asset that is currently in use.

-   **Pending Retirement**

Network asset that is currently in maintenance.

</td></tr><tr><td>

Supported by

</td><td>

Name of the person who supports this network asset.

</td></tr><tr><td>

Supported by group

</td><td>

Group that supports the network inventory.

</td></tr><tr><td>

Comments \(Customer visible\)

</td><td>

Any comments.

</td></tr><tr><td>

Operational notes

</td><td>

Free-form operation note text for this network asset. For example, `Check diesel fuel for generator`.

</td></tr></tbody>
</table>19. On the **Review and submit** card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Notes|Any additional notes.|

20. Select **Submit**.


## Result

The change tasks are created and executed for each activity. The logical connection record is created with the associated Configuration items \(CI\).

**Parent Topic:**[Design and Assign function](../concept/using-playbooks-design-assign-inventory-record.md)

**Related topics**  


[Logical connections](../concept/design-logical-connection-design-assign-playbook.md)

