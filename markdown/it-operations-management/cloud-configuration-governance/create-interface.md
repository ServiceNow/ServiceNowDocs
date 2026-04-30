---
title: Create or extend a CAPI interface
description: You can create a new CAPI interface or extend an existing one by adding new operations.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create or extend a CAPI interface

You can create a new CAPI interface or extend an existing one by adding new operations.

## Before you begin

-   Role required: admin
-   Review [Default CAPI APIs](../reference/default-apis.md) and make sure the provider and product that you want to create do not exist.
-   Familiarize yourself with the cloud provider API so that you know how to create REST calls to the provider. If you are not familiar with the headers, authentication requirements, endpoint, and data that you can pass into the provider API, you cannot build your own CAPI components.

## About this task

Usually, you can use the default interfaces that are provided in the Cloud Provisioning and Governance application. To create a custom interface, base it on an existing one that is similar.

## Procedure

1.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API**, and then click the **Interface** tab.

2.  Click **New**.

3.  In the Add Cloud interface window, enter a name for the interface, a helpful description, and select the most relevant category to which the API interface should belong.

    This example shows an interface for Azure storage:

    ![Azure storage interface](../image/capi-azure-storage-interface.png)

4.  In the CAPI Interface Operations related list, click **New**.

    Each operation that you create corresponds to a different REST API call.

5.  Provide a name for the operation that corresponds to the API you want to call in the provider.

    For example, you can create an operation called **CreateContainer** that corresponds to the Create Container operation in Azure.

    ![Create Container](../image/capi-create-container.png)

6.  Right-click the header and select **Save**.

7.  In the Interface Operation Parameters related list, click **New**.

8.  Create a parameter that the operation needs as defined by the cloud provider REST API documentation.

    If you do not know the parameters, the operation fails. In the Azure storage example, the **CreateContainer** operation must have the name of the container that is referred to here as **ContainerName**.

    ![Container name](../image/capi-containername.png)

9.  Click **Submit**.

10. Add as many parameters as you need for the operation, and then add all the operations you need.


## What to do next

[Create a CAPI API](create-api.md)

**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

