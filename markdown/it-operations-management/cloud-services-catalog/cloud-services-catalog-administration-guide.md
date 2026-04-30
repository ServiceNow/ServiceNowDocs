---
title: Cloud Services Catalog administration guide
description: After you set up the Cloud Services Catalog application, you must set up some additional items so that your users can request and manage any cloud resource.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Services Catalog administration guide

After you set up the Cloud Services Catalog application, you must set up some additional items so that your users can request and manage any cloud resource.

## Configuring governance

You can use governance tools to restrict the provisioning of cloud resources, such as quotas and policies. For example, you can configure the approval workflow that is used after a user requests a cloud resource, whether an email is sent after a cloud resource is stopped, and which datacenter is automatically selected when a user selects a resource from a cloud provider. For more information about quotas, policies, and other governance types, see [Cloud Governance](../../cloud-management-v2/concept/cloud-governance.md).

## Populating the Cloud Services Catalog

After you apply the governance quotas and policies, you must create Cloud Services Catalog items. You can create a catalog item in the following ways:

1.  Import a template from Amazon Web Services, Microsoft Azure or Google Cloud Platform.
2.  Use or modify an [out-of-the-box](out-of-the-box-catalog-items.md) catalog item.
3.  Use a [Terraform template](../../cloud-management-v2/task/catalog-item-terraform-template.md).

For information about domain separation, multi-repo support with Terraform app, cloud accounts, the Cloud admin portal, or the Cloud API, see the following topics:

-   [Use multiple repositories structure with Terraform Connector app](../../cloud-management-v2/task/use-multiple-repositories-structure-with-terraform-connector.md)
-   [Domain separation and Cloud Services Catalog](domain-separation-and-cloud-services-catalog.md): Get additional information about domain separation.
-   [Cloud accounts](../../cloud-management-v2/concept/cloud-accounts.md): Learn about the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure.
-   [Cloud Admin Portal](../../cloud-management-v2/concept/cloud-admin-portal.md): Manage, design, govern, operate, and analyze all your cloud resources from this portal.
-   [Cloud API \(CAPI\)](../../cloud-management-v2/concept/cloud-management-api.md): Integrate Cloud Provisioning and Governance with cloud providers by using REST APIs.

-   **[Cloud Services Catalog and Terraform Connector](cloud-services-catalog-and-terraform-connector.md)**  
Use the Cloud Services Catalog app with Terraform Connector support with all its features that help in provisioning and managing cloud resources across various public and private clouds.
-   **[Permissions management for Cloud Services Catalog](working-with-permissions.md)**  
Permissions are your group-level access rights to features and actions in Cloud Services Catalog.
-   **[Policies and permission levels on services](../reference/policies-and-permission-levels-on-services.md)**  
Configure policies with the necessary level of permissions to provide access to the AWS, Azure, ADO, Ansible and Google Cloud services, respectively.

**Parent Topic:**[Configuring Cloud Services Catalog](configuring-csc.md)

