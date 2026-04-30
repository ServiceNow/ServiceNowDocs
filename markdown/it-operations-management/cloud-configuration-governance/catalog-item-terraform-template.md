---
title: Create a catalog item from the Terraform template
description: Create a catalog item from the Terraform template to request cloud resource provisioning. Activated catalog items appear in the cloud user portal.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Using Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Create a catalog item from the Terraform template

Create a catalog item from the Terraform template to request cloud resource provisioning. Activated catalog items appear in the cloud user portal.

## Before you begin

-   Ensure that an appropriate Terraform config provider is available. For more information on creating the config provider, see [Create a Terraform Open Source config provider](setup-cpg-terraform-connector-for-terraform-open-source.md) and [Create a Terraform Enterprise or Terraform Cloud config provider](setup-cpg-terraform-connector-for-terraform-enterprise.md).
-   Ensure that the Terraform template is working \(that is, you can directly use the template with the Terraform system to provision the specified cloud resources\). For more information on Terraform templates, see the [Terraform language documentation](https://www.terraform.io/language).
-   Ensure that the provider block of the Terraform template adheres to the following syntax:
    -   Provider block syntax for the Microsoft Azure cloud:

        ```
        provider "azurerm" {
        
          subscription_id = "${var.subscriptionId}"
          client_id       = "${var.clientId}"
          client_secret   = "${var.clientSecret}"
          tenant_id       = "${var.tenantId}"
        }
        ```

    -   Provider block syntax for the Amazon Web Services cloud:

        **Important:** By default, the ServiceNow® Cloud Provisioning and Governance \(CPG\) Terraform Connector does not support AWS IAM role-based authentication when using Terraform templates.

        ```
        provider "aws" {
          access_key      = "${var.access_key}"
          secret_key      = "${var.secret_key}"
          region          = "${var.region}"
        }
        ```

    -   Provider block syntax for Google Cloud Platform

        ```
        terraform {
          required_providers {
            google = {
              source  = "hashicorp/google"
              version = "5.10.0"
            }
          }
        }
         
        provider "google" {
          credentials = var.credentials
          project     = var.project
          region      = var.region
        }
        ```

    -   Provider block syntax for VMware Cloud:

        ```
        provider "vsphere" {
          user                  = "${var.user}"
          password              = "${var.password}"
          vsphere_server        = "${var.vsphere_server}"
        }
        
        ```

        **Note:** Do not hard-code any credential in the Terraform template. Use appropriate Terraform variables to fetch the credentials from the ServiceNow AI Platform.

-   Ensure that the variable definition file \(`variable.tf`, `.tfvars`, or `.tfvars.json`\) contains the definition of the variables used in the provider block.
-   If you are using Terraform Enterprise or Terraform Cloud, ensure that the MID Server can connect with Version Control System \(VCS\) accounts provisioned in the Terraform organization.

    To verify connectivity with the VCS accounts provisioned in the Terraform organization, execute the appropriate curl command on the MID Server.

    -   **GitHub**

        ```
        curl -H "Authorization: <API credential> https://<github-api-host>/user/repos?per_page=100&page=1"
        ```

    -   **GitLab**

        ```
        curl -H "Authorization: <API credential>" https://<gitlab-api-host>/api/v4/projects?visibility=private&per_page=100&page=1
        ```

    -   **Microsoft Azure DevOps**

        ```
        curl -H "Authorization: <API credential> https://<azure-devops-api-host>/<organization>/<project>/_apis/git/repositories?api-version=6.0"
        ```

        Where,

        -   **organization** is the name of the Microsoft Azure DevOps organization.
        -   **project** is the name of the Microsoft Azure DevOps project.
    For more information on the API credentials, see [Cloud Services Catalog Terraform Connector API Key Credentials form reference](../reference/cpg-terraform-connector-api-key-credentials-form-reference.md).


Role required: sn\_cmp.cloud\_service\_designer

## About this task

The Cloud Services Catalog Terraform Connector app supports the following Terraform data types:

-   string
-   number
-   bool
-   list
-   tuple
-   map
-   object

## Procedure

1.  Create a cloud catalog item.

    1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal**.

        The Cloud Admin Portal opens in a new browser tab.

    2.  Navigate to **Design** &gt; **Cloud Catalog Items**.

    3.  Select **New**.

    4.  On the form, fill in the fields.

<table id="table_ev2_rpb_55b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name of the catalog item.

</td></tr><tr><td>

Source

</td><td>

Source of the catalog item.Select **Configuration Management Template** from the drop-down list.

</td></tr><tr><td>

Provider Type

</td><td>

Terraform config provider type that you want to use.-   To use Terraform Enterprise or Terraform Cloud, select **Terraform Enterprise**.
-   To use a Linux-based Terraform Open Source server, select **Terraform Environment**.
-   To use a Windows-based Terraform Open Source server, select **Terraform Windows Environment**.


</td></tr><tr><td>

Provider

</td><td>

Name of the Terraform config provider that you want to use.

</td></tr></tbody>
</table>    5.  Save the Cloud Catalog Item form.

2.  Associate a Terraform template with the catalog item.

    1.  From the Cloud Templates related list, select **New**.

    2.  From the Configuration installable drop-down list, select the Terraform template you want to use.

    3.  Save the ServiceNow Cloud Templates Versions form.

        **Note:** A catalog item can include multiple versions of the cloud template, but only one version can be active.

    4.  Select **Activate** to activate the cloud template.

3.  To add or remove catalog item form fields, edit the variable sets associated with the catalog item.

4.  Select the **Active** check box to activate the catalog item.

5.  Select **Update**.


## What to do next

Verify that the catalog item appears in the Cloud User Portal.

**Parent Topic:**[Using Cloud Services Catalog Terraform Connector](../concept/using-ccg-terraform-connector.md)

