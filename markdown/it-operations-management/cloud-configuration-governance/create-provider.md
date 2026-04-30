---
title: Add a product to an existing provider in CAPI
description: The Cloud Provisioning and Governance Cloud API \(CAPI\) offers many providers, such as AWS and Azure, and products, such as EC2 instances. However, you can add products to existing providers for new types of cloud resources.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud API \(CAPI\), Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Add a product to an existing provider in CAPI

The Cloud Provisioning and Governance Cloud API \(CAPI\) offers many providers, such as AWS and Azure, and products, such as EC2 instances. However, you can add products to existing providers for new types of cloud resources.

## Before you begin

-   Role required: admin
-   Review [Default CAPI APIs](../reference/default-apis.md) and make sure the provider and product that you want to create are not already provided.
-   Familiarize yourself with the cloud provider API so that you know how to create REST calls to the provider. If you are not familiar with the headers, authentication requirements, endpoint, and data that you can pass into the provider API, you cannot build your own CAPI components.

## About this task

This topic provides general instructions for extending an existing cloud provider, product, and resource type.

## Procedure

1.  In your instance \(not in the Cloud Admin Portal\), enter the following text into the application filter:

    `sn_capi_product.list`

    ![Opening the list of CAPI products](../image/sn_capi_prouct.png)

2.  Press `ENTER`.

    The list of products that belong to all providers appears. You can filter the list to verify that the product you want to create is not already provided.

3.  Click **New** and then enter a name and choose one of the existing service categories that is most appropriate.

4.  Click **Submit**.

    The list of products appears again.

5.  Find the product that you created, and then double-click the empty cell in the **Provider** column.

    ![Double click the empty cell](../image/double-click-empty-cell.png)

6.  Add the correct provider.

7.  Add a unique provider name: Double-click the cell in the **Provider Name** field and then change the name.

    The system can auto-generate a provider name for you, but you should modify it to avoid conflicts with existing provider names.

8.  In the Cloud Admin Portal, navigate to **Design** &gt; **Cloud API**.

9.  Click the tile for the provider to which you added the new product.

10. Verify that your product is in the **Cloud Products** related list.

11. Click the information icon \(![Information icon](../image/icon-information.png)\) for the cloud product, and then click **Open Record**.

12. In the Cloud Resource Types related list, click **New** and then fill in the form.

<table id="table_kdx_mbs_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and descriptive name.

</td></tr><tr><td>

Product

</td><td>

The Cloud Product for which you're creating the Resource type. Select from the lookup list or create new.

</td></tr><tr><td>

CI Class

</td><td>

A CMDB table you need to associate with the resource type. If you do not see the correct CMDB table, see [Create a CI class for a virtual cloud resource](create-a-ci-class-cloud.md) for instructions on how to create one.

</td></tr><tr><td>

Pattern

</td><td>

The pattern that is used to discover the resource type. Select from the [Discovery patterns](../../service-mapping/concept/c_MappingPatternsCustomization.md) lookup list or [create a new pattern](../../service-mapping/task/t_CreatePatternPatDef.md).

</td></tr><tr><td>

Dependency Sequence

</td><td>

The order in which resource type is provisioned or discovered. Specify the order based on inter-dependencies of resources. For example, if you have a network and a subnet that you want to discover or create, specify a higher order for network than subnet, so that discovery or creation of resources is performed logically and sequentially.

</td></tr></tbody>
</table>    ![A new resource type](../image/capi-resource-type.png)

13. Click **Submit**.


## What to do next

[Create a CI class for a virtual cloud resource](create-a-ci-class-cloud.md) if necessary, or [Create or extend a CAPI interface](create-interface.md)

**Parent Topic:**[Cloud Provisioning and Governance](../concept/cloud-management-v2-landing-page.md)

