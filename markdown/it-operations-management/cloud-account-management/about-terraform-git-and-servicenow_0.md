---
title: Setting up Terraform and GitHub
description: Simplify cloud account provisioning using Terraform. The workflow provides the basic steps involved in setting up Terraform and GitHub.Publish the Terraform template defined by the application in GitHub to enable version control, collaboration, and centralized storage.Integrate with Terraform Cloud/Terraform Enterprise to organize accounts, define workflows, enforce security, improve collaboration, and enhance scalability.Integrate GitHub with Terraform to link workspaces to repositories, enabling version control, change tracking, and rollbacks.Generating API tokens with limited permissions enhances security, enables fine-grained control, facilitates automation, and provides temporary access within your Terraform organization.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2024-03-14"
reading_time_minutes: 5
breadcrumb: [Provisioning modes for Cloud Account Management in Cloud Workspace, Setting up AWS cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Setting up Terraform and GitHub

Simplify cloud account provisioning using Terraform. The workflow provides the basic steps involved in setting up Terraform and GitHub.

**Parent Topic:**[Cloud Account Management](cam-landing.md)

## Publish Terraform templates

Publish the Terraform template defined by the application in GitHub to enable version control, collaboration, and centralized storage.

### Before you begin

Role required: Terraform admin

### Procedure

1.  Create a GitHub repository dedicated to your Terraform templates.

2.  Save the following codes in a separate file.

    -   File name: awsaccount.tf

        ```
        terraform {
          required_providers {
            aws = {
              source  = "hashicorp/aws"
              version = "~>5.0"
            }
          }
        }
        
        provider "aws" {
          region = var.region
        }
        
        resource "aws_organizations_account" "account" {
          email = var.root_email
          name = var.account_name
          tags = var.tags
          parent_id = var.parent_id
          close_on_deletion=var.close_delete
          create_govcloud=var.gov_cloud
        }
        
        resource "aws_budgets_budget" "cost" {
          name  = join("-", ["SN-CAM-Monthly-Budget", aws_organizations_account.account.id])
          count = var.monthly_budget > 0 ? 1 : 0
          budget_type  = "COST"
          limit_amount = var.monthly_budget
          limit_unit   = "USD"
          time_unit    = "MONTHLY"
        
          cost_filter {
            name = "LinkedAccount"
            values = [
              aws_organizations_account.account.id
            ]
          }
        
          notification {
            comparison_operator        = "GREATER_THAN"
            threshold                  = 100
            threshold_type             = "PERCENTAGE"
            notification_type          = "FORECASTED"
            subscriber_email_addresses = [var.root_email, var.notification_email]
          }
        
          notification {
            comparison_operator        = "GREATER_THAN"
            threshold                  = 85
            threshold_type             = "PERCENTAGE"
            notification_type          = "ACTUAL"
            subscriber_email_addresses = [var.root_email, var.notification_email]
          }
        
          notification {
            comparison_operator        = "GREATER_THAN"
            threshold                  = 100
            threshold_type             = "PERCENTAGE"
            notification_type          = "ACTUAL"
            subscriber_email_addresses = [var.root_email, var.notification_email]
          }
        }
        ```

    -   File name: variables.tf

        ```
        variable "region" {
          type = string
          default = "us-east-1"
        }
        
        variable "account_name" {
          type = string
          description = "(Required) Account Name"
        }
        
        variable "root_email" {
          type = string
          description = "(Required) Account Email"
        }
        
        variable tags{
          type = map(string)
          description = "(Required) Tags for the resource"
        }
        
        variable "close_delete" {
          type = bool
          description = "Close Account on deletion"
          default = true
        }
        
        variable "gov_cloud" {
          type = bool
          description = "Gov Cloud Account"
          default = false
        }
        
        variable "parent_id" {
          type = string
          description = "(Required) Account Parent Organizational Unit"
        }
        
        variable monthly_budget {
          type = number
          default = 0
        }
        
        variable notification_email {
          type = string
          description = "Additional email where Budget Notifications are to be sent"
        }
        ```

3.  Push the Terraform files to the remote repository.

4.  Make a note of the location or URL once the template is stored in the GitHub.

    This template is then referenced in Terraform Cloud and the ServiceNow instance to automate the creation of a subscription account.

    **Important:**

    Don’t modify the template as the variables are closely connected to the application.


## Create a Terraform organization for Cloud Account Management in Cloud Workspace

Integrate with Terraform Cloud/Terraform Enterprise to organize accounts, define workflows, enforce security, improve collaboration, and enhance scalability.

### Before you begin

Role required: Terraform admin

Attributes required for this setup:

-   AWS Access Key
-   AWS Secret Key

Make sure you have access to Terraform Cloud or Terraform Enterprise to perform the following procedure.

### Procedure

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


## Integrate Terraform Cloud with GitHub

Integrate GitHub with Terraform to link workspaces to repositories, enabling version control, change tracking, and rollbacks.

### Before you begin

Role required: Terraform admin or DevOps team member

### Procedure

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


### What to do next

Make a note of the OAuth Token ID and share it with the ServiceNow admin.

![GitHub OAuth Token ID](../image/git-oauth-token.png)

## Create Terraform API token

Generating API tokens with limited permissions enhances security, enables fine-grained control, facilitates automation, and provides temporary access within your Terraform organization.

### Before you begin

Role required: Terraform admin

### Procedure

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

### What to do next

[Setting up Cloud Account Management in Cloud Workspace](configuring-cloud-workspace.md)

[Add members to the group](../task/add-member-group.md)

[Set up Terraform API key in ServiceNow](../task/configure-api-key.md).

[Set up scan configuration for data visualization](../task/set-up-data-visualization.md).

