---
title: Cloud API \(CAPI\)
description: The Cloud API \(CAPI\) enables you to integrate Cloud Provisioning and Governance with cloud providers using REST APIs.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud API \(CAPI\)

The Cloud API \(CAPI\) enables you to integrate Cloud Provisioning and Governance with cloud providers using REST APIs.

## CAPI components

Integration with cloud providers is performed through REST calls, such as PUT, GET, POST, and DELETE. CAPI provides the framework for you to integrate a cloud vendors REST API so that your instance can communicate with the cloud provider to manage cloud resources.

See [Browse APIs by product](https://www.servicenow.com/docs/access?context=api-product-type&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) to learn more.

CAPI contains these components:

![CAPI overview](../image/capi-overview.png "CAPI overview")

-   **Providers**

    Cloud providers are the clouds that you can connect to. By default, Cloud Provisioning and Governance includes the most commonly used providers, such as AWS, Azure, and VMware. Each provider has many products, each of which provide resource types. Each resource type maps to a single CI type. For example, the **AWS provider** includes the **AWS Elastic Compute Cloud** product, which includes the **AWS::EC2::Instance** resource type. This resource type is one of the most common cloud resources that you can create. It maps directly to the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] CI type, where virtual machines are saved in the CMDB.

-   **Interfaces**

    Interfaces define the framework that the system needs to structure the REST calls that the cloud provider APIs expect. Interfaces define operations, also called methods, and the parameters that each method requires.

    Interfaces are reusable. If you extend CAPI to include new products and APIs, you can use existing interfaces to make the same REST calls.

-   **APIs**

    CAPI APIs are the core component of CAPI that ties a product and interface together. The APIs include the actual code that the system executes.

    Each CAPI API includes these components:

    -   CAPI Method Mappers provide the methods that are mapped to the operations defined in the interface. From CAPI method mappers, you create MID Server script includes in JavaScript to tell the cloud provider exactly what to do. It is through the script includes that the connection to the cloud provider occurs.

        **Note:** If you create custom CAPI APIs, the system provides an empty script include for you to customize. You can also modify existing script includes on method mappers if necessary. However, many of the default APIs that come with the Cloud Provisioning and Governance application do not use modifiable script includes. The connections are hard-coded in Java. You can still use these APIs in new resource blocks that you create, but you cannot modify the APIs.

    -   API Config Overrides contain the identity, such as a key, and credentials, such as the secret key, and other important parameters required by the cloud provider. These parameters help the cloud provider perform the operations in the CAPI Method Mappers related list. API Config Overrides are necessary because, when the system calls the cloud provider API via REST, credential data is not included. Resource blocks use the parameters and values that you define in the API Config Overrides to query the credential store. When your API executes, the attributes are made available to all method calls in your script includes.

        The overrides are scoped only for this API. The overrides do not override anything in other APIs.

    Because you can define multiple versions of a CAPI API with slight variations, you can extend \(without overwriting\) an existing API while retaining desired functionality.


This image illustrates the components of CAPI that are used when you provision an Azure virtual machine using the default CAPI settings provided with Cloud Provisioning and Governance:

![CAPI Azure](../image/capi-example.png "CAPI Azure")

In this example, the **Microsoft.Compute** product is contained in the **Azure** provider. Azure uses the **Microsoft.Compute** product for virtual machines. In your instance, the **Microsoft.Compute** product maps to the **Microsoft.Compute/virtualMachines** resource type, which is associated to the **Virtual Machine Instance** CI type in the CMDB.

The **Compute** interface contains definitions for methods like **CreateNode**, which defines how to create the actual virtual machine. Of the many parameters that **CreateNode** uses, **Location** captures the datacenter where the virtual machine resides.

The **Azure Compute API** pulls together the **Microsoft.Compute** product and the structure defined in the **Compute** interface. The implementation of the **CreateNode** method calls the **azure-compute-1.0-CreateNode** MID Server script include, which calls the **AzureComputeVirtualMachine** MID Server script include. The script includes make the actual calls to the Azure API. To access the Azure account, the **SecretKey**, **ClientID**, **TenantID**, and other methods are passed in Config Overrides.

## How CAPI integrates with the instance

CAPI integrates these components in your instance:

-   **Cloud Provisioning and Governance resource blocks**

    A resource block represents a single cloud resource, such as a virtual server, virtual server storage, or a datacenter. You can also think of it as a CI type in the CMDB. You put many resource blocks together in a blueprint, which appears as a catalog item \(also called a stack\) to your users in the Cloud Catalog.

    In the system, each resource block is like a container that references CAPI, and links responses from the cloud provider to a specific CI. Resource blocks use:

    -   Operational steps that call CAPI for each operation, such as the provision operation, and pass along necessary parameter values that the cloud provider needs to execute the operation.
    -   Response processors that process and parse the REST response from the provider and update records in the CMDB.
-   **The CMDB**

    Each resource block is based on a CI type from the CMDB. For Cloud Provisioning and Governance, all cloud-related CI types are based on the **Virtual Machine Object CI** class, which provides all the attributes that you need for all the cloud resources supported by default. If a CI type for a cloud resource does not exist in the base system, you must create a new CI class and add the necessary attributes.

    If you do create a new CI class, you must also create:

    -   A CI class for each of the resources that are available to your users. All CI classes are based on the virtual machine object class.
    -   An identification rule that specifies an Object ID. Whenever components of Cloud Management refer to a specific cloud resource in the CMDB, they need the Object ID to find the correct cloud resource.
    -   A relationship rule that specifies how the CI class for the resource is related to other CI classes. For example, a **virtual server** CI must have a **Hosted on::Hosts** relationship with a **datacenter** CI. These relationship rules are necessary for CI uniqueness when processed by the Identification and Reconciliation Engine \(IRE\). The combination of the service account, the object ID of the resource, and the datacenter \(or location\) where the resource is located determines the uniqueness.
-   **MID Server script include**

    Each operation in the CAPI API has a MID Server script include that you configure. The script include calls the JavaScript classes that are already in other script includes in the system, or JavaScript classes that you create. Eventually, the invoker class is called to trigger the REST call. MID Server script includes are configured on your ServiceNow instance, but run on the MID Server.


This image illustrates how the components work together when a user provisions a resource from the Cloud User Portal:

![CAPI and your instance](../image/capi-and-instance.png)

## REST calls to the cloud provider

REST calls to the cloud provider are triggered from the MID Server script includes that are referenced from scripted CAPI Method Mappers inside CAPI API records. To create your own CAPI APIs, or to create custom MID Server script includes \(which are part of CAPI Method Mappers\), you must understand:

-   The classes that are available for you to call in MID Server script includes. See [CAPI classes in MID Server script includes](mid-server-script-includes.md).
-   How the cloud provider implements REST. See:
    -   [Azure REST API Reference](https://docs.microsoft.com/en-us/rest/api/azure/)
    -   [AWS Guides and API References](https://docs.aws.amazon.com/index.html#lang/en_us)

For example, to learn how to make a REST call to Azure to create a resource group, review this Azure topic: [Resource Groups - Create Or Update](https://docs.microsoft.com/en-us/rest/api/resources/resourcegroups/createorupdate). You can find the endpoint, parameters, and request body that Azure requires, and the responses it provides. You can see that:

-   The endpoint is `management.azure.com`
-   The method to call with a PUT operation is `subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}?api-version=2018-02-01`, where you specify the subscription ID, the resource group name, and the API version.

Remember that the REST API calls take place inside the MID Server script includes that are associated with CAPI API method mappers. Call the methods that CAPI already makes available for you by using the classes extended from **CloudAPIBase** and **CloudRESTAPIInvoker**. You can also create more script includes to extend these base classes and create your own classes. Familiarize yourself with these base classes and the methods available within them.

## Get started here

1.  [Review CAPI APIs that are provided with Cloud Provisioning and Governance by default](../reference/default-apis.md).
2.  [Review the CAPI classes that are provided by default](mid-server-script-includes.md). These classes can be called from the MID Server script includes in your CAPI API operations.
3.  Walk through the provisioning of an [Azure virtual machine](../task/walk-through-azure-provisioning.md) and an [AWS virtual machine](../task/walk-through-provisioning.md) to see how the components work together. The Azure walkthrough uses a MID Server script include so you can see the various CAPI classes used in the provision operation. The AWS walkthrough does not use a MID Server script include.
4.  [Add a product to an existing provider in CAPI](../task/create-provider.md).
5.  [Create a CI class for a virtual cloud resource](../task/create-a-ci-class-cloud.md).
6.  [Create or extend a CAPI interface](../task/create-interface.md).
7.  [Create a CAPI API](../task/create-api.md), and a custom MID Server script include that makes the REST calls to the cloud provider. An empty MID Server script include is always generated for new CAPI APIs. Modify it with the calls to other JavaScript classes and methods, such as the methods in the Invoker class.

**Parent Topic:**[Cloud Provisioning and Governance](cloud-management-v2-landing-page.md)

