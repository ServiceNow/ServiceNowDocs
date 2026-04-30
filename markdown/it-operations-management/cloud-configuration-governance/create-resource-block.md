---
title: Create a custom resource block
description: If the blocks in the base system do not provide the cloud resources that you need to provision, you can create a custom resource block.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a custom resource block

If the blocks in the base system do not provide the cloud resources that you need to provision, you can create a custom resource block.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal** &gt; **Design** &gt; **Resource Blocks** and click **New**.

2.  Enter a unique and meaningful **Name** and **Description** for the resource block, and then enter the following settings:

<table id="table_r15_zcr_fz"><tbody><tr><td>

Layer

</td><td>

Select the layer that represents the type of resource block:

 -   **Application**: Resources that are applications. For example, the 'PetStore' application might exist on a Tomcat or WebLogic platform.
-   **Platform**: Resources that are typically hosted on a virtual server like MySQL, Tomcat, or Apache.
-   **Logical DataCenter**: Resources that are datacenters like AWS, Azure, or vSphere.
-   **Virtual Infrastructure**: Resources that are virtual and still provide infrastructure for the virtual world like NetApp SVM, NetApp CDOT, CISCO ICF Cloud, or VMware NSX.
-   **Virtual Workload**: Resources that are hosted on a datacenter. For example, Virtual Server, Storage Volume, Network, or Gateway.
 **Note:**

-   Applications are deployed on Platforms.
-   Platforms are deployed on Logical Datacenters or Virtual Infrastructures.


</td></tr><tr><td>

CI type

</td><td>

Select the type of CI in your CMDB that the resource block represents. When the user launches a stack, the cloud resources are provisioned and actual CIs that for the resources are created in the CMDB in this CI type.

 For example, if you select Storage Volume, the system creates a record in the Storage Volume \[cmdb\_ci\_storage\_volume\] table when the user provisions a new volume.

 **Note:** Each resource block is based on a CI type from the CMDB. Ensure that you do not have more than one resource block bound to a CI type.

</td></tr><tr><td>

Default Guest InterfaceCreate interface

</td><td>

Select the guest interface that contains the operations you need for the resource. Later you can further define and select the operations to use for this default guest interface. The system gives you a set of default operations for each interface.

 If another resource block specifies a **Host interface** \(see the Host interface field description\) that matches what you specify here in the **Guest interface** field, that resource block can be a potential host for this resource block.

 If you select the **Create interface** check box, enter a name for the guest interface. The system creates the guest interface, opens the resource block that you are configuring in the resource block form, and lists the new interface in the **Resource Guest Interface** related list. See the description of the Resource Guest Interface in the following steps.

 If you create a new guest interface, also keep in mind that other resource blocks can use the interface.

</td></tr><tr><td>

Host interface

</td><td>

Select the interface that the potential host of this resource block must offer up. Any other resource block that offers up a default guest interface of the same type you specify here can become a host of this resource. Later on, you can select one or more actual host resources.

 For example, by default the AWS Datacenter resource block specifies the **Compute** interface as a default guest interface. That means the AWS Datacenter is offering the **Compute** host interface to other resource blocks through which to connect to the AWS Datacenter.

 Specify the **Compute** interface here as the host interface of the resource block so the resource block can look for any other resource block using the **Compute** interface as its guest interface. Since the AWS Datacenter does use the **Compute** interface as its guest interface, later you can select the AWS Datacenter as the actual host in the Host Resource related list.

 Other resource blocks that offer the **Compute** interface by specifying **Compute** as the guest interface, are also potential hosts for this resource block.

 You must know which interfaces the potential host resources offer as guest interfaces. And determine which operations are part of those guest interfaces.

</td></tr></tbody>
</table>3.  Click **Submit**.

    Continue updating settings on the related lists, as needed.

4.  Complete the following steps to add another guest interface.

    You can specify an additional guest interface to offer to other resource blocks. For example, a datacenter resource block might offer a **Compute** interface, a **Network Service Container interface**, and a **Firewall** interface for other resource blocks to use.

    1.  Under **Guest Interface**, click **New**.

    2.  In the **Guest interface** field, select an interface.

        ![Selecting a guest interface](../image/selecting-a-guest-interface.png)

    3.  Click **Submit** or **Update**.

5.  In Host Resource, specify the resource that can host this resource block, typically the one that offers the interface you specified in the **Host Interface** field.

    The selected host resource block handles the provisioning of this resource block. For example, the host resource is a virtual machine resource block that can host an Apache Web server. The host resource selection limits the options that are presented to users when they select a host.

    For example select **vSphere Datacenter** in the **Host Resource** field for this resource to be hosted in a VMWare cloud.

    ![example host resource](../image/host-resource-example.png)

    **Note:** You can select only the host resources that support the **Host interface** previously specified for this resource block.

6.  Complete the following steps to add bindings.

    A binding is another resource block that this resource block can connect to. Select resource blocks that support the same **Guest interface** configured for this resource block.

    When you create a blueprint, you can add an attach connection between two resource blocks that are connected with this binding. Understanding the direction of the binding is essential to configuring the resource block. You attach a virtual server to a network, or you attach storage to a virtual server. You cannot reverse these directions.

    1.  Under **Bindings**, click **New**.

    2.  In the **Host Resource** field, select a resource in the **Guest Resource** field.

        The guest resource is the resource block that you are attaching to the current resource block.

    3.  Click **Submit** or **Update**.

    For example, a virtual server can connect to virtual storage. By default, the base system provides a Virtual Server resource block with a binding to the Storage Volume resource block to enable this connection.

    ![Example binding to storage volume](../image/example-binding.png)

7.  Complete the following steps to configure endpoint operations between the two resources to bind.

    The endpoints call operations during binding. For example, a storage volume can specify an endpoint with required conditions and the operations to execute to make a connection to a virtual server. The virtual server must also support a binding interface to the storage volume.

    Implement an endpoint type, such as **Block EP**, for the virtual server to consume the endpoint. Later, when you create blueprints, create the binding between the storage volume and the virtual server.

    ![Endpoint mapping for a storage volume](../image/connection-in-blueprint-canvas.png "Example of binding in a blueprint")

    1.  Under **Endpoint Operations**, click **New**.

    2.  In **Binding Resource**, select the resource block that consumes the endpoint from this resource block.

    3.  Select the type of endpoint that the **Source Resource** presents.

    4.  In **Operation implementation**, select the implementation that performs the operation you are defining in this endpoint mapping.

    5.  Select the **Type** of operation to perform for the mapping.

        Only operations that are appropriate for the specified **Endpoint** appear in the list.

        Do not change the settings in **Source Resource**.

    6.  Click **Submit** or **Update**.


-   **[Specify a host resource for a resource block](specify-host-resource-cmp.md)**  
Hosts that support the **Host interface** of a resource block are potential hosts for the resource block. You use the **Host interface** setting to further limit the options that are presented to the stack requester while selecting a host type.
-   **[Specify the bindings for resource blocks](specify-resource-bindings-cmp.md)**  
Bindings represent endpoint relationships. For example, a storage volume might implement an endpoint type of Block EP \(cmdb\_ci\_endpoint\_block\). A virtual server might consume an endpoint of that type. Bindings must support the Guest interface that is specified for the resource block.
-   **[Configure endpoint operation mapping](configure-endpoint-mapping-cmp.md)**  
You can configure endpoint mapping on a storage volume to make a connection to a resource.

**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

