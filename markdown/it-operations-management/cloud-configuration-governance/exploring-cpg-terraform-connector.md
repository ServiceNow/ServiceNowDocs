---
title: Exploring Cloud Services Catalog Terraform Connector
description: Whether you're starting or expanding your implementation of Cloud Services Catalog Terraform Connector, learn more about the available features that help in provisioning and managing cloud resources across various public and private clouds.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Exploring Cloud Services Catalog Terraform Connector

Whether you're starting or expanding your implementation of Cloud Services Catalog Terraform Connector, learn more about the available features that help in provisioning and managing cloud resources across various public and private clouds.

The Cloud Services Catalog Terraform Connector integrates with the Cloud Provisioning and Governance application and helps you to create or update catalog items from the Terraform templates. Then, you can use the catalog items to provision the cloud resources.

## Key features of Cloud Services Catalog Terraform Connector

-   Discover the Terraform templates and workspaces from the Terraform environment.
-   Create catalog items from the Terraform templates.
-   Detect changes in the Terraform template and use the IaC change task workflow to update the catalog item.
-   Utilize the multi-repo support.
-   Specify metadata to populate the catalog item form fields and values.
-   Reduce the Terraform Cloud license cost by using the discovered Terraform workspaces to provision the cloud infrastructure.

## Use Terraform as a configuration provider

Use the Terraform Open Source, Terraform Enterprise, and Terraform Cloud config provider to provision resources in the following clouds.

Starting this release, you can use OpenTofu with Cloud Provisioning and Governance. You must have admin rights to configure the alias name for Terraform Open Source at the vm host level.

-   Amazon Web Services \(AWS\)
-   Microsoft Azure
-   Google Cloud Provider
-   VMware vSphere
-   IBM Cloud Platform \(Deprecated\)

In addition, you can use the Cloud Services Catalog Terraform Connector to provision resources to the Oracle Cloud Infrastructure \(OCI\) through the Cloud Provisioning and Governance: Oracle Cloud \(OCI\) Add-On for Terraform Connector app. For more information, see [Cloud Provisioning and Governance: Oracle Cloud \(OCI\) Add-On for Terraform Connector](https://store.servicenow.com/sn_appstore_store.do#!/store/application/faee70bf1b1cc510f62a64abbc4bcbe5/).

Starting with Cloud Provisioning and Governance: Terraform Connector version 1.5.2, the app doesn't support provisioning resources to the IBM Cloud Platform.

## Discover the Infrastructure as Code \(IaC\) templates

Use Cloud Services Catalog Terraform Connector to discover the IaC \(Terraform\) templates from the Terraform environment. Terraform Enterprise or Terraform Cloud organizations use various Version Control Systems to store the Terraform templates. Cloud Services Catalog Terraform Connector can discover the templates stored in the following VCS:

-   Public and self-hosted GitHub
-   Public and self-hosted GitLab
-   Public and self-hosted Microsoft Azure DevOps

For more information, see [Run the IaC Discovery](../task/discover-terraform-config-installables-vcs-workspaces.md).

Utilize the hierarchical structure of multiple repositories with the support of Terraform Connector IaC discovery capabilities.

## Create catalog items from the Terraform templates

Use the Cloud Services Catalog Terraform Connector app to create catalog items from the discovered Terraform templates and use them to provision resources in various clouds. For more information, see [Create a catalog item from the Terraform template](../task/catalog-item-terraform-template.md).

## Detect changes in the Terraform templates

Use IaC Discovery to detect changes in the Terraform templates that are used in existing catalog items. When Cloud Services Catalog Terraform Connector detects a change in the Terraform template, it creates an IaC change task. You can use the IaC change task to update the affected catalog item or deactivate it, and then create another catalog item from the updated Terraform template. For more information on the catalog item change task, see [Manage the Terraform template-based catalog items](../task/create-or-update-terraform-based-catalog-item.md).

## Reduce Terraform Cloud license cost

Use the discovered Terraform workspaces to provision the catalog items from the Terraform templates. Reusing workspace helps you to manage the Terraform Cloud license cost by avoiding the creation of workspaces.

