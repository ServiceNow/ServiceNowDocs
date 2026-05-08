---
title: Create a Terraform Enterprise or Terraform Cloud config provider
description: Create Terraform Enterprise or Terraform Cloud config provider in Cloud Provisioning and Governance. The config provider enables Cloud Provisioning and Governance to discover the workspaces and Version Control System \(VCS\) repositories attached to the Terraform organization.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a Terraform Enterprise or Terraform Cloud config provider

Create Terraform Enterprise or Terraform Cloud config provider in Cloud Provisioning and Governance. The config provider enables Cloud Provisioning and Governance to discover the workspaces and Version Control System \(VCS\) repositories attached to the Terraform organization.

## Before you begin

-   Ensure that a supported Terraform Enterprise or Terraform Cloud version is in use. Cloud Services Catalog Terraform Connector supports the following Terraform versions:
    -   Terraform Enterprise versions 1.1.9 and 1.2.0 or higher
    -   Terraform Cloud versions 1.1.9 and 1.2.0 or higher
-   To use a minor or patch version of the Terraform Enterprise or Terraform Cloud, ensure that the minor or patch version is added to the workload config provider. For more information, see [Add support for minor or patch versions of the Terraform](../../cloud-management-v2-setup/task/terraform-use-minor-patch-version-cli.md).
-   Ensure that the following properties are correctly configured in the MID Server. The MID Server uses these properties to connect with the Terraform Enterprise or Terraform Cloud.

    -   **glide.http.proxy\_host**
    -   **glide.http.proxy\_port**
    -   **glide.http.proxy\_username**
    -   **glide.http.proxy\_password**
    For more information, see the Knowledge Base article [KB0754247](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0754247).

-   Ensure that the MID Server has Terraform Enterprise and REST capabilities. For more information, see Configure MID Server capabilities.
-   Ensure that the MID Server can communicate with the VCS accounts provisioned in the Terraform Enterprise or Terraform Cloud organization.

Role required: admin

## Procedure

1.  Create an API key credential for Terraform Enterprise or Terraform Cloud account.

    For more information, see [Create API key credentials for the Terraform account and the supported VCS account](create-vcs-credentials-for-terraform-connector.md).

2.  Create a config provider for Terraform Enterprise or Terraform Cloud.

    1.  On the Cloud Admin Portal, navigate to **Manage** &gt; **Config Management**.

    2.  Select **New**.

    3.  On the form, fill in the fields.

        For a description of the form fields, see [Cloud Services Catalog Terraform Connector Create Config Provider form reference](../reference/cpg-terraform-connector-config-provider-form.md).

    4.  Select **Submit**.


## What to do next

Discover the workspaces and Version Control System \(VCS\) repositories attached to the Terraform organization specified in the config provider. For more information, see [Run the IaC Discovery](discover-terraform-config-installables-vcs-workspaces.md).

