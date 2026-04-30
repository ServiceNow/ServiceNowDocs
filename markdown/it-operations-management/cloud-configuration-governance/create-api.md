---
title: Create a CAPI API
description: If the existing CAPI APIs do not integrate with the CAPI interface for a provider, you can create an API. The steps in resource blocks can call your API methods when operations are executed.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a CAPI API

If the existing CAPI APIs do not integrate with the CAPI interface for a provider, you can create an API. The steps in resource blocks can call your API methods when operations are executed.

## Before you begin

-   Role required: admin
-   Review [Default CAPI APIs](../reference/default-apis.md) and make sure the provider and product that you are creating do not exist.
-   Familiarize yourself with the cloud provider API so that you know how to create REST calls to the provider. If you are not familiar with the headers, authentication requirements, endpoint, and data that you can pass into the provider API, you cannot build your own CAPI components.

## About this task

This topic provides instructions for creating a CAPI API. It also cover the configuration of CAPI, resource blocks, blueprints, and credential mappings.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API**.

2.  Click the **API** tab.

3.  Click **New**.

4.  Fill out the form fields \(see table\):

<table id="table_ib1_q1k_v2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cloud API

</td><td>

Provide a descriptive name.

</td></tr><tr><td>

Interface

</td><td>

Select from among the existing interfaces that provide the operations you need.

</td></tr><tr><td>

Connector

</td><td>

**Script Connector** appears in this field if the connector is a Java connector that is available out-of-box and cannot be modified. You do not need to modify these script connectors.

</td></tr><tr><td>

Product

</td><td>

Select the product that is part of the provider. The product includes resource types in the CMDB.

</td></tr><tr><td>

Version

</td><td>

Provide a version number to identify this API. Enter `1.0` if this API is the first version. You can create several versions of the same API and then refer to the specific versions in the operation steps of resource blocks.

</td></tr><tr><td>

Scripted

</td><td>

This field is selected if the **Interface** value is **Script Connector**.

</td></tr><tr><td>

Script Type

</td><td>

Select the language for the script. **Note:**

JavaScript is recommended. The method mappers use MID Server script includes written in Javascript.

</td></tr><tr><td>

ExecuteScriptOnInstance

</td><td>



</td></tr><tr><td>

Description

</td><td>

Provide a description for this API.

</td></tr></tbody>
</table>5.  Verify that all the operations you need appear in the **CAPI Method Mappers** related list.

    The operations in the CAPI Method Mappers list are the same operations in the interface that you selected. They are bound to this API. You cannot add or remove any operations from the list. Some of the operations, especially Azure operations, use MID Server script includes that perform the actual implementation for the API. The script includes a call to the REST API for the provider, such as AWS or Azure. You should be able to find the API in the provider's documentation.

6.  To see the script include for a CAPI Method Mapper:

    1.  Click the gear icon \(![Gear icon](../image/icon-gear-blue.png)\) on the **CAPI Method Mappers** related list, add the **Request Script** field to the **Selected** column, and then click **OK**.

        ![Add the Request Script field](../image/add-request-script.png)

        The MID Server script includes now appear in the list of method mappers.

    2.  Click the name of a script to view the script include.

        In this example, the **CreateNode** operation uses the **azure-compute-1.0-CreateNode** script include.

        ![CreateNode example](../image/capi-createnode-api-example.png)

        That script include contains the following code:

        ```
        
        createNode();
        function createNode(){
           var acp = new AzureComputeVirtualMachine(this.parameters, this.headers);
            //this passes the parameters and headers into the AzureComputeVirtualMachine script include.
           var vm = acp.createVirtualMachine();
        
           return vm;
        }
        
        ```

        Notice that the code calls the **AzureComputeVirtualMachine** script include, which is available by default with the Cloud Provisioning and Governance application. It contains all the API calls to Azure against virtual machines.

7.  Create an API config override to pass the necessary credential information to the cloud provider.

    You also need to pass header information required by the cloud provider REST API. API config overrides are necessary because credential data is not included when your instance makes the REST call to the cloud provider API.

    **Tip:** If you do not know which API config overrides to create, look at a similar API that exists in CAPI, and use the same overrides. For example, if you are creating an API for something like AWS storage, look at other AWS APIs such as AWS Block Storage or AWS Compute.

    1.  In the API Config Override related list, click **New**.

    2.  Click the lookup icon and select an existing config parameter.

        Many useful parameters are provided by default, such as **Identity**, **Credentials**, and so on.

    3.  Enter an **Override value**.

        You can set a static value, or you can pull a value from the system in the form of `$(CloudCredential.attribute_name)`. The `CloudCredential` portion unlocks it from the credential store. The `attribute_name` portion is an attribute that depends on the particular credential or alias or endpoint URL that you are trying to retrieve.

        If you navigate to **Connections and Credentials** &gt; **Credentials** and open your AWS credential, you can right-click the **Access Key ID** field and see the name of the column in the Credentials table where the access key is stored. In this case, the access key is stored in the `access_key` column. So your Override value should be `$(CloudCredential.access_key)`.

        ![An access key](../image/access-key-field.png)

8.  If you need to create a configuration parameter to use in the API Config Override, follow this procedure:

    1.  On the API Config Override form, click the lookup icon in the **Config Parameter** field.

    2.  Click **New** on the Configuration Parameter window and then fill in the form.

<table id="table_fbs_y4b_n2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Config parameter name

</td><td>

Enter a descriptive name.

</td></tr><tr><td>

Default value

</td><td>

Set an optional default value.

</td></tr><tr><td>

Endpoint

</td><td>

This field is read only.

</td></tr><tr><td>

Description

</td><td>

Enter a helpful description.

</td></tr><tr><td>

Config data type

</td><td>

Select the type of data: -   **String**
-   **DateTime**
-   **Date**
-   **Long**
-   **Password**
-   **Boolean**


</td></tr><tr><td>

Config type

</td><td>

Select the type of configuration:-   Header: Use this value to pass the override values as headers. If your have a MID Server script include as part of your API and it uses `this.headers` as a parameter, the override values are passed to the provider API.
-   Config
-   URI Config


</td></tr></tbody>
</table>9.  If necessary, modify the script includes that execute the operations against the cloud provider API:

    1.  On the Cloud API form, in the CAPI Method Mappers related list, click the information icon \(![Information icon](../image/icon-information.png)\) next to the CAPI interface operation.

        Do not click the CAPI Interface Operation name itself.

    2.  Click **Open Record**.

    3.  On the operation form, you can modify the following field values:

<table id="table_y4k_xyb_n2b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Endpoint operation

</td><td>

Keep the default **Execute Script** endpoint operation.

</td></tr><tr><td>

Supported in version

</td><td>

You typically do not need to change this value.Change the **Supported in** version to use the method mapper in a different version of the API. By default, the method mappers are set to the same version number as the API they belong to.

</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>    4.  In the **Request Script** field, click the information icon \(![Info icon](../image/icon-information-other.png)\) next to the placeholder MID Server script include to modify it.

    5.  On the script include form, create your script.

        The following example JavaScript lists Azure load balancers. Note the helpful comments:

        ```
        
        getResourceInfo();
        
        function getResourceInfo() {
        	var anpi = new AzureLoadBalancer(this.parameters, this.headers);
               
               //this calls the 'AzureLoadBalancer' MID Server script include, which in turn
               //calls the 'AzureCloudAPIBase' script include, both of which 
               //are already in your instance by default. 
               //The 'AzureCloudBase' script include runs a query for resources of a given type in a
        	//specified region.
        
        	var items = anpi.listResourcesByRegionOrIDs();
               //This function is in the 'AzureCloudAPIBase' script include. It calls the Azure API.
        
        	return items;
        }
        
        ```

        The overrides provided for this operation are what Azure needs to find the load balancers: the Client ID, Tenant ID, the Secret Key, and the Endpoint URL:

        ![API Config Overrides](../image/capi-azure-lb-overrides-example.png)

        For the Google Cloud integration example, a MID Server JAR file is also needed.

    6.  Click **Submit**.

    7.  Modify the script include for each operation.


**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

