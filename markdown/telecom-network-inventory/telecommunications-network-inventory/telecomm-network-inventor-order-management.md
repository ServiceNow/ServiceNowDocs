---
title: Telecommunications Network Inventory and Order Management for Telecommunications and Media
description: With the Order Management for Telecommunications and Media \(OMT\) application, you can manage all your product and service orders from one place. These product orders are divided into service orders that are further divided into resource orders.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Integrating Telecommunications Network Inventory with other applications, Telecommunications Network Inventory]
---

# Telecommunications Network Inventory and Order Management for Telecommunications and Media

With the Order Management for Telecommunications and Media \(OMT\) application, you can manage all your product and service orders from one place. These product orders are divided into service orders that are further divided into resource orders.

## Introduction to OMT integration

The order workflow generates the order tasks that fulfill the customer-facing service order \(CFS\) and resource-facing service order \(RFS\). Network-related tasks that involve the inventory configuration items \(CIs\), models, and templates, may interact with the Telecommunications Network Inventory application to create network CIs. For all network-related order tasks, you must create a change request in the Telecommunications Network Inventory application.

The following diagram shows the high-level process of managing a service request and detailed workflow of the Telecommunications Network Inventory and Order Management for Telecommunications applications.

![Workflow explaining how TNI and OMT interact with each other to create a network CI.](../image/mmasset0020486-omt-integration.png)

Following are the stages of the workflow:

1.  Orchestration: In this stage, the Order Management for Telecommunications application fulfills the function of order orchestration. It generates resource orders to execute a variety of order-related tasks, encompassing network planning. These resource orders can be initiated by either a service agent or through the TMF 641.
2.  Plan: In this stage, the SPM leverages pre-defined SPM project template to initiate project creation. Subsequently, the SPM utilizes the established integration with the Order Management for Telecommunications to facilitate further project processing.
3.  Procure: In this stage, instantiation of procurement activity for hardware assets to fulfill the request is obtained.
4.  Design Assign: In this stage, the Telecommunications Network Inventory application initiates the following process:
    1.  creates change request that triggers the respective change model based on the analyzed change characteristics.
    2.  creates change tasks based on the change characteristics.
    3.  completes all the tasks through the inventory task flow that includes template sub flow, read flow action, and create flow action. After which required CIs or resources are read or created.
5.  Build: In this stage, the service is physically built or implemented through FSM.
6.  Activate: The service is deployed using activation procedure.

To create a network CI, the Telecommunications Network Inventory and Order Management for Telecommunications applications are integrated to perform service or product tasks, such as design and assign. A change request is initiated for the tasks that need a network inventory-related action.

You must ensure that these conditions are met:

1.  You must have the license of both the Telecommunications Network Inventory and Order Management for Telecommunications applications in the same instance.
2.  In this integration, only the ADD action service order request from Order Management for Telecommunications and Media is provided.

## For admins

To create a change request, an admin must perform the following tasks for an order task that needs the network inventory actions:

1.  Create a record producer. To learn more, see [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
2.  Create a change model. To learn more, see [Create a change model](https://www.servicenow.com/docs/access?context=create-a-change-model&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

    By default, the Telecommunications Network Inventory application provides the change models that are described in the following table.

    |Change Models|Description|
    |-------------|-----------|
    |Provision LAG|Creates Ethernet links across ports, and a LAG circuit over those Ethernet links. LAG has virtual interfaces. The VLAN ranges are also created and associated with LAG.|
    |GPON broadband Service \(Automated\)|Provisions a GPON service over the existing network.|
    |Fiber-wise Mobility Infrastructure|Provisions a mobility infrastructure over the existing network.|
    |Design and Assign Telco Equipment|Creates equipment according to the predefined template at a particular network site.|

    The states are New, Implement, Review, and Closed for the earlier change models. By default, all new change model states are set as New.

3.  Create a decision entry in the decision table provided by the Telecommunications Network Inventory application. See [Order Management for Telecommunications integration](../task/decision_table_for_tni_omt_integration.md) to learn how to create an entry.


![TNI-OMT Integration for creating a change task. For the text description, refer to the workflow steps that follow.](../image/omt-tni-integration-flow.png)

The workflow for creating a change task using TNI-OMT integration is as follows:

1.  The OMT subflow creates an order task.
2.  When the Order Task Created trigger is received, the TNI flow launches the Create Change Request and later creates a Change Request action.
3.  The OMT action and Service Specification are mapped to the Change Model, Record Producer in the TNI Order Task Submit Script Include and Decision Tables. Then the OMT characteristic is mapped to the Record Producer variables.
4.  The Producer is then submitted to the Record Producer via the sn\_sc.CatItem API.
5.  It creates a Change Request with respect to the Order Task, Change Model, and Variables. Also, it uses the sn sc.CatItem API to return the result to the TNI flow.
6.  When this action is completed, it adds work notes to the Order task.
7.  After the Change Request is closed, it adds work notes to the Order task.

## For inventory agents

An inventory agent can open, verify, implement, and close the assigned change tasks. After implemented, the created CIs are added under the **Affected CIs** tab. The work notes of the order task are updated when the order task is closed.

As a result, the Order Management for Telecommunications and Media application fetches the list of the affected CIs and creates an install base item to relate the product order to the CI. To learn more, see [Configuring order fulfillment in Order Management for Telecommunications, Media, and Technology](https://servicenow.com/docs/bundle/utah-technology/page/product/tmt-order-mgt/concept/order-mgt-configuring.html).

**Note:**

-   A change request for an order task is created automatically only if a decision entry is created.
-   A number of change requests is created based on the need for inventory action of an order task.
-   As a demo data:
    -   In the Order Management for Telecommunications and Media application, the SD-WAN product has an Allocate and Install CPE task that triggers an equipment creation change request to the Telecommunications Network Inventory application.
    -   The Telecommunications Network Inventory application has demo data that you can use to create equipment, provision a link aggregation group \(LAG\), automate a Gigabyte Passive Optical Network \(GPON\) broadband, and fiber wise mobility infra as Telecommunications Network Inventory workflows.

**Parent Topic:**[Integrating Telecommunications Network Inventory with other applications](integrating-telecommunications-network-inventory--applications.md)

**Related topics**  


[Telecommunications Network Inventory integration with Hardware Asset Management](integration-with-hardware-asset-management.md)

