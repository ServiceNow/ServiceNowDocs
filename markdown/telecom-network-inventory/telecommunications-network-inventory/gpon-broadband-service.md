---
title: Designing and assigning a GPON broadband service
description: With the Gigabyte Passive Optical Network \(GPON\) Broadband Service change model, you can create an automated set of tasks to fulfill a GPON broadband order request.Needs review and comment by Jijesh.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Telecommunications Network Inventory reference, Telecommunications Network Inventory]
---

# Designing and assigning a GPON broadband service

With the Gigabyte Passive Optical Network \(GPON\) Broadband Service change model, you can create an automated set of tasks to fulfill a GPON broadband order request.

## GPON Broadband Service overview

As a product manager, you can use the GPON Broadband Service change model to design and allocate your inventory for GPON broadband services. With this model, you can fulfill your customer orders and requests for your network expansion.

## Change execution process for GPON Broadband Service request

The change request execution process includes the task stages that you need to complete for the GPON Broadband Service request. You must do these task stages in the following sequence to successfully complete the request.

-   **Create the change request**

    Create the change request by using the GPON Broadband Service change model. To learn more, see [Create and execute a change task in Telecommunications Network Inventory](../task/create-change-task-in-tni.md). .

-   **Path compute and create logical connection**

    Identify the possible paths between the network sites and create a logical connection between each site. To learn more, see the next section in this topic called "Path computation for the GPON Broadband Service change model."

-   **Create a logical connection**

    Add similar sets of site selection fields for the physical and logical connections between your start \(A\) and end \(Z\) locations. You can only select those interfaces that are associated with the designated equipment model for the A- and Z-end interfaces. To learn more, see [Change request and change task forms](change_request_forms.md) .

-   **Create a physical connection**

    Add similar sets of site selection fields for the physical and logical connections between your start \(A\) and end \(Z\) locations to configure your inventory equipment. You can only select those interfaces that are associated with the designated equipment model for the A- and Z-end interfaces. To learn more, see the next section in this topic called "Path computation for the GPON Broadband Service change model."

-   **Add an interface card**

    Select a site and equipment model when you add interface cards. Use the **Slot** field to select the slot that you want to add to the equipment model. To learn more, see [Change request and change task forms](change_request_forms.md).

-   **Create equipment**

    Select a network site and equipment model for your equipment instantiation. The instantiation process is when you generate and validate the equipment records at the site level. To learn more, see [Change request and change task forms](change_request_forms.md) and [Change request and change task forms](change_request_forms.md).


After you complete this sequence, you can complete the design and assign procedure for the GPON broadband services.

To execute this process successfully, you need to consider a set of conditions as well as scenarios. To learn more, see the next section in this topic called "Path computation for the GPON Broadband Service change model.".

## Path computation for the GPON Broadband Service change model

An internal path computation function is part of the GPON Broadband Service change model. Its purpose is to identify the possible paths between your network sites. This computation is based on the parameters that you enter when you complete each change task that is associated with the GPON Broadband Service change model.

When you create the change request with the GPON Broadband Service change model and save the request, five default change tasks are created. To learn more, see [Design your GPON Broadband Service](../task/gpon-broadband-change-model.md).

The following scenarios are handled in the path computation when you execute the process to complete the GPON broadband service request:

-   When all physical connections are available, the Passive Optical Network \(PON\) access path is created.
-   If the physical connection between the splitter and PFP is used, the PON access path fails.
-   If all physical connections are available, the PON network path is created.
-   If a physical connection between OLT and FDP is used, the PON network path creation fails.
-   If all logical connections are shared, the VLAN path search can create the connection.
-   If a link aggregation group \(LAG\) path is used, the VLAN path search fails.

The path computation uses record producers in each change task that is associated with the GPON Broadband Service change model to collect the required data. It collects most of its connection data when you complete the Compute and Create logical connection change task that you created from a GPON Broadband Service change model.

1.  The path search is between the equipment model that you specified for the A connection end of the connection and the equipment model that you specified in the Z end connection.
2.  The path search is between the equipment model that you specified for the A connection end of the connection and the equipment type that you specified in the Z end connection.
    -   The logical connection model indicates what model of logical connection must be created after the path computation.
    -   The bandwidth refers to the bandwidth table.
    -   The allowed physical connection model captures the physical connection CI model, which can be used to find a path and is added in the path element.

The path computation works on the following conditions:

1.  The equipment hierarchy up to the interface has a **Contains:: Contained By** relationship that is updated when you instantiate the piece of equipment by using the Create Inventory Equipment change model.
2.  The equipment is related to the network site. This condition is also enforced when you instantiate the piece of equipment by using the Create Inventory Equipment change model.
3.  The physical connection that you create between the interfaces is associated with valid models.
4.  When you create a physical connection by using the Create Physical Connection change model, a CI relationship is created between the sites.
5.  The logical connection that you create between the interfaces is associated with valid models.
6.  When you create a logical connection by using the Create Physical Connection change model, a CI relationship is created between those sites.
7.  Connection elements are added for the logical connections. These elements should be valid physical connections between the sites when the computation performs the path search.
8.  Port A and Port Z must be populated for the physical and logical connections.
9.  The **Availability** field for the physical and logical connections must be available to qualify those connections as possible underlying paths for routing. This validation ensures that a resource is not used multiple times.

To learn more about errors occur in the path computation, see [Path computation error messages](../reference/path-computation-error.md).

**Parent Topic:**[Telecommunications Network Inventory reference](telecommunications-network-inventory-reference.md)

**Related topics**  


[Design your GPON Broadband Service](../task/gpon-broadband-change-model.md)

