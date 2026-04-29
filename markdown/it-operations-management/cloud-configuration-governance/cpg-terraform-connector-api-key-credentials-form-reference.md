---
title: Cloud Services Catalog Terraform Connector API Key Credentials form reference
description: The Cloud Services Catalog Terraform Connector uses API key credentials to authenticate the requests sent to the Terraform Enterprise and Terraform Cloud and the version control systems provisioned in them.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Services Catalog Terraform Connector reference, Cloud Services Catalog Terraform Connector, Support for continuous delivery \(configuration management\), Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Services Catalog Terraform Connector API Key Credentials form reference

The Cloud Services Catalog Terraform Connector uses API key credentials to authenticate the requests sent to the Terraform Enterprise and Terraform Cloud and the version control systems provisioned in them.

To learn more about API key permissions and tokens, see [https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/api-tokens](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/api-tokens).

<table id="table_bbz_drq_p5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name of the credential.

</td></tr><tr><td>

Active

</td><td>

Option for enabling this credential for discovery. Select this check box to enable discovery.

</td></tr><tr><td>

API Key

</td><td>

API key that can be used to access the account.-   Terraform Enterprise or Terraform Cloud API key: Bearer token for accessing Terraform Enterprise or Terraform Cloud.

Ensure that the API key adheres to the following syntax:

    ```
Bearer <API key>
    ```

-   GitHub API key: API token for accessing the GitHub enterprise or community account.

Ensure that the token adheres to the following syntax:

    ```
Token <API key>
    ```

-   GitLab API key: Bearer token for accessing the GitLab enterprise or community account.

Ensure that the token adheres to the following syntax:

    ```
Bearer <API key>
    ```

-   Microsoft Azure DevOps API key: base-64 encoded token for accessing the Azure DevOps enterprise or community account.

**Important:** Prefix the API token with a colon \(:\), and then encode the entire string to base-64.

Ensure that the token adheres to the following syntax:

    ```
Basic <base-64 encoded API key>
    ```


</td></tr><tr><td>

Applies to

</td><td>

MID Server to which you apply the credentials. Select **All MID servers**

</td></tr><tr><td>

Order

</td><td>

Order in which the platform runs this credential as it attempts to log in to devices. A smaller number indicates that the credential appears higher in the list. Establish the credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number, or none, the instance tries the credentials in a random order. The default value is 100.

</td></tr><tr><td>

Credential alias

</td><td>

Credential alias that can resolve the credential.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Services Catalog Terraform Connector reference](cpg-terraform-connector-reference.md)

