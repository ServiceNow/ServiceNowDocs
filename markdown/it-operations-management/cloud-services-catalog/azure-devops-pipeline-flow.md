---
title: Order a Microsoft Azure DevOps catalog item
description: Provision the Microsoft Azure DevOps catalog by using the Microsoft Azure DevOps catalog order form in the Cloud Services Catalog application.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrating Azure DevOps and CI-CD tool, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Order a Microsoft Azure DevOps catalog item

Provision the Microsoft Azure DevOps catalog by using the Microsoft Azure DevOps catalog order form in the Cloud Services Catalog application.

## Before you begin

To use Microsoft Azure DevOps for Cloud Services Catalog, assign Azure DevOps and Cloud Management capabilities to the MID Server. For more information, see [Configure MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

Set the deploymentID as variables in the AWS pipelines that you want to discover. The subscriptionID isn’t required for Microsoft Azure pipelines.

Tag all the resources with the deploymentID key.

Role required: none

## About this task

View this video to understand ADO deployment with Cloud Services CatalogFollow this short video to learn how to order an Azure DevOps catalog item.

## Procedure

1.  In the **Update variable** dialog box, override the pipeline variables by selecting the **Let users override this value when running this pipeline** check box.

2.  ![Dialog box that has two options that you can select. You can either keep the value secret or to override the value when you run the pipeline.](../image/update-variable.png)

3.  Navigate to **Employee Center** &gt; **Cloud Services** &gt; **Integrations** &gt; **CSC DevOps Integration**.

    Use this Azure DevOps Catalog item order form to call an ADO pipeline.

    ![Ordering an Azure DevOps catalog item.](../image/ado-catalog-form.png)

4.  On the form, fill in the **UserGroup** and **Change Request** fields.

5.  In the Choose Configuration Provider list, select the config provider that is associated with the Azure DevOps organization.

6.  Select the project and associated pipeline in the organization.

    The pipeline variables are automatically filled in. You can modify the variables. For example, although the pipeline secret variables are masked, you can modify these values.

7.  Select the **Service Account**, which is the same option that you selected as a service connection in the Azure DevOps pipeline.

    -   For Amazon Web Services, a location list is displayed when you select **Service Account**.
    -   You can expose a pipeline variable location or region and use it in a pipeline for provisioning. This pipeline variable is overridden by the value that you chose in the location list to ensure that provisioning and Discovery are at the same location.
    -   A location is required for Discovery in Microsoft Azure, so no list is displayed when you select **Service Account**. These settings ensure the correct resources that are related to the stack are populated in CMDB. You can run Discovery based on those settings.
8.  If the location is pre-filled for the AWS pipeline, select the same location in the catalog for Discovery.

9.  Set up the identifying tags for the provisioned resources.

    The DeploymentID field is read-only and auto-generated for the order. The DeploymentID is assigned as a tag to all the provisioned resources if you added it as a tag in the Azure DevOps pipeline template of the stacks in the cloud. The DeploymentID is also assigned as a tag to the stack. If the pipeline has any of these three variables \(Application, BusinessService or CostCenter\), they’re displayed in the General info in the Azure DevOps UI.

10. From the list, select the field values to be updated in the pipeline variables.

    These entries are considered for the current order only.

    **Note:** You can't modify these read-only variables from the pipeline variable section. These variables are added as tags to the stack in the cloud and are inserted in the CMDB key value table as well. You can do only the resource level actions on a provisioned stack because the stack level action is turned off. The previous stack is marked as obsolete if you run the pipeline again, although the resources remain in the cloud.


## What to do next

Verify that a blueprint approval policy \(CSC Content Approval Policy ADO Integration\) is applied on the Microsoft Azure DevOps catalog. This policy mandates that an approval must be obtained from the Change management group before any provisioning can take place.

**Parent Topic:**[Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline](../concept/integrating-azure-devops-and-cicd-pipeline.md)

