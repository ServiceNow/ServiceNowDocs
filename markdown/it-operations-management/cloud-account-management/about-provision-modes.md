---
title: About provision modes in Cloud Account Management
description: Cloud Account Management supports both Terraform \(Cloud and Enterprise\) and cloud native interface provision modes.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Terraform working in Cloud Workspace]
breadcrumb: [Explore, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# About provision modes in Cloud Account Management

Cloud Account Management supports both Terraform \(Cloud and Enterprise\) and cloud native interface provision modes.

## Terraform support

Terraform templates are configuration files that specify the infrastructure resources needed for a specific application or environment using the Hashicorp Configuration Language \(HCL\). Cloud Account Management dynamically retrieves Terraform credentials and templates from the Git repository during the Terraform account creation process. Using the Terraform template, the ServiceNow instance interacts with the cloud organization’s IAM \(Identity and Access Management\) to retrieve the user's identity.

## Cloud native interface support

An AWS or Azure admin creates the IAM user with the specified permissions, and the Cloud Account Management admin enters the credentials of the IAM user into the ServiceNow instance. No additional steps are required for users to access the cloud native interface.

![Terraform and cloud native interface support in a Cloud Account Management instance](../image/terraform.png "Cloud Account Management provision modes")

