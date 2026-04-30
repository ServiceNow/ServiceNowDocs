---
title: Cloud Provisioning and Governance administration guide
description: After you set up the Cloud Provisioning and Governance application on your instance, there are many items that you must configure before your users can request and manage any cloud resources.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Provisioning and Governance administration guide

After you set up the Cloud Provisioning and Governance application on your instance, there are many items that you must configure before your users can request and manage any cloud resources.

## Requirements

Role required to use the Cloud Provisioning and Governance administration guide is cloud\_admin.

## Before you begin

-   **Set up Cloud Provisioning and Governance**

    See the appropriate setup guide for your cloud provider:

    -   [Cloud Provisioning and Governance setup guide for AWS](../../cloud-management-v2-setup/concept/cloud-mgt-aws-setup-day-1.md)
    -   [Cloud Provisioning and Governance setup guide for Azure](../../cloud-management-v2-setup/concept/cloud-mgt-azure-setup-guide.md)
    -   [Cloud Provisioning and Governance setup guide for VMware](../../cloud-management-v2-setup/concept/cloud-mgt-vmware-setup-guide.md)
    .


## What to do after setup

-   **Create resource profiles**

    Resource profiles contain the attributes that a resource can have. Users select values for these attributes when they order a cloud resource. You can configure these types of resource profiles: Compute \(such as the size of a VM\), Operating System \(such as the type and version\), Storage \(such as backup\), and Security Groups \(such as whether to use HTTPS\). See [Resource Profiles](cloud-resource-profiles.md) for more information.

-   **Configure governance**

    Governance tools that you can use to restrict the provisioning of cloud resources include quotas and policies. Examples of things you can configure include the approval subflow that is used after a user requests a cloud resource, whether an email is sent after a cloud resource is stopped, and which datacenter should be automatically selected when a user selects a resource from a specific cloud provider. See [Cloud Governance](cloud-governance.md) for more information.

-   **Populate the Cloud Service Catalog**

    After you apply governance quotas and policies, create Service Catalog items. You can create a catalog item in the following ways:

    -   Import a template from AWS or Microsoft Azure
    -   Use or modify a base-system catalog item
    -   Use a Terraform template

