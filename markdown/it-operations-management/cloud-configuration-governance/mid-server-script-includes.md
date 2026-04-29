---
title: CAPI classes in MID Server script includes
description: Cloud Provisioning and Governance provides several JavaScript classes that make REST calls to cloud providers. These classes are called from MID Server script includes \(for Azure by default\) or from Java calls in the system \(for AWS by default\). If you create custom providers, interfaces, or CAPI APIs \(for any cloud provider\), you can use MID Server script includes to call the classes.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# CAPI classes in MID Server script includes

Cloud Provisioning and Governance provides several JavaScript classes that make REST calls to cloud providers. These classes are called from MID Server script includes \(for Azure by default\) or from Java calls in the system \(for AWS by default\). If you create custom providers, interfaces, or CAPI APIs \(for any cloud provider\), you can use MID Server script includes to call the classes.

**Note:** In CAPI APIs, there are no MID Server script includes \(in Method Mappers\) that you can customize to call the AWS classes. By default, the CAPI APIs for AWS make Java calls to then call the AWS classes. However, if you create CAPI APIs, you can also create custom script includes to call the classes.

View CAPI classes by navigating to **MID Servers** &gt; **Script Includes** in the base system instance interface \(not the Cloud Admin Portal\). You search for the name of a class in the **Go to** search box using the **Name** column:

![Searching for MID Server script includes](../image/capi-classes-finding.png)

## Base classes

These base classes are available by default. They form a basis for the Azure and AWS classes that make the actual REST calls.

-   **CloudAPIBase**

    CloudAPIBase is a provider-agnostic API that communicates with all types of cloud APIs. It provides functions for basic debugging and logging, and for collecting proxy information on the MID Server. It also defines Headers, Parameters, Endpoints, and `this.parameter`.

-   **AWSCloudAPIBase**

    This class is extended from CloudAPIBase and provides functions that call the invoker to make GET, PUT, POST, and DELETE requests. The class provides the option of an `executeAction` method, which is an AWS implementation of GET, or the invoke method, which provides REST API calls.

-   **AzureCloudAPIBase**

    This class is extended from CloudAPIBase and provides functions that do these actions:

    -   Fetch resource IDs.
    -   Fetch endpoint properties.
    -   List resources.
    -   Call the invoker to make GET, PUT, POST, and DELETE requests.

AzureCloudAPIBase utilizes the `_invokeRequest` method to make REST API calls to Azure using the standard REST API calls.

![CloudAPIBase](../image/capi-cloudapibase.png "Base APIs")

## Invoker classes

Invoker classes perform the actual REST calls to the cloud provider. If you create a custom CAPI interface and API, you should extend **CloudRestAPIInvoker** to create your REST calls.

-   **CloudRestAPIInvoker**

    This class is an abstracted class for making REST API calls. If there are headers and/or parameters to send with a request, classes that implement the invoker must extend this object. They also must provide overrides for **getEndpointUrl** to return the targeted endpoint, and for **getHeaders** and **getParameters**. For example, with Azure REST APIs, authentication requires the passing of a token as a header. The extension implementing it should provide a response from **getHeaders** that performs the token creation or retrieval and sets it. This base object invokes **getHeaders** and sends whatever it gets back with the request. This class also provides a **getResponse** method to handle the response from the cloud provider.

    If you create a custom CAPI API, you should extend **CloudRestAPIInvoker** to make REST calls to the cloud provider.

-   **AmazonWebServicesAPIInvoker**

    This class is extended from **CloudRestAPIInvoker** and provides methods for making REST API calls to the cloud provider.

-   **AzureAPIInvoker**

    This class is extended from **CloudRestAPIInvoker** and provides functions that make these REST API calls to Azure Resource Manager:

    -   Sets the Service Principal, headers, and parameters for REST calls.
    -   Gets the endpoint URL, token \(client ID, tenant ID, and secret key\), and headers/parameters.
    -   Retrieves and decodes the JSON response body from the cloud provider.
-   **AzureEAAPIInvoker**

    This class returns the token for access to the Azure Enterprise Agreement \(EA\) REST API.

-   **AzureStorageAPIInvoker**

    This class makes REST calls for Azure storage. The functions in this class can get the token, response, headers, and parameters.


This graphic illustrates how these base classes are used to extend AWS-specific and Azure-specific classes:

![CloudRestAPIInvoker](../image/capi-cloudrestapiinvoker.png "Invoking REST calls")

## Exceptions

-   **RESTAPIException**

    This base class handles exceptions that might occur during the REST call. It returns the response code from the cloud provider.

-   **AWSAPIException**

    This class handles exceptions that might occur during the REST call.

-   **AzureAPIException**

    This class throws a runtime exception when needed during Azure API invocation.


![RESTAPIException](../image/capi-restapiexception.png "Handling exceptions")

## Classes for credentials

-   **CloudRESTRequestSigningUtil**

    This class uses overrides that are specified in CAPI API Config Overrides. The **AmazonWebServicesRequestSigner** class extends this class. For Azure, many signers are built into the MID Server script includes for Method Mappers in Azure CAPI APIs.

-   **AmazonWebServicesRequestSigner**

    This class sets up a secure session for the REST API call by taking information about a request, and creating a [signature v4](http://docs.aws.amazon.com/general/latest/gr/sigv4_signing.html)-signed string for the request. This class is extended from CloudRESTRequestSigningUtil.


## Other Azure classes

|Class|Description|
|-----|-----------|
|AzureAlertRule|Class to create and delete Azure alert rules.|
|AzureAuthorizationPolicy|Class to assign tag policies.|
|AzureComputeAvailabilitySet|Class to fetch Azure availability sets. Refer to: https://docs.microsoft.com/en-us/rest/api/compute/availabilitysets|
|AzureComputeHardware|Class to fetch Azure sizes. Refer to: https://docs.microsoft.com/en-us/rest/api/compute/virtualmachinesizes|
|AzureComputeImage|Class to handle Azure API calls against image. Refer to: https://docs.microsoft.com/en-us/rest/api/manageddisks/images/images-rest-api|
|AzureComputeVirtualMachine|Class to handle Azure API calls against virtual machines. Refer to: https://docs.microsoft.com/en-us/rest/api/compute/virtualmachines VM Size and Capacities: https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-windows-sizes https://docs.microsoft.com/en-us/azure/virtual-machines/virtual-machines-linux-sizes Cloud-Init supported Versions: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/using-cloud-init|
|AzureDeployment|Class to handle Azure ARM template deployment.|
|AzureDeploymentOperation|Class to handle Azure ARM template deployment operation.|
|AzureImages|Class to handle Azure Images.|
|AzureLoadBalancer|Class to handle Azure API calls against load balancers. Refer to: https://msdn.microsoft.com/en-us/library/azure/mt163651.aspx|
|AzureLocalNetworkGateways|Class to create and retrieve local network gateways.|
|AzureNetworkNIC|Class to handle Azure API calls against network interface cards. Refer to: https://msdn.microsoft.com/en-us/library/azure/mt163579.aspx|
|AzureNetworkPublicIP|Class to handle Azure API calls against public IP addresses. Refer to: https://msdn.microsoft.com/en-us/library/azure/mt163638.aspx|
|AzureNetworkRouter|Class to handle Azure API calls against route table. Refer to: https://docs.microsoft.com/en-us/rest/api/network/route-tables|
|AzureNetworkSecurityGroup|Class to handle Azure API calls against network interface cards. Refer to: https://msdn.microsoft.com/en-us/library/azure/mt163579.aspx|
|AzureNetworkVirtualNetwork|Class to handle Azure API calls against virtual networks.|
|AzureProvider|Class to get Azure provider details, such as the provider URL and version.|
|AzureRegion|Class to fetch Azure regions.|
|AzureResource|Deals with the object referenced by ObjectID in the parameters. It also fetches the API version. This class is Intended mostly to get unsupported types or delete resources.|
|AzureResourceGroupManager|Class to handle Azure ARM resource groups.|
|AzureResponseUtil|Class to translate Azure API response to DTO object.|
|AzureStorageAccount|Class to handle Azure API calls against storage account. Refer to: //https://msdn.microsoft.com/en-us/library/azure/mt163638.aspx|
|AzureStorageBlob|Class to create and manipulate storage containers and blobs.|
|AzureStorageManagedDisk|Class to handle Azure API calls against managed disk. Refer to: https://docs.microsoft.com/en-us/rest/api/manageddisks/disks/disks-create-or-update|
|AzureSubscription|Class to fetch Azure subscriptions.|
|AzureVirtualNetworkGateways|Class to create and manipulate virtual network gateways.|
|AzureCloudEAAPIBase|Base object for Azure EA API handlers. Azure EA APIs have a base URL of https://consumption.azure.com and require the enrollment number in the path. This class handles marshalling of the EnrollmentNumber and EnrollmentToken parameters.|

## Other AWS classes

<table id="table_dct_f3x_2fb"><thead><tr><th>

Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AmazonImages

</td><td>

Class to handle Amazon machine images.

 http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html

</td></tr><tr><td>

AmazonResponseProcessorUtil

</td><td>

Class to handle AWS REST API response.

</td></tr><tr><td>

AWSAutoScalingGroups

</td><td>

Class to handle AWS API calls to create and manipulate [Auto Scaling Groups](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_CreateAutoScalingGroup.html).

</td></tr><tr><td>

AWSCloudFormation

</td><td>

Handler for AWS CloudFormation API calls.

</td></tr><tr><td>

AWSEC2

</td><td>

Handler for AWS EC2 API calls.

</td></tr><tr><td>

AWSKeyValuePair

</td><td>

Class to import and manipulate key pairs.

</td></tr><tr><td>

AWSLaunchConfigurations

</td><td>

Helper class.

</td></tr><tr><td>

AWSS3

</td><td>

Handler for AWS S3 API calls.

</td></tr><tr><td>

AWSTopics

</td><td>

Class with [AWS topics](http://docs.aws.amazon.com/sns/latest/api/API_ListTopics.html).

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Provisioning and Governance](cloud-management-v2-landing-page.md)

