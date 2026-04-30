---
title: Add the Billing Profile Reader role to the Microsoft Azure service principal
description: Assign the Billing Profile Reader role to the Azure service principal for your Microsoft Customer Agreement \(MCA\) account to download Azure price sheet data.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configure, Cloud Cost Management, IT Asset Management]
---

# Add the Billing Profile Reader role to the Microsoft Azure service principal

Assign the Billing Profile Reader role to the Azure service principal for your Microsoft Customer Agreement \(MCA\) account to download Azure price sheet data.

## Before you begin

Role required: Azure Cloud admin

## About this task

The Billing Profile Reader role provides the required permissions to download price sheet data at the profile scope only for MCA accounts. For more information on Azure roles, see [Microsoft documentation](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal).

## Procedure

1.  Log in to the [Azure portal](https://portal.azure.com) and search for **Cost Management + Billing**.

2.  Select **Billing scopes**.

3.  Select **Access Control \(IAM\)** at the billing profile scope to which you’re assigning the billing profile reader role.

4.  Select **+Add**.

5.  In the Add role assignment window, select **Billing profile reader** in the **Role** field.

6.  In the **Users, groups, or apps** field, select the service principal to which you’re assigning the role.

7.  Complete the role assignment for the Azure MCA account by selecting **Add**.


## What to do next

[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

**Related topics**  


[Schedule and manage the Cloud Cost Management jobs that download Microsoft Azure price sheets](azure-pricesht-sched-dwnld-cloudin.md)

