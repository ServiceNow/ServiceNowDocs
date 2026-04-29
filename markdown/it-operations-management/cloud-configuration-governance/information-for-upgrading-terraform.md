---
title: Upgrading the Terraform environment
description: Understand the high-level workflows for upgrading the Terraform environment.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Cloud Services Catalog Terraform Connector, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Upgrading the Terraform environment

Understand the high-level workflows for upgrading the Terraform environment.

-   **Upgrading Terraform Open Source**

<table id="table_q4s_2c1_w5b"><thead><tr><th>

Upgrade method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Upgrade the existing Terraform Open Source installation to a newer supported version

</td><td>

**Note:** If you choose to upgrade the existing Terraform Open Source installation, you may experience a longer upgrade time.

 Perform the following actions to upgrade the existing Terraform Open Source installation:

1.  Upgrade the Terraform Open Source server to a version that is supported by the Cloud Services Catalog Terraform Connector.

For more information on upgrading Terraform, see Upgrade Guides in [Terraform documentation](https://www.terraform.io/docs).

Cloud Services Catalog Terraform Connector supports Terraform Open Source versions 1.1.0 through 1.1.9 and 1.2.0 or higher

2.  Test and modify the existing Terraform templates to ensure compatibility with the target Terraform Open Source version.
3.  Update the Terraform Open Source version mentioned in the Terraform Open Source config provider.


</td></tr><tr><td>

Set up a new Terraform server with the desired Terraform Open Source version

</td><td>

Perform the following actions to set up a new Terraform server with the desired Terraform Open Source version:1.  Create a Linux or Windows server for Terraform Open Source installation.
2.  Install a Terraform Open Source version that is supported by the Cloud Services Catalog Terraform Connector.

Cloud Services Catalog Terraform Connector supports Terraform Open Source versions 1.1.0 through 1.1.9 and 1.2.0 or higher

3.  Copy the existing Terraform templates to the new Terraform server.

**Note:** Ensure that all the templates are stored in separate directories and all the template directories are in the same base directory.

4.  Test and modify the copied Terraform templates to ensure compatibility with the target Terraform Open Source version.
5.  Create a Terraform Open Source config provider. For more information, see [Create a Terraform Open Source config provider](../task/setup-cpg-terraform-connector-for-terraform-open-source.md).
6.  Remove the old catalog items per the business strategy of your organization, and then retire the old Terraform server.


</td></tr></tbody>
</table>-   **Upgrading Terraform Enterprise and Terraform Cloud**

    Test and modify the existing Terraform templates to ensure compatibility with the new Terraform Enterprise or Terraform Cloud version.

    **Note:** The stacks and Terraform workspaces are tied to the Terraform version through which they were provisioned. Therefore, the same Terraform version is used to provision and deprovision a stack or Terraform workspace.


