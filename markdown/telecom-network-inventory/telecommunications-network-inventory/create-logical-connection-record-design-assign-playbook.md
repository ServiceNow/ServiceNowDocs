---
title: Create a logical connection record using the Design and Assign function
description: Use the Design and Assign function to create a logical connection in the Telecommunications Network Inventory application. By creating a logical connection, you can fulfill the design request for a network service.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
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

    1.  Select the design and assign icon \(![Design and Assign Icon](../image/icon-design-assign.png)\).

        The Design and Assign home page is displayed.

    2.  Select **New** &gt; **Create Logical Connection**

        A change request is created in Design in progress state. The Design and Assign window is displayed.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Number|The change request number that is automatically generated to instantiate a logical connection with the Design in progress state.|
        |Category|Category of this change request. Select **Other** if your category isn’t in the list.|
        |Priority|Priority of this change request.|
        |Short description|Summary of the design.|
        |Description|Description of the design in detail.|

    4.  Select **Mark complete**.

2.  Set up the logical connection card.

    1.  On the Setup logical connection card, fill in the fields.

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

Bandwidth for this logical connection. Only bandwidths compatible with the logical connection model are listed here.**Note:** This field lists all bandwidths if no compatible bandwidth is available.

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
</table>    2.  Select **Mark complete**.

3.  Define the end points.

    1.  On the Define end points card, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Start site|Originating network site for this connection.|
        |Start equipment|Originating equipment for this connection.|
        |Start interface|Originating network interface for this connection.|
        |End site|Destination network site for this connection.|
        |End equipment|Destination equipment for this connection.|
        |End interface|Destination network interface for this connection.|

    2.  Select **Mark complete**.

4.  Assign the connection element.

    **Note:** To skip this activity, select **Skip**.

    1.  On the Assign connection element card, select **Add**.

    2.  On the Assign connection element form, fill in the fields.

        To learn more about fields, see [Assign connection element form](../reference/assign-connection-element.md).

    3.  Select **Mark complete**

5.  Assign a protection element.

    **Note:** To skip this step, select **Skip**.

    1.  On the Assign protection element card, select **Add**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Start Site|Originating network site for this protection path.|
        |Start equipment|Originating equipment for this protection path.|
        |Model|Model where this protection logical connection is configured. Only compatible models based on the model relationship are displayed.|
        |End Site|Destination network site for this protection path.|
        |End equipment|Destination equipment for this protection path.|
        |Protecting logical connection|Logical connection that acts as redundancy path.|

    3.  Select **Mark complete**.

6.  Define the number element.

    **Note:** To skip this step, select **Skip**.

    1.  On the Define number element card, select **Add**.

    2.  On the form, fill in the fields.

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
</table>    3.  Select **Mark complete**.

7.  Define the IP address.

    **Note:** To skip this step, select **Skip**.

    1.  On the Define IP address card, select **Add**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |IP pool|Parent pool of this IP address allocation.|
        |IP sub network|IP network subnet of this IP address allocation.|
        |Allocated IP address|Select the allocated IP addresses.|

    3.  Select **Mark complete**.

8.  Set the attributes.

    **Note:** If you want to skip this step, select **Skip**.

    1.  On the Set attributes card, select **Add**.

    2.  On the attribute form, fill in the fields.

        To learn more about fields, see [Attribute form](../reference/attribute-form.md)

9.  On the Review and submit card, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Notes|Any additional notes.|

10. Select **Submit**.


## Result

The change tasks are created and executed for each activity. The logical connection record is created. The created logical connection automatically associates the interface with its corresponding card or equipment.

**Note:**

The system now automatically associates each logical interface with its corresponding card or equipment. With the logical and physical interface alignment enhancement, logical interfaces \(such as VLANs\) and physical interfaces \(such as Gigabyte Ethernet ports\) are mapped to their parent equipment or card. The system establishes a parent relationship for each logical interface using the parent’s unique serial number for accurate identification. This enhancement ensures consistency across systems and prevents duplicate CI creation by aligning identification and relationship logic between logical and physical interfaces.

**Parent Topic:**[Design and Assign function](../concept/using-playbooks-design-assign-inventory-record.md)

**Related topics**  


[Logical connections](../concept/design-logical-connection-design-assign-playbook.md)

