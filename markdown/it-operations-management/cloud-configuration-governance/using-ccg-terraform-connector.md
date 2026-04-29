---
title: Using Cloud Services Catalog Terraform Connector
description: Understand the high-level use cases and usage workflows for the Cloud Services Catalog Terraform Connector application.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Using Cloud Services Catalog Terraform Connector

Understand the high-level use cases and usage workflows for the Cloud Services Catalog Terraform Connector application.

-   **[Associate the Terraform input parameters with the Cloud Provisioning and Governance catalog item](../../cloud-management-v2-setup/task/terraform-catalog-metadata-ingest.md)**  
Create a JSON file to store the variables that are used in the template file so that you can map them to discovered resources, pools, and filters. You can use variables or parameters from the Terraform template to map to fields on the catalog item provision form.
-   **[Populate the datacenter in Terraform-based catalog items](../task/terraform-auto-pop-location.md)**  
In any request for a catalog item using Terraform templates, the required Location value specifies the datacenter or region where to provision the configuration items and stacks. You can use a variable named **region** in the Terraform template to map to the Location field on the request form.
-   **[Create a catalog item from the Terraform template](../task/catalog-item-terraform-template.md)**  
Create a catalog item from the Terraform template to request cloud resource provisioning. Activated catalog items appear in the cloud user portal.
-   **[Manage the Terraform template-based catalog items](../task/create-or-update-terraform-based-catalog-item.md)**  
Use an Infrastructure as Code \(IaC\) change task to create or update the Terraform template-based catalog items. The IaC change task helps ensure that the catalog items are aligned with the latest infrastructure specifications coded in the Terraform template.
-   **[Map credentials between Cloud Provisioning and Governance and Terraform](../task/map-cloud-mgmt-terraform-credentials.md)**  
Map credential types and service account fields between Cloud Provisioning and Governance and Terraform using Credential Mapping.
-   **[Associate the Terraform environment variable with the datacenter resource block](../task/associate-terraform-variable-with-datacenter-resource-block.md)**  
Associate the Terraform environment variable with the Cloud Provisioning and Governance datacenter resource block. After associating the environment variable, you can use it to pass custom inputs parameters during resource deployment through Terraform Enterprise.

**Parent Topic:**[Cloud Services Catalog Terraform Connector](../reference/cpg-terraform-connector-landing-page.md)

