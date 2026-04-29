---
title: Integrate Terraform Cloud with GitHub
description: Integrate GitHub with Terraform to link workspaces to repositories, enabling version control, change tracking, and rollbacks.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Terraform and GitHub, Provisioning modes for Cloud Account Management in Cloud Workspace, Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Integrate Terraform Cloud with GitHub

Integrate GitHub with Terraform to link workspaces to repositories, enabling version control, change tracking, and rollbacks.

## Before you begin

Role required: Terraform admin or DevOps team member

## Procedure

1.  Go to the Terraform org created for this application.

2.  Navigate to **Settings** &gt; **Providers**.

3.  Select **Add a VCS provider**.

4.  From the GitHub drop-down list, choose a **GitHub.com \(Custom\)**.

5.  Select the link **Register a new OAuth Application**.

    ![Terraform CVS provider registration form](../image/register-oauth.png)

6.  Select **Register application**.

7.  Copy the client ID.

8.  Select **Generate a new client secret** and copy the generated Client Secret.

9.  Go back to the Terraform console where the **Add a VCS provider** page is open and paste both Client ID and Client Secret.

    ![Terraform VCS provider page](../image/terraform-vcs-form.png)

10. Select **Connect and continue**.

11. Select **Authorize**.

    **Note:** Follow the platform-specific instructions to authorize Terraform Cloud to access your GitHub repository.

    For more details, see the official documentation: [https://developer.hashicorp.com/terraform/cloud-docs/vcs/Github-enterprise](https://developer.hashicorp.com/terraform/cloud-docs/vcs/github-enterprise).

12. On the **Advance Settings** page, select **Skip and finish**.


## What to do next

Make a note of the OAuth Token ID and share it with the ServiceNow admin.

![GitHub OAuth Token ID](../image/git-oauth-token.png)

**Parent Topic:**[Setting up Terraform and GitHub](../concept/about-terraform-git-and-servicenow_0.md)

**Related topics**  


[Publish Terraform templates](publish-terraform-templates.md)

[Create a Terraform organization for Cloud Account Management in Cloud Workspace](integrate-terraform-and-git.md)

[Create Terraform API token](set-up-administrator-api-key.md)

