---
title: Run Discovery on Azure DevOps config provider
description: Add the Azure DevOps config provider and run Discovery to discover all projects, pipelines, and pipeline variables in an organization by using the Cloud Services Catalog application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/cloud-services-catalog/running-discovery-on-ado-config-provider.html
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating Azure DevOps and CI-CD tool, Configure, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Run Discovery on Azure DevOps config provider

Add the Azure DevOps config provider and run Discovery to discover all projects, pipelines, and pipeline variables in an organization by using the Cloud Services Catalog application.

## Before you begin

Role required: none

## Procedure

1.  Navigate to the **Admin** portal and select **Manage****Credentials**.

2.  Add the **API key** credential that you created with the Personal Access Token \(PAT\) credential.

    For more information on setting PAT privileges, see [Azure DevOps permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-services-catalog/ado-permissions.md).

3.  Prefix the Personal Access Token \(PAT\) credential with straight quotes \(':'\) and encode to a base64 format.

4.  Prefix the encoded format string with a Basic string.

    For example, Basic encoded base 64\(:PAT\).

5.  Add a required alias.

6.  Navigate to **Manage** &gt; **Config Management** and add a config provider.

    \[Omitted image "edit-ado-config-provider.png"\] Alt text: Edit Azure Devops Config provider form.

    **Important:**

    Infrastructure as Code \(IaC\) Discovery is supported. You can discover the Azure DevOps pipeline Ansible job templates by setting up a scheduled discovery.

7.  Discover all projects, pipelines, and pipeline variables in an organization by running Discovery.

    \[Omitted image "ado-config-provider.png"\] Alt text: Azure DevOps Config provider for DevOps project.

8.  Find the Config installables under the selected Azure DevOps project.

    \[Omitted image "cfg-installables.png"\] Alt text: Details of ADO Config provider Installables.


## Result

You can now order an Azure DevOps catalog item from the Azure DevOps catalog order form on Employee Center.

**Parent Topic:**[Integrating Azure DevOps and the Continuous Integration-Continuous Deployment pipeline](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/cloud-services-catalog/integrating-azure-devops-and-cicd-pipeline.md)

