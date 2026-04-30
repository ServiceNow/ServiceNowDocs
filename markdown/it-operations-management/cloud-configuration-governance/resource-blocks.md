---
title: Resource blocks in Cloud Provisioning and Governance
description: Resource blocks act as a type of middleware component between catalog items, the Cloud API \(CAPI\), and the CMDB.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Resource blocks in Cloud Provisioning and Governance

Resource blocks act as a type of middleware component between catalog items, the Cloud API \(CAPI\), and the CMDB.

The following graphic illustrates how resource blocks fit between other components in the system:

![Resource blocks in the cloud provisioning and governance environment](../image/rb-system-basic.png)

-   **Blueprints**

    Each resource block becomes a building block within a blueprint. The blueprint eventually becomes a catalog item \(also called a stack\) that a user provisions from the Cloud Catalog.

-   **Cloud API \(CAPI\)**

    Each resource block defines allowable operations, such as Provision and Deprovision. These operations call various components within CAPI to carry out the operation that is received from the stack.

-   **The CMDB**

    Each resource block is based on a CI type from the CMDB. Resource blocks also have a response processor that handles responses from the cloud provider to take some type of action in the CMDB, such as creating or updating a CI.


## How resource blocks are connected

Resource blocks are connected to each other in blueprints. For example, in this blueprint, a virtual server resource block is connected to storage. The virtual server and the storage are both connected to an AWS datacenter resource block.

![Blueprint server with storage](../image/bp-server-with-storage.png "Blueprint server with storage")

For these connections to be successful, each resource block needs to specify a type of interface. This graphic illustrates these interfaces:

![Resource block interfaces](../image/rb-interfaces.png "Types of interfaces for resource blocks")

-   The guest interface connects to the resource that is above it. The guest interface contains the operations \(also called operation signatures\), which allows users to take action on their resource.
-   The host interface connects to the resource below the resource block in the blueprint. The host interface also contains operation signatures.
-   The bindings connect adjacent resources.

Resource blocks can have as many guest interfaces, host interfaces, and bindings as necessary. Connections can be made in different directions:

-   Vertical connections require the top resource block to have the same host interface as the bottom resource block guest interface.

    **Note:** In blueprints, this vertical connection is called a containment connection.

-   Horizontal connections bind one resource to another, but both resources have to reside on top of the same resource block.

    **Note:** In blueprints, this horizontal connection is called an attached-to connection.


The same example blueprint with a virtual server with attached storage on an AWS datacenter, the resource blocks are configured as this graphic illustrates:

![Interfaces for resource blocks](../image/rb-example-connections.png "Interfaces for resource blocks")

<table id="table_ils_l45_w2b"><thead><tr><th>

Resource block

</th><th>

Interfaces and bindings

</th></tr></thead><tbody><tr><td>

Virtual server

</td><td>

-   Host interface: Compute
-   Binding: to Storage Volume

</td></tr><tr><td>

AWS Datacenter

</td><td>

-   Guest interface: Compute
-   Guest interface: Storage Server interface

</td></tr><tr><td>

Storage

</td><td>

Host interface: Storage Server interface

 The binding between the virtual server and the storage is unidirectional. You configure the binding on the virtual storage resource block only by specifying the storage resource block. You do not need to configure another binding on the storage resource block.

</td></tr></tbody>
</table>## Guest interfaces and operations

Each guest interface provides a default set of operations \(also called operation signatures\) that allow the user to choose what they want to do with a virtual resource. The most common operation is Provision, which means that a virtual resource is created. Many guest interfaces and corresponding operations are provided by default with the Cloud Provisioning and Governance application. You can use these default guest interfaces for many of your resource blocks.

If you do need to create a new guest interface, these operations are provided by default:

-   Start
-   Stop
-   Provision
-   Deprovision
-   Cleanup
-   ModifySchedule
-   ModifyLease

## Resource block component details

Each resource block contains these components:

-   **Layers**

    The logical layer in the stack that this resource block belongs to. By default, Cloud Provisioning and Governance provides the layers. When you configure resource blocks, you can choose the one that relates to you.

-   **Operations for each guest interface**

    As mentioned, each guest interface provides operations. For example, the most common operations for a virtual server are **Provision**, **Deprovision**, **Start**, **Stop**.

-   **Input parameters for each operation**

    The input parameters hold values that the cloud provider uses, via CAPI, when operations are run. These parameters hold the information that the user selects while performing an operation, such as provisioning, on a stack.

    For example, a user typically must specify the location, which is a datacenter, that a stack belongs in. The value that the user selects in the **Location** field is held in the Location parameter. The system takes this parameter, which is available by default for the virtual server resource block, and passes it to the CreateNode CAPI interface operation. The CreateNode interface operation tells the cloud provider to create \(or provision\) the actual virtual server.

-   **Steps for each operation**

    Each operation requires a step to do the actual work. Each step calls a specific interface and method in CAPI, and passes along the input parameters required by that method. For example, the **Provision** operation on a virtual server provides one step to first connect and create a virtual machine, and another step to create the node in the cloud provider. Each step provides different input parameters. To connect and create a virtual machine, the cloud account, among many other parameters, is required. To create the node, the cloud account is not required.

    You can add as many steps as needed for each operation. You can also use output attributes to pass values in attributes from one step to another step, or from steps in one operation to steps in a subsequent operation. For example, the **Provision** operation for a virtual server can provide an output attribute for the network interface ID and another for the node ID. When the cloud provider sends the response, the actual ID of the network and node are parsed out of the response and saved in the output attributes. Subsequent steps can then use the IDs to perform actions.

-   **Response processors**

    Response processors tell the system what to do in the CMDB. When the cloud provider sends a response after an operation is run, the processor handles the response.

    **Note:** These processors are scripts that are system includes. They are not MID Server script includes like the CAPI scripts that you can create to integrate with the cloud provider.


![How resource block components work together](../image/rb-system-complex.png "How components work together")

Users can see catalog items, also called stacks, in the Cloud Catalog. A catalog item is based on a blueprint, which in turn is composed of resource blocks that are connected together.

1.  The user kicks off the process by requesting a stack. The request is the **Provision** operation in the system.
2.  The system runs the steps in order for the **Provision** operation for the resource blocks that comprise the stack.
3.  Each step calls CAPI to determine which method to run, while also passing in values for necessary parameters.
4.  CAPI interfaces with the API of the cloud provider to provision the actual resource.

![Response process from the cloud provider](../image/rb-system-complex-response.png "Process flow when a resource is created in the cloud provider")

1.  The cloud provider provisions the resource and responds with JSON.
2.  The system parses the response inside the resource script in the resource block.
3.  The system updates the CMDB. When provisioning a new resource, the system creates a CI in the correct table.
4.  The new stack appears in the cloud user portal for the user to manage.

## The Resource Blocks page

Manage resource blocks in the Resource Blocks page. Open the Cloud Admin portal, and then navigate to **Design** &gt; **Resource Blocks**.

![Resource block page and descriptions of the items in the page](../image/resource-block-list.png "Resource Blocks page components")

-   **[Create a custom resource block](../task/create-resource-block.md)**  
If the blocks in the base system do not provide the cloud resources that you need to provision, you can create a custom resource block.
-   **[Configure resource block input parameters](../task/manage-resource-block-operations.md)**  
You can configure operations for each interface of a resource block by specifying input parameters, steps, and output attributes. Input parameters hold values that the system requires to identify and manage a virtual resource, such as the datacenter and resource group that the resource is in.
-   **[Add operation steps to a resource block](../task/add-operation-steps.md)**  
After you configure operations and input parameters for your resource block, add steps for each operation to tell the system which Cloud API \(CAPI\) to call. Each step is a separate call to CAPI.
-   **[Extend Cloud Provisioning and Governance resource blocks with an override operation](../task/extend-cloud-management-entities.md)**  
You can extend your existing guest interface to create a new operation. You can also create a new guest interface with its own operations, parameters, and inputs.
-   **[Add a resource script to a resource block](../task/add-resource-script-resource-block.md)**  
A resource script operates on a resource during deployment or returns data to the CMDB after a resource is deployed.
-   **[Configure a response processor](../task/configure-response-processor.md)**  
Configure a response processor to handle responses from datacenters.
-   **[Add Terraform Orchestration interface on a resource block](../task/add-terraform-orchestration-interface.md)**  
After you have activated the Terraform store app for Cloud Provisioning and Governance, to support cloud-based operations for cloud providers using Terraform Open Source Edition. Add the Terraform Orchestration interface on resource block, to execute cloud-based operations via terraform templates.
-   **[Create a resource block for Microsoft Azure Cloud](../task/create-resource-block-azure-terraform.md)**  
Resource blocks are the building blocks of cloud catalog items. Create a resource block for the Microsoft Azure Cloud Platform provider, based on a CI type from the CMDB.

**Parent Topic:**[Cloud Admin Portal](cloud-admin-portal.md)

