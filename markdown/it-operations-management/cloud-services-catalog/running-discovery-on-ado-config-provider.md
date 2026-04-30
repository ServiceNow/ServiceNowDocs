---
title: Run Discovery on Azure DevOps config provider
description: Add the Azure DevOps config provider and run Discovery to discover all projects, pipelines, and pipeline variables in an organization by using the Cloud Services Catalog application.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline, Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Run Discovery on Azure DevOps config provider

Add the Azure DevOps config provider and run Discovery to discover all projects, pipelines, and pipeline variables in an organization by using the Cloud Services Catalog application.

## Before you begin

Role required: none

## Procedure

1.  Navigate to the **Admin** portal and select **Manage****Credentials**.

2.  Add the **API key** credential that you created with the Personal Access Token \(PAT\) credential.

3.  Prefix the Personal Access Token \(PAT\) credential with straight quotes \(':'\) and encode to a base64 format.

4.  Prefix the encoded format string with a Basic string.

    For example, Basic encoded base 64\(:PAT\).

5.  Add a required alias.

6.  Navigate to **Manage** &gt; **Config Management** and add a config provider.

    ![Edit Azure Devops Config provider form.](../image/edit-ado-config-provider.png)

    **Important:**

    Infrastructure as Code \(IaC\) Discovery is supported. You can discover the Azure DevOps pipeline Ansible job templates by setting up a scheduled discovery.

7.  Discover all projects, pipelines, and pipeline variables in an organization by running Discovery.

    ![Azure DevOps Config provider for DevOps project.](../image/ado-config-provider.png)

8.  Find the Config installables under the selected Azure DevOps project.

    ![Details of ADO Config provider Installables.](../image/cfg-installables.png)


## Result

You can now order an Azure DevOps catalog item from the Azure DevOps catalog order form on Employee Center.

**Parent Topic:**[Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline](../concept/integrating-azure-devops-and-cicd-pipeline.md)

