---
title: Set up the Microsoft Azure DevOps console
description: Set up the Microsoft Azure DevOps console as the first step before you run Discovery and order a catalog item in the Cloud Services Catalog application.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up the Microsoft Azure DevOps console

Set up the Microsoft Azure DevOps console as the first step before you run Discovery and order a catalog item in the Cloud Services Catalog application.

## Before you begin

1.  Add a deploymentID variable to the Microsoft Azure DevOps pipelines in your organization. The Microsoft Azure DevOps integration discovers pipelines with a deploymentID variable only.
2.  Tag all the provisioned resources with a deploymentID key in the pipeline so that you can discover the resources after provisioning.

The subscriptionID isn’t required for Azure DevOps and Ansible templates.

Role required: none

## Procedure

1.  Name a pipeline variable deploymentID that you can use for pointed Discovery to update the resources in CMDB.

2.  Create a Personal Access Token \(PAT\) credential that you can use in Azure DevOps Discovery.

3.  In the **Update variable** dialog box, override the pipeline variables by selecting the **Let users override this value when running this pipeline** check box.

    ![Update variable dialog box that has two options that you can select. Keep the value secret or override the value when you run the pipeline.](../image/update-variable.png "Update variable dialog box")

    The pipeline works with the CSC DevOps Integration catalog item. The Microsoft Azure DevOps integration discovers pipelines with the deploymentID variable.


**Parent Topic:**[Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline](../concept/integrating-azure-devops-and-cicd-pipeline.md)

