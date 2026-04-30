---
title: Add operation steps to a resource block
description: After you configure operations and input parameters for your resource block, add steps for each operation to tell the system which Cloud API \(CAPI\) to call. Each step is a separate call to CAPI.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add operation steps to a resource block

After you configure operations and input parameters for your resource block, add steps for each operation to tell the system which Cloud API \(CAPI\) to call. Each step is a separate call to CAPI.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## Procedure

1.  On the resource block, click the **Steps** sub-tab under **Operations**.

2.  Click **Add Step**.

3.  Fill in the form fields.

<table id="table_q1n_4qw_52b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Operation Type

</td><td>

Select the type of operation:

-   **Invoke Cloud API**: Select this option to select a provider, interface, and method from CAPI.
-   **Invoke Host Resource Operation**: Select this option to use an operation \(also called an operation signature\) from the host interface that you already specified for this resource block.
-   **Invoke Script**: Select this option to invoke a method from an existing MID Server script include.
-   **Invoke Workflow**: Select this option to invoke a pre-existing workflow triggering operations on this resource block.
-   **Invoke Flow**: Select this option to invoke subflows from a list of active subflows.


</td></tr><tr><td>

API Provider\[Operation Type = Invoke Cloud API\]

</td><td>

Select the API that provides the interfaces you need. The providers are part of the Cloud API \(CAPI\).

 For example, CAPI supplies the AWS provider, which has products, some of which have provider names.

 This value appears if you select the Invoke Cloud API operation type.

</td></tr><tr><td>

API Interface\[Operation Type = Invoke Cloud API\]

</td><td>

Select the interface that has the methods you want to use. For example, the **Blob Storage Interface** provides the **CreateContainer** interface, which the system uses during provisioning.

</td></tr><tr><td>

API Method\[Operation Type = Invoke Cloud API\]

</td><td>

Select the method to perform the operation. In this example, **CreateContainer** is required to provision storage.

</td></tr><tr><td>

CAPI Version\[Operation Type = Invoke Cloud API\]

</td><td>

Enter the version of the CAPI API.

</td></tr><tr><td>

Host Interface\[Operation Type = Invoke Host Resource Operation\]

</td><td>

Select the interface from which to call an operation. You can only select the same interface that you configured on the **General Information** tab of the resource block. To change the interface, navigate back to the **General Information** tab and select another value in the **Host Interface** field.

</td></tr><tr><td>

Interface Operation\[Operation Type = Invoke Host Resource Operation\]

</td><td>

Select the operation from the host interface. For example, if you select **Storage Server** Interface, you can call all the operations in that interface, such as CreateStorageVolume.

</td></tr><tr><td>

Scripts\[Operation Type = Invoke Script\]

</td><td>

Enter the script you want to invoke, along with a method in the script. Use this syntax: `script-name.method`.

</td></tr><tr><td>

Workflow\[Operation Type = Invoke Script\]

</td><td>

Do not use Workflow.

</td></tr><tr><td>

Flow\[Operation Type = Invoke Flow &gt; Subflow\]

</td><td>

Select the subflow from the Subflows list. For example, if you select a Terraform Enterprise Provision subflow, you can simply reuse the existing subflow to populate the Inputs&amp;Outputs

</td></tr><tr><td>

Condition

</td><td>

Enter an optional condition that must be met before the system uses this step.

</td></tr></tbody>
</table>    If you look at the Azure API and the CreateNode method mapper, you can see that the endpoint operation is a script. It calls the MID Server script include, which shows you the createNode\(\) function. This function uses AzureComputeVirtualMachine script include. Take time to review and understand this script include.

4.  Click **Submit**.

    The **Input** and **Response Processor** tabs appear for the step.

5.  On the **Input** tab, configure the CAPI operation inputs.

    On the CAPI interface, which in this case is **Blob Storage** Interface, open CreateContainer method. The inputs from CAPI are shown on the Input tab, where you create parameters.

    Remember that the parameters on the **Input Parameters** tab is where users enter values. You can map those input parameters to the parameters on the **Input** tab. To do this, copy the **Mapping** value from the **Input Parameters** tab into the **Value** field on the **Steps** &gt; **Input** tab.

    If this step is invoking a script, and that script requires arguments to return values, you can add a new input parameter for each argument. Use this syntax in the **Value** field: `${parameter.arg1}`.

6.  If any subsequent steps in this operation or subsequent operations require parameters values from this step to be passed to them, configure output attributes.

    For example, the Provision operation for a virtual server can provide an output attribute for the network interface ID and another for the node ID. When the cloud provider sends the response, the actual ID of the network and node are parsed out of the response and saved in the output attributes. Subsequent steps use the IDs to perform actions.

    1.  Click the **Output Attributes** tab.

    2.  Enter code in the following notation:

        ```
        
        {
          "Attribute": "${Value}"
        }
        
        ```

        Where the value comes from a mapping to the interface and the operation.

        For example, in the following output attribute:

        ```
        
        {
          "NodeId": "${Compute Interface.CreateNode.Output.resp.nodeId}"
        }
        
        ```

        -   `NodeId` is the attribute.
        -   `Compute Interface` specifies the interface.
        -   `CreateNode` is the name of the method that creates the node.
        -   `Output.resp` is a mandatory part of the syntax.
        -   `nodeId`

-   **[Add an operation to a resource block to use with a workflow](add-op-to-resource-for-wrkflw.md)**  
You can select from the existing operations in a resource block to work with your workflow or you can create a custom operation.
-   **[Add a resource operation step to invoke a workflow](add-resource-op-step-invoke-wrkflw.md)**  
You can invoke a workflow by adding an operations step to a resource and then associating the resource to a workflow.
-   **[Add a resource operation step to invoke a subflow](add-resource-op-step-subflow.md)**  
Invoke a subflow by adding an operations step to a resource and then associating the resource to a new or existing subflow.

**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

