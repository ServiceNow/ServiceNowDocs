---
title: Use multiple repositories structure with Terraform Connector app
description: You can now discover multiple Terraform configurations from one repository, at any folder level with Terraform Enterprise Config Provider.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Use multiple repositories structure with Terraform Connector app

You can now discover multiple Terraform configurations from one repository, at any folder level with Terraform Enterprise Config Provider.

## Before you begin

Role required: admin

Perform the [Run the IaC Discovery](discover-terraform-config-installables-vcs-workspaces.md) steps and specify what repository, branches and folder paths have to be considered for discovering Terraform configurations with these steps.

## Procedure

1.  Add repositories and branches that you want to consider for discovering Terraform configurations.

2.  Use **&lt;Repository-Name&gt;::&lt;Branch-Name&gt;** format to include a branch from a repository.

3.  To specify multiple repository and branch mappings, use comma \(,\).

    Example: Repo1::Branch1, Repo2::Branch2.

    Leave the field bank if you want to discovery all the repositories and branches in that VCS.

4.  Select **Do you wish to specify sub-folder paths for Discovery** if you want to discover Terraform configurations from specific folder paths of the repository.

5.  In the **Folder Path List**, add the list of folder paths separated by comma\(,\) to discover terraform configurations from it.

    -   Folder path filter applies to all Repository Branches included in ‘Repo and Branch inclusion List’.
    -   All Terraform configurations you want to discover from a specific folder path needs to be in subfolders just one level below in folder hierarchy. Example:**/gcp/vm** folder path has one Terraform configuration for virtual machine,
    -   Specify **/gcp** in folder path list to discover vm Terraform configuration.

