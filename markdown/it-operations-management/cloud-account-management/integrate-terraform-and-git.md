---
title: Create a Terraform organization for Cloud Account Management in Cloud Workspace
description: Integrate with Terraform Cloud/Terraform Enterprise to organize accounts, define workflows, enforce security, improve collaboration, and enhance scalability.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Terraform and GitHub, Provisioning modes for Cloud Account Management in Cloud Workspace, Setting up AWS cloud, Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a Terraform organization for Cloud Account Management in Cloud Workspace

Integrate with Terraform Cloud/Terraform Enterprise to organize accounts, define workflows, enforce security, improve collaboration, and enhance scalability.

## Before you begin

Role required: Terraform admin

Attributes required for this setup:

-   AWS Access Key
-   AWS Secret Key

Make sure you have access to Terraform Cloud or Terraform Enterprise to perform the following procedure.

## Procedure

1.  Log in and navigate to the Terraform Cloud \(`https://app.terraform.io/session`\) or Terraform Enterprise portal \( `https://<tfe_server_url>/api/v1`\).

2.  Select the user name or organization name.

3.  In the modal window, enter a unique org name and other details.

4.  Select **Create Organization**.

    **Note:**

    -   After a new organization is created, you’ll receive confirmation within the platform. You can manage your organization settings, add members, and configure workspaces within your newly created organization.

    -   To see to the official Terraform documentation:
        -   Terraform Cloud: [https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/organizations](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/organizations)
        -   Terraform Enterprise: [https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/organizations](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/organizations)
5.  In Terraform org, navigate to **Settings** &gt; **Variable set** &gt; **Create variable set**.

    A variable set is a collection of variables shareable across multiple workspaces.

6.  Provide a descriptive name like AWS credentials.

7.  Select the appropriate scope \(organization or a workspace\).

8.  Create two variable sets within the **Variables** section as follows:

    -   Key: AWS\_ACCESS\_KEY\_ID and Value: &lt;AWS access key&gt;
    -   Key: AWS\_SECRET\_ACCESS\_KEY and Value: &lt;AWS secret key&gt;

        **Note:** Select as **Sensitive** to restrict the visibility of credentials to unauthorized personnel with Terraform access.

    For more details on variable sets, see [https://developer.hashicorp.com/terraform/tutorials/cloud-get-started/cloud-create-variable-set\#](https://developer.hashicorp.com/terraform/tutorials/cloud-get-started/cloud-create-variable-set).


**Parent Topic:**[Setting up Terraform and GitHub](../concept/about-terraform-git-and-servicenow_0.md)

**Related topics**  


[Publish Terraform templates](publish-terraform-templates.md)

[Integrate Terraform Cloud with GitHub](integrate-terraform-cloud-and-git.md)

[Create Terraform API token](set-up-administrator-api-key.md)

