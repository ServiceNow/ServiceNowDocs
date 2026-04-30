---
title: Publish Terraform templates
description: Publish the Terraform template defined by the application in GitHub to enable version control, collaboration, and centralized storage.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up Terraform and GitHub, Provisioning modes for Cloud Account Management in Cloud Workspace, Setting up AWS cloud, Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Publish Terraform templates

Publish the Terraform template defined by the application in GitHub to enable version control, collaboration, and centralized storage.

## Before you begin

Role required: Terraform admin

## Procedure

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


**Parent Topic:**[Setting up Terraform and GitHub](../concept/about-terraform-git-and-servicenow_0.md)

**Related topics**  


[Create a Terraform organization for Cloud Account Management in Cloud Workspace](integrate-terraform-and-git.md)

[Integrate Terraform Cloud with GitHub](integrate-terraform-cloud-and-git.md)

[Create Terraform API token](set-up-administrator-api-key.md)

