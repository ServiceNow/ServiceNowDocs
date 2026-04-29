---
title: Create Terraform API token
description: Generating API tokens with limited permissions enhances security, enables fine-grained control, facilitates automation, and provides temporary access within your Terraform organization.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Terraform and GitHub, Provisioning modes for Cloud Account Management in Cloud Workspace, Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Create Terraform API token

Generating API tokens with limited permissions enhances security, enables fine-grained control, facilitates automation, and provides temporary access within your Terraform organization.

## Before you begin

Role required: Terraform admin

## Procedure

1.  Log in to the Terraform console.

2.  Select **Account Settings** from the user profile.

3.  Select **Tokens** and then select **Create an API token**.

4.  Enter **Description**.

5.  Set the **Expiration** date.

    **Note:** The expiration date should align with the security standards of your company.

6.  Select **Generate token**.

7.  Share the following details with the ServiceNow admin to register in the ServiceNow instance:

    -   VCS Identifier or the GitHub repository location, where you have stored the Terraform template, for example: `https://github.com/<your_repository>/cam-create-aws-account`.
    -   Terraform Organization Name
    -   Terraform OAuth Token ID
    -   Terraform API Key Token
    -   Terraform URL

## What to do next

[Setting up Cloud Account Management in Cloud Workspace](../concept/configuring-cloud-workspace.md)

[Add members to the group](add-member-group.md)

[Set up Terraform API key in ServiceNow](configure-api-key.md).

[Set up scan configuration for data visualization](set-up-data-visualization.md).

**Parent Topic:**[Setting up Terraform and GitHub](../concept/about-terraform-git-and-servicenow_0.md)

**Related topics**  


[Publish Terraform templates](publish-terraform-templates.md)

[Create a Terraform organization for Cloud Account Management in Cloud Workspace](integrate-terraform-and-git.md)

[Integrate Terraform Cloud with GitHub](integrate-terraform-cloud-and-git.md)

