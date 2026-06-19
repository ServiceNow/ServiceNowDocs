---
title: AWS VM provisioning walkthrough
description: This example walks you through the components of Cloud Provisioning and Governance that function during the provisioning of a virtual machine in an AWS datacenter. Topics covered include blueprints, resource blocks, the Cloud API \(CAPI\), and MID Server script includes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-configuration-governance/walk-through-provisioning.html
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 13
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS VM provisioning walkthrough

This example walks you through the components of Cloud Provisioning and Governance that function during the provisioning of a virtual machine in an AWS datacenter. Topics covered include blueprints, resource blocks, the Cloud API \(CAPI\), and MID Server script includes.

## Before you begin

Role required: admin

## About this task

This walkthrough starts with a Windows VM that a user already provisioned in AWS. Next it walks you through the blueprint with the VM, the resource blocks, and then the CAPI calls specified from the resource blocks. Finally, the walkthrough shows you how a base MID Server script include makes the actual calls to the AWS API.

This example uses default resource blocks and script includes that are available in your instance. Therefore, although you might not have a provisioned VM on your instance, you can still follow these steps and view the components used in this example to understand how the components work.

For an example of a VM in Azure, see [Azure VM provisioning walkthrough](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/walk-through-azure-provisioning.md).

**Note:** The terms virtual machine, VM, and virtual server are used interchangeably in this example.

## Procedure

1.  Look at a provisioned VM in the Cloud User Portal, and focus on some of the details about the VM:

    1.  On your instance, open the Cloud User Portal \(Cloud Provisioning and Governance **Cloud User Portal**\).

    2.  View a provisioned VM in a stack, such as this Windows VM, by clicking **Stacks**, and then clicking the name of the stack.

        In this example, the stack is named **MyStack**.

        \[Omitted image "mystack-example.png"\] Alt text: MyStack example

    3.  Under **Resources**, click the VM in the stack.

        \[Omitted image "mystack-virtual-server.png"\] Alt text: Virtual Server example

    4.  View the properties of the VM, and notice that it is in region us-east-1 in an AWS Datacenter.

        \[Omitted image "mystack-vm-details.png"\] Alt text: VM details

2.  Look at the blueprint on which the VM is based:

    1.  Navigate to **Design** &gt; **Blueprints**, and then open a blueprint with a virtual server in the Azure datacenter. The **Deployment Model** tab appears by default, showing you the various components of the blueprint.

        This example blueprint has three components: The container, the virtual server, which is the actual VM that is provisioned, and the AWS datacenter.

        \[Omitted image "mystack-blueprint.png"\] Alt text: An example blueprint with a Windows server

    2.  Click the **Operations** tab on the bottom, and then click **Provision**.

        \[Omitted image "mystack-provision-block.png"\] Alt text: Provision operation

        The Provision operation is the operation that the system triggered when it created the VM. Other default operations are available, but this example focuses on the Provision operation.

    3.  Click the **Provision** block for Blueprint Container Resource.

        \[Omitted image "myazurevm-provision-container.png"\] Alt text: My Azure VM blueprint container

    4.  On the right, notice that one of the parameters in the Inputs list is Location.

        This parameter holds the value eastus, which is where the VM lives in the datacenter.

        \[Omitted image "mystack-location-param.png"\] Alt text: The Location parameter

        Inputs can be specified on the container, as it is in this example, or on any other resource block. By default, the **Location** parameter is already specified for you in the Blueprint Container resource block, so that you can use it in every blueprint like this one. If you switch the blueprint to **Draft**, you can add more parameters to the Blueprint Container resource block. You cannot add parameters to the Virtual Server resource block. For this walkthrough, no additional parameters are necessary.

3.  Look at the Virtual Server and AWS Datacenter resource blocks used in this blueprint:

    1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

    2.  Search for and open the **Virtual Server** resource block, which is provided by default with Cloud Provisioning and Governance.

        \[Omitted image "rb-virtual-server-tile.png"\] Alt text: The default virtual server resource block

    3.  On the Resource Block form, click the **Host Resource** related list to view the list of supported host resource blocks.

    4.  Notice that the host interface and host resource are already specified:

        \[Omitted image "mystack-virtualserver-rb-interfaces.png"\] Alt text: Host interface on virtual server

        -   The **Host Interface** field specifies the interface that must match the guest interface in the resource block that hosts this virtual machine. In this case, the host interface is the Compute Interface, which is also the guest interface on the AWS Datacenter resource block. By default, the datacenter resource blocks provide several guest interfaces that other resource blocks like virtual storage can use to connect to the datacenter.
        -   The **HostResource** column in the **Host Resource** related list already specifies **AWS Datacenter**, which means that the AWS datacenter resource block is a valid host for this VM.
    5.  Click the **Operations** tab, and then click the **Steps** subtab.

        \[Omitted image "mystack-operations-steps.png"\] Alt text: Selecting the Steps subtab

    6.  Select **Provision** from the **Operation** list.

        \[Omitted image "mystack-operations-provision.png"\] Alt text: The Provision operation

        Remember that the Provision operation is the operation that the system used to create the VM. Other default operations are available, but this example focuses on the Provision operation.

    7.  Notice the step that appears in the list and the full step description that appears above the input parameters:

        \[Omitted image "mystack-provision-step.png"\] Alt text: Step for Provision

        -   **Host Resource Operation:** indicates that this step calls an operation on the host resource \(the AWS datacenter in this example\).
        -   **Compute Interface** is the guest interface on the AWS datacenter that this step is using.
        -   **ConnectAndCreateVirtualMachine** is the operation in the AWS datacenter that this step calls.
        **Note:** In this case, the step calls an operation from another resource block: the AWS datacenter. Steps can also call CAPI directly, and then CAPI can execute REST calls to the cloud provider API. You can see that when you look at the AWS datacenter resource block.

    8.  Navigate back to **Design** &gt; **Resource blocks**.

    9.  Open the **AWS Datacenter** resource block,which is the host resource block that the virtual server is connected to.

    10. Notice the supported guest interfaces in the **Guest Interface** related list:

        \[Omitted image "mystack-aws-rb-compute-interface.png"\] Alt text: Guest interfaces for AWS datacenter

        These guest interfaces are the interfaces that the AWS datacenter makes available to other resource blocks. The **Compute Interface** is provided so that the Virtual Server resource block, which specifies the Compute Interface as its host interface, can connect to the datacenter.

    11. Click the **Operations** tab, and then click the **Steps** subtab.

        \[Omitted image "mystack-operations-steps.png"\] Alt text: Selecting the Steps subtab

    12. In the **Interface** list, select **Compute Interface** if it is not already selected.

        \[Omitted image "mystack-awsdatacenter-compute.png"\] Alt text: Compute interface

        Remember that this interface is specified in the Virtual Server resource block.

    13. In the **Operation** list, search for and select **ConnectAndCreateVirtualMachine**.

        \[Omitted image "mystack-connectandcreate-operation.png"\] Alt text: The ConnectAndCreateVM operation

        Remember that this operation is specified in the Virtual Server resource block.

    14. Notice the CAPI call that is used in the only step for the ConnectAndCreateVirtualMachine operation:

        \[Omitted image "mystack-awsdatacenter-createnode.png"\] Alt text: The CreateNode API call

        -   **Cloud API:** indicates that this step calls CAPI, so that CAPI can execute a REST call to the cloud provider, which in this case is AWS.
        -   **Compute Interface** specifies the CAPI interface that this step calls.
        -   **CreateNode** indicates the method that is executed. As the name suggests, this method tells AWS to create the virtual machine.
    15. With the resource block in the **Draft** state, point to the highlighted \(blue\) step and then click the **Edit Step** icon to open the step configuration.

        \[Omitted image "mystack-edit-step.png"\] Alt text: Edit step

    16. Look at the step configuration, and notice the settings that integrate with CAPI:

        \[Omitted image "mystack-edit-steps.png"\] Alt text: Step settings\\

        |Field|Description|
        |-----|-----------|
        |Operation Type|**Invoke Cloud API** specifies that this step should call the CAPI via the given provider, interface, and method.|
        |API Provider|**AWS Elastic Compute Cloud** is a product \(not that actual provider\) that belongs to the AWS provider as defined in CAPI.|
        |API Interface|**Compute Interface** is a product that belongs to the AWS provider as defined in CAPI.|
        |API Method|**CreateNode** is the method that calls AWS to create the VM.|

        **Note:** The CAPI API definition ties together the provider \(AWS\), the product \(AWS Elastic Compute Cloud\), the interface \(Compute Interface\), and the method \(CreateNode\).

    17. Close the window.

    18. With the **Compute Interface.CreateNode** step selected, click the **Response Processor** tab, and notice the **Create\_Virtual\_Server\_Response\_Processor** script.

        \[Omitted image "mystack-response-processor.png"\] Alt text: Response Processor tab

        This script is the response processors that updates the CMDB in your instance after the virtual machine is created in AWS.

    19. View an explanation of the script and the example that is a part of the topic at [Create a Response Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/response-processor-example.md).

        When you finish reviewing that topic, return to this topic.

4.  Look at the CAPI components that work together to provision the VM:

    1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API**.

    2.  Click the **API** tab.

    3.  Search for an open **AWS Compute API**.

        There are two AWS Compute API records. Open the first one in the list that matches the image in the next step.

    4.  Look at how this CAPI API ties together an interface and a product:

        \[Omitted image "mystack-aws-compute-api.png"\] Alt text: AWS Compute API

<table id="table_afd_zy3_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud API Interface

</td><td>

**Compute Interface** is the same interface that you can see specified in the resource block. The interface contains the definition for methods, including the **CreateNode** method.

</td></tr><tr><td>

Connector

</td><td>

**Cloud Compute Connector** indicates that this CAPI makes Java calls to the system, which then calls the AWS API. This connector is not scripted. If this were a scripted connector, it was have a MID Server script include that calls the AWS API. **Note:** Most AWS-related APIs that are provided in the Cloud Provisioning and Governance application by default are not scripted, like this one, and cannot be modified. But you can create your own scripted APIs.

</td></tr><tr><td>

Version

</td><td>

**1.0** indicates the version of the API. You could have multiple versions of this API with different version numbers. Remember that in the step in the AWS Datacenter resource block that creates the VM, a Version field is provided. Although it was blank in this example because there is only one version of this API, you could specify a different version number.

</td></tr><tr><td>

Product

</td><td>

**AWS Elastic Compute Cloud** is the product that belongs to the AWS provider in CAPI. This product is provided by default with Cloud Provisioning and Governance, and is one of the most commonly used products for creating VMs on AWS.

</td></tr></tbody>
</table>    5.  In the CAPI Method Mappers related list, click the record preview icon for the **CreateNode** record, and then click **Open Record**.

        \[Omitted image "mystack-createnode-icon.png"\] Alt text: Open CreateNode method mapper

    6.  Look at the **CreateNode** method mapper:

        \[Omitted image "mystack-createnode-mapperform.png"\] Alt text: The Method Mapper form for CreateNode

        Notice that the Endpoint operation is not **Execute Script**. This value indicates that the CreateNode method is using a Java call within the Cloud Provisioning and Governance application on your instance to make a REST call to the AWS API. Therefore, you cannot modify how the CreateNode method works. If the value was **Execute Script**, you would see a MID Server script include specified in the **Request** script field. You would be able to modify that script include, or specify a new one, to customize the REST calls to the AWS provider.

    7.  Scroll down and look at parameters in the CAPI Parameter Mappers related list.

        Notice that important parameters, such as **Location**, are provided.

    8.  Navigate back to the AWS Compute API form.

    9.  Click the **API Config Overrides** related list, and review the items that are required for authentication:

<table id="table_otb_2z4_z2b"><thead><tr><th>

Config Parameter and Override Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AccountAliasName

 $\(CloudCredential.Alias\)

</td><td>

The account alias is an optional value that you can create in your AWS account. It is a secondary name for your account ID. See [the AWS documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/console_account-alias.html) for more information.

</td></tr><tr><td>

Credentials

 $\(CloudCredential.secret\_key\)

</td><td>

The secret key is used with the access key for authentication. You configured this value in your AWS credential record during setup. To refer to that procedure, see [Configure access to the AWS accounts using permanent AWS credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/aws-create-creds-cloud-mgt.md).

</td></tr><tr><td>

Endpoint

 $\(CloudCredential.URL\)

</td><td>

The endpoint is the URL that your users must log in to and authenticate. It uses the account ID or the account alias. See the [AWS documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_how-users-sign-in.html) for more information.

</td></tr><tr><td>

Identity

 $\(CloudCredential.access\_key\)

</td><td>

The Identify record holds the AWS access key, which AWS requires for authentication.

</td></tr></tbody>
</table>    10. Navigate back to **Design** &gt; **Cloud API**, and then click the **Interface** tab.

    11. Search for and open **Compute Interface**.

        This interface is the interface specified in the resource block and the **AWS Compute API** CAPI API.

    12. Review the contents of the interface.

        Notice that the interface provides REST response structures for methods like **CreateNode**. You typically do not need to modify existing interfaces.\[Omitted image "mystack-compute-interface.png"\] Alt text: CreateNode response structure highlight

        Note the service category and the operations:

        |Field or related list|Description|
        |---------------------|-----------|
        |Service Category|The service category classifies the interface. The category for the Compute Interface is also **Compute**.|
        |CAPI Interface Operations|The interface operations define the JSON structure for the REST call and the parameters that are required for the interface.|

    13. Click the **CreateNode** CAPI interface operation.

        This operation is the one that provides the framework for creating the EC2 virtual server in AWS.

    14. Review the components of the operation:

<table id="table_mbr_r2l_y2b"><thead><tr><th>

Field or related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response structure

</td><td>

The response structure is the JSON framework for REST API call. It provides a list of attributes that AWS can use to create the virtual resource with empty values.

</td></tr><tr><td>

Interface Operation Parameters

</td><td>

These parameters are also the parameters that the CAPI interface needs from the system so it can pass it in the REST call to the cloud provider.

</td></tr></tbody>
</table>        \[Omitted image "capi-interface-createnode.png"\] Alt text: The CreateNode operation

    15. Navigate back to **Design** &gt; **Cloud API**, and then click the **Provider** tab.

    16. Open the **AWS** provider.

        The AWS Provider form opens, showing you that this provider is based on an existing CMDB class: **AWS Datacenter \[cmdb\_ci\_aws\_datacenter\]**.

        \[Omitted image "capi-product-aws.png"\] Alt text: The AWS Provider

    17. Click the Cloud Products related list if it is not already selected, and sort the list by the **Name** column.

        Notice that several AWS products are already available by default. One of the most commonly used AWS products is **Elastic Compute Cloud \(EC2\)**.

        \[Omitted image "capi-product-ec2.png"\] Alt text: Amazon EC2

    18. Click **AWS Elastic Compute Cloud** in the **Name** column.

        Notice that the product specifies many resource types, each of which is mapped to a CI class.

        \[Omitted image "mystack-aws-product.png"\] Alt text: AWS product

        These resource types indicates the some of the CIs, but not all, that are related to the virtual machine. The response processor in the resource block populates CIs with data when AWS provisions the VM.

5.  To see the important CIs that are related to the VM:

    1.  On the Cloud User Portal, click **Stacks**, and then open the stack containing the VM.

    2.  Click the View Dependency icon.

        \[Omitted image "mystack-view-dependency.png"\] Alt text: Viewing the dependency

        The dependency map displays the stack CI at the top, the VM in the middle, and the various related CIs, such as the image, at the bottom.

        \[Omitted image "mystack-dependency-map.png"\] Alt text: The dependency map for a VM in a stack

    3.  To view the form for the VM in the CMDB, right-click the arrow next to any CI, such as the VM.

        \[Omitted image "mystack-vm-ci-arrow.png"\] Alt text: View a VM Ci

    4.  From the menu, select **View Form**.

        \[Omitted image "mystack-vm-ci-viewform.png"\] Alt text: View the CI form

        The CI form opens, showing you that much of the information is already available on the Cloud User Portal when you view the properties of the VM.

<table id="table_fkq_lbn_3yb"><thead><tr><th>

 

</th><th>

VM properties in the Cloud User Portal

</th></tr></thead><tbody><tr><td>

\[Omitted image "mystack-vm-ci-form-view.png"\] Alt text: VM form

</td><td>

\[Omitted image "mystack-vm-properties.png"\] Alt text: VM details

</td></tr></tbody>
</table>
**Parent Topic:**[Cloud Provisioning and Governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-configuration-governance/cloud-management-v2-landing-page.md)

