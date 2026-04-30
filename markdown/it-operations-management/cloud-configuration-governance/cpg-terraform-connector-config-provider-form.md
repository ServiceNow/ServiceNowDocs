---
title: Cloud Services Catalog Terraform Connector Create Config Provider form reference
description: Cloud Provisioning and Governance uses the config provider to interact with the Terraform deployment.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cloud Services Catalog Terraform Connector reference, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Cloud Services Catalog Terraform Connector Create Config Provider form reference

Cloud Provisioning and Governance uses the config provider to interact with the Terraform deployment.

<table id="table_rhn_wlx_l5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the config provider.

</td></tr><tr><td>

Provider

</td><td>

Config provider type.-   Terraform Enterprise: Select this value to create a Terraform Enterprise config provider.
-   Terraform Environment: Select this value to create a Linux based Terraform Open Source config provider.
-   Terraform Windows Environment: Select this value to create a Windows based Terraform Open Source config provider.

</td></tr><tr><td>

Organization

</td><td>

Terraform organization that contains the Terraform workspaces and template repositories.This field appears when you select Terraform Enterprise from the Provider drop-down list.

</td></tr><tr><td>

URL

</td><td>

Base URL of the Terraform API server or IP address of the Terraform server.-   To create a config provider for Terraform Open Source, enter the IP address or hostname of the machine where Terraform CLI is installed or accessed via MID Server.
-   To create a config provider for Terraform Enterprise, enter the base URL of the Terraform Enterprise API server.
-   To create a config provider for Terraform Cloud, enter `https://app.terraform.io/api/v2`

</td></tr><tr><td>

Base Directory

</td><td>

Directory where all the individual Terraform template directories are located.

 This field appears when you select Terraform Environment or Terraform Windows Environment from the Provider drop-down list.

</td></tr><tr><td>

Server Type

</td><td>

Server type of the Terraform deployment.

</td></tr><tr><td>

Credential

</td><td>

Credential for accessing Terraform.-   For the Linux based Terraform Open Source server, select the appropriate SSH private key credential.
-   For the Windows based Terraform Open Source server, select the appropriate Remote Desktop Protocol \(RDP\) credential.
-   For Terraform Enterprise or Terraform Cloud, select the appropriate Terraform API key credential.

</td></tr><tr><td>

Version

</td><td>

Supported Terraform Open Source CLI version installed in the Terraform server.For more information on the supported Terraform Open Source versions, see the prerequisites section of [Create a Terraform Open Source config provider](../task/setup-cpg-terraform-connector-for-terraform-open-source.md).

 For more information on the supported Terraform Enterprise and Terraform Cloud versions, see the prerequisites section of [Create a Terraform Enterprise or Terraform Cloud config provider](../task/setup-cpg-terraform-connector-for-terraform-enterprise.md).

 Starting with Cloud Provisioning and Governance: Terraform Connector version 1.5.2, version 1.0.0 is deprecated. The deprecated version represents Terraform Open Source CLI version 0.11 and 0.12.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Services Catalog Terraform Connector reference](cpg-terraform-connector-reference.md)

