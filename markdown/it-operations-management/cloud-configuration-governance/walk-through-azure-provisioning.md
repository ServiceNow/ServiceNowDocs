---
title: Azure VM provisioning walkthrough
description: This example walks you through the components of Cloud Provisioning and Governance that function during the provisioning of a virtual machine in an Azure datacenter. Topics covered include blueprints, resource blocks, the Cloud API \(CAPI\), and MID Server script includes.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Azure VM provisioning walkthrough

This example walks you through the components of Cloud Provisioning and Governance that function during the provisioning of a virtual machine in an Azure datacenter. Topics covered include blueprints, resource blocks, the Cloud API \(CAPI\), and MID Server script includes.

## Before you begin

Role required: admin

## About this task

This walkthrough starts with a Linux VM that a user already provisioned in Azure. Next, it walks you through the blueprint with the VM, the resource blocks, and then the CAPI calls specified from the resource blocks. Finally, the walkthrough shows you how a MID Server script include eventually, through several CAPI calls, makes the actual REST calls to the Azure API.

This example uses default resource blocks and script includes that are available in your instance. Therefore, although you might not have a provisioned VM on your instance, you can still follow these steps and view the components used in this example to understand how the components work.

For an example of a VM in AWS, see [AWS VM provisioning walkthrough](walk-through-provisioning.md).

**Note:** The terms virtual machine, VM, and virtual server are used interchangeably in this example.

## Procedure

1.  Look at a provisioned VM in the Cloud User Portal, and focus on some of the details about the VM:

    1.  In the base system instance interface, open the Cloud User Portal \(**Cloud User Portal**\).

    2.  On the Cloud User Portal, view a provisioned VM in a stack, such as this VM, by clicking **Stacks**, and then clicking the name of the stack.

        In this example, the stack is named **MyAzureVM**.

    3.  Under **Resources**, click the VM in the stack.

        ![Virtual Server example](../image/myazurevm-vm.png)

    4.  View the properties of the VM, and notice that it is in an **Azure Datacenter** in region **eastus**.

        ![VM details](../image/myazurevm-vm-details.png)

2.  Look at the blueprint on which the VM is based:

    1.  Navigate to **Design** &gt; **Blueprints**, and then open a blueprint with a virtual server in the Azure datacenter. The **Deployment Model** tab appears by default, showing you the various components of the blueprint.

        This example blueprint has three components: the container, the virtual server, which is the actual VM that is provisioned, and the Azure datacenter.

        ![My Azure VM](../image/myazurevm-blueprint.png)

    2.  Click the **Operations** tab on the bottom, and then click **Provision**.

        ![Provision operation](../image/mystack-provision-block.png)

        The Provision operation is the operation that the system triggered when it created the VM. Other default operations are available, but this example focuses on the Provision operation.

    3.  Click the **Provision** block for Blueprint Container Resource.

        ![My Azure VM blueprint container](../image/myazurevm-provision-container.png)

    4.  On the right, notice that one of the parameters in the Inputs list is Location.

        This parameter holds the value eastus, which is where the VM lives in the datacenter.

        ![The Location parameter](../image/mystack-location-param.png)

        Inputs can be specified on the container, as it is in this example, or on any other resource block. By default, the **Location** parameter is already specified for you in the Blueprint Container resource block, so that you can use it in every blueprint like this one. If you switch the blueprint to **Draft**, you can add more parameters to the Blueprint Container resource block. You cannot add parameters to the Virtual Server resource block. For this walkthrough, no additional parameters are necessary.

3.  View the Virtual Server and Datacenter resource blocks used in this blueprint:

    1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Resource Blocks**.

    2.  Search for and open the **Virtual Server** resource block, which is provided by default with Cloud Provisioning and Governance.

        ![The default virtual server resource block](../image/rb-virtual-server-tile.png)

    3.  On the Resource Block form, click the **Host Resource** related list to view the list of supported host resource blocks.

    4.  Notice the host interface and host resource that are already specified:

        ![Azure resource block](../image/myazurevm-virtualserver-rb-interfaces.png)

        -   The **Host Interface** field specifies the interface that must match the guest interface in the resource block that hosts this virtual machine. In this case, the host interface is the Compute Interface, which is also the guest interface on the Azure Datacenter resource block. By default, the datacenter resource blocks provide several guest interfaces that other resource blocks like virtual storage can use to connect to the datacenter.
        -   The **HostResource** column in the **Host Resource** related list already specifies **Azure Datacenter**, which means that the Azure datacenter resource block is a valid host for this VM.
    5.  Click the **Operations** tab, and then click the **Steps** subtab.

        ![Selecting the Steps subtab](../image/mystack-operations-steps.png)

    6.  Select **Provision** from the **Operation** list.

        ![The Provision operation](../image/mystack-operations-provision.png)

        Remember that the Provision operation is the operation that the system used to create the VM. Other default operations are available, but this example focuses on the Provision operation.

    7.  Notice the step that appears in the list and the full step description that appears above the input parameters:

        ![Step for Provision](../image/mystack-provision-step.png)

        -   **Host Resource Operation:** indicates that this step calls an operation on the host resource \(the Azure datacenter in this example\).
        -   **Compute Interface** is the guest interface on the Azure datacenter that this step is using.
        -   **ConnectAndCreateVirtualMachine** is the operation in the Azure datacenter that this step calls.
        **Note:** In this case, the step calls an operation from another resource block: the Azure datacenter. Steps can also call CAPI directly, and then CAPI can execute REST calls to the cloud provider API. You can see that when you look at the Azure datacenter resource block.

    8.  Navigate back to **Design** &gt; **Resource blocks**.

    9.  Open the **Azure Datacenter** resource block, which is the host resource block that the virtual server is connected to.

    10. Notice the supported guest interfaces in the **Guest Interface** related list:

        ![Azure datacenter with Compute API](../image/myazurevm-rb-guest-interface.png)

        These guest interfaces are the interfaces that the Azure datacenter makes available to other resource blocks. The **Compute Interface** is provided so that the Virtual Server resource block, which specifies the Compute Interface as its host interface, can connect to the datacenter.

    11. Click the **Operations** tab, and then click the **Steps** subtab.

        ![Selecting the Steps subtab](../image/mystack-operations-steps.png)

    12. In the **Interface** list, select **Compute Interface** if it is not already selected.

        ![Compute interface](../image/mystack-awsdatacenter-compute.png)

        Remember that this interface is specified in the Virtual Server resource block.

    13. In the **Operation** list, search for and select **ConnectAndCreateVirtualMachine**.

        ![The ConnectAndCreateVM operation](../image/mystack-connectandcreate-operation.png)

        Remember that this operation is specified in the Virtual Server resource block.

    14. Notice the CAPI call that is used in the only step for the ConnectAndCreateVirtualMachine operation:

        ![The CreateNode API call](../image/mystack-awsdatacenter-createnode.png)

        -   **Cloud API:** indicates that this step calls CAPI, so that CAPI can execute a REST call to the cloud provider, which in this case is Azure.
        -   **Compute Interface** specifies the CAPI interface that this step calls.
        -   **CreateNode** indicates the method that is executed. As the name suggests, this method tells the cloud provider to create the virtual machine.
    15. To open the step configuration: With the resource block in the **Draft** state, point to the highlighted \(blue\) step, and then click the **Edit Step** icon that appears.

        ![Edit step](../image/mystack-edit-step.png)

    16. Look at the step configuration and notice the settings that integrate with CAPI:

        ![Edit steps](../image/myazurevm-edit-steps.png)

        |Field|Description|
        |-----|-----------|
        |Operation Type|**Invoke Cloud API** specifies that this step should call the CAPI via the specified provider, interface, and method.|
        |API Provider \(which is actually the product\)|**Microsoft.Compute** is a product \(not the actual provider\) that belongs to the Azure provider as defined in CAPI.|
        |API Interface|**Compute Interface** is a product that belongs to the Azure provider as defined in CAPI.|
        |API Method|**CreateNode** is the method that calls Azure to create the VM.|

        **Note:** The CAPI API definition ties together the provider \(Azure\), the product \(Microsoft.Compute\), the interface \(Compute Interface\), and the method \(CreateNode\).

    17. Close the window.

    18. With the **Compute Interface.CreateNode** step selected, click the **Response Processor** tab, and notice the **Create\_Virtual\_Server\_Response\_Processor** script.

        ![Response Processor tab](../image/mystack-response-processor.png)

        This script is the response processor that updates the CMDB in your instance after the virtual machine is created.

    19. View an explanation of the script and the example that is a part of the topic at [Create a Response Processor](../reference/response-processor-example.md).

        When you finish reviewing that topic, return to this topic.

4.  Look at the CAPI components that work together to provision the VM:

    1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API**.

    2.  Click the **API** tab and then search for an open **Azure Compute API**.

    3.  Look at how this CAPI API ties together an interface and a product:

        ![Azure Compute API](../image/myazurevm-azure-compute.png)

        |Field|Description|
        |-----|-----------|
        |Cloud API Interface|**Compute Interface** is the same interface that you can see specified in the resource block. The interface contains the definition for methods, including the **CreateStack** method.|
        |Connector|**Script Connector** indicates that this CAPI provides a MID Server script include for each operation. The script include calls the API. You can modify the script include or even create a new one.|
        |Version|**1.0** indicates the version of the API. You could have multiple versions of this API with different version numbers. Remember that in the step in the datacenter resource block that creates the VM, a Version field is provided. Although it was blank in this example because there is only one version of this API, you can specify a different version number.|
        |Product|**Microsoft.Compute** is the product that belongs to the provider in CAPI. This product is provided by default with Cloud Provisioning and Governance, and is one of the most commonly used products for creating VMs on Azure.|

    4.  In the CAPI Method Mappers related list, click the record preview icon for the **CreateNode** record, and then click **Open Record**.

        ![The CreateNode method mapper](../image/myazurevm-createnode-mapper.png)

    5.  Look at the **CreateNode** method mapper:

        ![CreateNode mapper form](../image/myazurevm-createnode-mapper-form.png)

        Notice that the **Endpoint operation** is **Execute Script**, which indicates that a customizable script include is used to call functions in CAPI, which eventually makes the REST calls to Azure. The **azure-compute-1.0-CreateNode** MID Server script include is specified in the **Request script** field.

        This graphic illustrates how the components — from the resource block to the script include — are connected:

        ![Azure datacenter script include](../image/myazurevm-rb-to-scriptinclude.png)

    6.  Click the record icon \(![Record icon](../image/icon-record.png)\) for the **Request script**.

        The **azure-compute-1.0-CreateNode** MID Server script include opens.

    7.  Review the contents of the script.

        ```
        
        createNode();
        function createNode(){
           var acp = new AzureComputeVirtualMachine(this.parameters, this.headers);
           var vm = acp.createVirtualMachine();
        
           return vm;
        }
        
        ```

        The script calls the **createVirtualMachine** function in the **AzureComputeVirtualMachine** class. It returns the virtual machine that is created. The **AzureComputeVirtualMachine** class extends **AzureCloudAPIBase**, which is one of the base APIs in Cloud Provisioning and Governance.

    8.  To see the **AzureComputeVirtualMachine** class, which is a MID Server script include, open the base system instance interface \(not the Cloud Admin Portal\), and then navigate to **MID Server** &gt; **Script Includes**.

    9.  Search for and open **AzureComputeVirtualMachine**.

        ![Search for an open a script include](../image/myazurevm-search-scriptinclude.png)

    10. Review the `createVirtualMachine` function:

        The function defines many variables that are required to create a VM, including the **Location** \(datacenter\) and the name of the VM, and so on.

        ```
         
        var location = this.parameters.get('Location');  
        var vmName = this.parameters.get('NodeName');
        ...
        
        ```

        This line of code calls the `_performVMOperation` function in this same script include and passes in the parameters that are necessary. Notice that an empty value `''` is passed for the `action` parameter:

        ```
        var response = this._performVMOperation(subscriptionId, resourceGroup, vmName, '', 'PUT', jsonObj.encode(params));
        ```

        The `_performVMOperation` function calls the function `_invokeRequest`, which is located in the **AzureCloudAPIBase** class:

        `return this._invokeRequest(this.pathDefault, param, method, requestBody);`

        The PUT method for the REST call is specified in the **method** parameter.

        Look at the **AzureCloudAPIBase** MID Server script include. The `_invokeRequest` function first calls the `_getEndpoint` function to get the endpoint and the `_getAPIInvoker` function to identify the **AzureAPIInvoker** class as the class that invokes the actual PUT call:

        `var apiInvoker = this._getAPIInvoker(apiEndpoint, this.apiVersion);`

        **AzureAPIInvoker** is extended from **CloudRESTAPIInvoker**, which provides the base functions for all invokers. Once the correct invoker class is identified, a **response** variable is created to hold the value returned from `invokePut` function in the **CloudRESTAPIInvoker**:

        ```
        response = apiInvoker.invokePut(requestBody);
        ```

        Look at the **CloudRESTAPIInvoker**, which is the base class for all invokers. The **invokePut** function specifies the PUT method and calls `getRequest`, and it returns the response from the **getResponse** function, which gets a status code and the response from Azure. This invoker class is where the connection to Azure is made.

        Return to the **AzureComputeVirtualMachine** MID Server script include and find these lines:

        ```
        
        var response = this._performVMOperation(subscriptionId, resourceGroup, vmName, '', 'PUT', jsonObj.encode(params));  
        this._compareVMState(response.id, 'PowerState/running');  
        var nodeResponse = this.getVirtualMachine(response.id);
        
        ```

        Remember that the variable **response** is returned from the call to `_performVMOperation`, which has the response from the API invoker that triggered the PUT method. The **nodeResponse** variable holds the response from the `getVirtualMachine` function, which is passed the ID of the virtual machine that is in the response. The `getVirtualMachine` function calls `_getVMInfo`, which calls the same `_invokeRequest` function that was called earlier. This call is another connection to the invoker, which performs the actual REST calls. In this case, the REST call is a GET REST call to Azure to obtain the identify of the VM.

        The `return nodeResponse;` line returns **nodeResponse** in the `createVirtualMachine` function, which was called from the MID Server script include on the **createNode** operation.

        This graphic illustrates the classes involved:

        ![Azure calls](../image/myazurevm-class-calls.png)

    11. Navigate back to the Azure Compute API form.

    12. Click the **API Config Overrides** related list, and review the items that are required for authentication.

<table id="table_otb_2z4_z2b"><thead><tr><th>

Config Parameter and Override Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ClientID

 $\(CloudCredential.client\_id\)

</td><td>

The client ID is necessary to identify the application in Azure.

</td></tr><tr><td>

EndpointURL

 $\(CloudCredential.URL\)

</td><td>

The endpoint URL is the authorizing input in Azure.

</td></tr><tr><td>

SecretKey

 $\(CloudCredential.secret\_key\)

</td><td>

The secret key is used to authorize the client.

</td></tr><tr><td>

TenantID

 $\(CloudCredential.tenant\_id\)

</td><td>

The tenant ID is the globally unique identifier for your tenant.

</td></tr><tr><td>

EnrollmentNumber

 $\(CloudCredential.sn\_cmp\_ea\_credential.enrollment\_number\)

 EnrollmentToken

 $\(CloudCredential.sn\_cmp\_ea\_credential.access\_key\)

</td><td>

Azure enrollment number and the token to access the enrollment account.

</td></tr></tbody>
</table>        See [Store the Azure service principal credentials in the instance](../../cloud-management-v2-setup/task/azure-create-creds-cloud-mgt.md) for more information on the Azure information that is used in these overrides.

    13. Navigate back to **Design** &gt; **Cloud API**, and then click the **Interface** tab.

    14. Search for and open **Compute Interface**.

    15. Review the contents of the interface.

        Notice that the interface provides REST response structures for methods like **CreateNode**. You typically do not need to modify existing interfaces.

        ![CreateNode response structure highlight](../image/mystack-compute-interface.png)

        Note the service category and the operations:

        |Field or related list|Description|
        |---------------------|-----------|
        |Service Category|The service category classifies the interface. The category for the Compute Interface is also **Compute**.|
        |CAPI Interface Operations|The interface operations define the JSON structure for the REST call and the parameters that are required for the interface.|

    16. Click the **CreateNode** CAPI interface operation.

        This operation is the operation that provides the framework for creating the EC2 virtual server.

    17. Review the components of the operation:

<table id="table_mbr_r2l_y2b"><thead><tr><th>

Field or related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response structure

</td><td>

The response structure is the JSON framework for REST API call. It provides a list of attributes that the provider can use to create the virtual resource with empty values.

</td></tr><tr><td>

Interface Operation Parameters

</td><td>

These parameters are also the parameters that the CAPI interface needs from the system so it can pass it in the REST call to the cloud provider.

</td></tr></tbody>
</table>        ![The CreateNode operation](../image/capi-interface-createnode.png)

    18. Navigate back to **Design** &gt; **Cloud API** and then click the **Provider** tab.

    19. Open the **Azure** provider.

        The Azure Cloud Provider form opens, showing you that this provider is based on an existing CMDB class: **Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]**.

    20. Click the Cloud Products related list, and sort the list by the **Name** column.

        Notice that several Azure products are available by default. One of the most commonly used Azure products created from templates is **Microsoft.Compute**.

        ![Microsoft.Compute](../image/myazurevm-microsoftcompute.png)

    21. Click **Microsoft.Compute** in the **Name** column.

        Notice that the product specifies many resource types, each of which is mapped to a CI class.

        ![Resource types](../image/myazurevm-microsoftcompute-resourcetypes.png)

        These resource types indicates some of the CIs, but not all, that are related to the virtual machine. The response processor in the resource block populates CIs with data when the cloud provider provisions the VM.

5.  To see the important CIs that are related to the VM:

    1.  On the Cloud User Portal, click **Stacks**, and then open the stack containing the VM.

    2.  Click the **View Dependency** icon.

        ![Viewing the dependency](../image/mystack-view-dependency.png)

        The dependency map displays the stack CI at the top, the VM in the middle, and the various related CIs, such as the image, at the bottom.

        ![Dependency Map](../image/myazurevm-dependencymap.png)

    3.  To view the form for the VM in the CMDB, right-click the arrow next to any CI.

        ![View a VM Ci](../image/mystack-vm-ci-arrow.png)

    4.  From the menu, select **View Form**.

        ![View the CI form](../image/mystack-vm-ci-viewform.png)

        The CI form opens, showing you much of the information is already available on the Cloud User Portal when you view the properties of the VM.

<table id="table_wjv_jbn_3yb"><thead><tr><th>

The VM CI form

</th><th>

VM properties in the Cloud User Portal

</th></tr></thead><tbody><tr><td>

![Azure VM form](../image/myazurevm-vm-ci-form-view.png)

</td><td>

![VM properties](../image/myazurevm-vm-properties.png)

</td></tr></tbody>
</table>
**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

