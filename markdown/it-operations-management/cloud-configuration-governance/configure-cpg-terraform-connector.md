---
title: Configuring Cloud Services Catalog Terraform Connector
description: Understand the high-level workflow for configuring the Cloud Services Catalog Terraform Connector application.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Configuring Cloud Services Catalog Terraform Connector

Understand the high-level workflow for configuring the Cloud Services Catalog Terraform Connector application.

Perform the following steps to configure the Cloud Services Catalog Terraform Connector application:

1.  Install Cloud Services Catalog Terraform Connector. For more information, see [Install Cloud Services Catalog Terraform Connector](../task/install-cpg-terraform-connector.md).
2.  If you want to use a minor or patch version of Terraform Open Source, Terraform Enterprise, or Terraform Cloud, add the minor or patch version to the workload config provider record. For more information, see [Add support for minor or patch versions of the Terraform](../../cloud-management-v2-setup/task/terraform-use-minor-patch-version-cli.md).
3.  To use Terraform Open Source as a config provider for Cloud Provisioning and Governance, do the following:
    1.  Assign Terraform capability to the MID Server. For more information, see [Configure MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    2.  Create a Terraform Open Source config provider. For more information, see [Create a Terraform Open Source config provider](../task/setup-cpg-terraform-connector-for-terraform-open-source.md).
4.  To use Terraform Enterprise or Terraform Cloud as a config provider for Cloud Provisioning and Governance, do the following:
    1.  Assign Terraform Enterprise and REST capabilities to the MID Server. For more information, see [Configure MID Server capabilities](https://www.servicenow.com/docs/access?context=t_ConfigureCapabilities&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
    2.  Create a Terraform Enterprise or Terraform Cloud config provider. For more information, see [Create a Terraform Enterprise or Terraform Cloud config provider](../task/setup-cpg-terraform-connector-for-terraform-enterprise.md).
5.  Discover resources from the Terraform environment. For more information, see [Run the IaC Discovery](../task/discover-terraform-config-installables-vcs-workspaces.md).

