---
title: Configure resource block input parameters
description: You can configure operations for each interface of a resource block by specifying input parameters, steps, and output attributes. Input parameters hold values that the system requires to identify and manage a virtual resource, such as the datacenter and resource group that the resource is in.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Resource blocks in Cloud Provisioning and Governance, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Configure resource block input parameters

You can configure operations for each interface of a resource block by specifying input parameters, steps, and output attributes. Input parameters hold values that the system requires to identify and manage a virtual resource, such as the datacenter and resource group that the resource is in.

## Before you begin

Role required: sn\_cmp.cloud\_service\_designer

## About this task

The system automatically associates default operations from the Cloud API \(CAPI\) to the resource block when you add interfaces to it. It also provides default input parameters for each operation.

## Procedure

1.  Open a resource block, and then click the **Operations** tab.

    ![Operations tab for resource blocks](../image/rb-operations.png)

    The **Input Parameters** sub-tab appears by default.

2.  Select the interface from the **Interface** choice list.

    The interfaces in this choice list are derived from the **Resource Guest Interface** list on the **General Information** tab that you already configured when you created a resource block.

    ![Selecting a resource block interface](../image/rb-interface-list.png)

3.  Select the operation on which you want to modify the input parameters.

    You can also create a new operation.

    1.  Click the **Add Operation** icon.

        ![Adding an operation](../image/icon-add-operation.png)

    2.  Fill out the form \(see table\):

<table id="table_cnl_w3v_m2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

Operation type

</td><td>

Select the type of operation from the choice list.

</td></tr><tr><td>

Access type

</td><td>

Select **Public** to make the resource block operation available from the catalog order form when a user manages a stack that they own. The actual operations appear in a list on the catalog order form:

 ![Operations for the user](../image/user-portal-operations.png)

 Select **Private** to prevent the operation from being used when a user launches a stack.

 This setting applies at the catalog-item level, not the whole-stack level. You can control the access type on the whole stack when you configure blueprints.

 As an example, you might want to mark the `Deprovision` operation as private for an individual VM, but not for the whole stack. This allows the user to deprovision everything at once and prevents the user from just deprovisioning the VM.

</td></tr></tbody>
</table>    3.  Click **Submit**.

4.  Configure the input parameters to provide a way to input the items you need to run the selected operation.

    For example, if you add a Provision operation for an AWS resource, you need, at minimum, the CloudAccount parameter and the Location parameter to perform the operation. You need to know the providers API to know what to pass to it. For example, if you want to add a provision operation for an S3 bucket on AWS, you need to know the [allowable AWS operations on buckets](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketOps.html) and the Request Elements for things like creating a bucket \([the PUT Bucket operation](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUT.html)\). You can typically find these resources in the AWS and Azure documentation.

    1.  Click the **Add Input Parameters** icon.

        ![add input parameters](../image/icon-add-input-parameters.png)

    2.  Add the **Name** of the parameter that you obtained from the cloud provider API.

        In this example, you could add `CreateBucketConfiguration` for an [AWS S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/API/RESTBucketPUT.html#RESTBucketPUT-requests).

    3.  In the **Datasource** column, select the type of input parameter you are configuring.

        This value specifies the source or location where the parameter value comes from:

        -   **Text**: a text value that the user passes.
        -   **Pools**: the query that you want to run against a pool to get a value back from it. The pool **Datasource Value** should follow this convention: `ServiceNow::Pools::PoolName.Pool-Filter-Name`. See [Pools and Filters for Cloud Provisioning](../concept/pools.md) for more information on pools.
        -   **CSVList**: values from a comma-separated value list that you enter into the **Datasource Value**.
        -   **Array**: an array of values. You can programmatically send it an array in JavaScript. The format is as follows: `['abc','def']`.
        -   **FormData**: data submitted from the form configured in the blueprint.
        -   **ResourceScript**: an expression that passes a value. The expression should follow this convention in the **Mapping** field:

            `$(Script:script-name.function[arg1=${value-to-pass},arg2=${value-to-pass}])`

        -   **TLR**: the value inherited from the top-level resource container above this resource block in the blueprint.
    4.  Click **Save**.

    5.  In the **Mapping** column, you can view the auto-generated mapping values.

        Mappings specify where to pull the information in the system. You do not have to change the mapping values except for **ResourceScript** type parameters, where you must enter the expression.

    6.  In the **Default Value** column, specify a value that you want the system to use if the user does not pass any value or if you did not enter anything in the **Datasource Value**.

    7.  Select **Create Form** to make this attribute available in the order form that the user sees when trying to provision the stack item.

        You can also select **Mandatory** to force the user to enter a value.

    8.  In the **Restricted To** column, click the restricted icon \(![restricted to](../image/icon-restricted-to.png)\), and then select a resource block to restrict the attribute to be passed to a specific host.

        In this example, you are configuring a resource block for a virtual server on vSphere, which requires the name of the VM folder \(represented by the `VmFolderName` attribute\). Other datacenter types do not need the name of the VM folder. Therefore, you can restrict `VmFolderName` to the vSphere datacenter resource block.

        This image illustrates how the VMFolderName attribute is restricted to the vSphere Datacenter.![VMFolderName](../image/vmfoldername-attribute.png)

        ![Restricting to a vSphere datacenter](../image/vsphere-datacenter-restricted-to.png)


**Parent Topic:**[Resource blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

