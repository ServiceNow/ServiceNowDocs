---
title: Add the Enrollment Reader role to the Microsoft Azure service principal
description: Assign the Enrollment Reader role to the Azure service principal for your Enterprise Agreement \(EA\) account to retrieve billing, purchase, and pricing data. You can assign this role using a Microsoft API.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-02-12"
reading_time_minutes: 1
breadcrumb: [Set up access to Microsoft Azure billing and usage data, Configure Cloud Cost Management for Microsoft Azure, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add the Enrollment Reader role to the Microsoft Azure service principal

Assign the Enrollment Reader role to the Azure service principal for your Enterprise Agreement \(EA\) account to retrieve billing, purchase, and pricing data. You can assign this role using a Microsoft API.

## Before you begin

Role required: Enterprise administrator \(EA\)

## About this task

Enrollment reader roles can view subscription charges related data at the enrollment, department, and account scopes. They can also view the Azure prepayment balance linked with the enrollment. Enrollment reader role is required only for EA accounts.

## Procedure

1.  Navigate to the [Role Assignments - Put](https://learn.microsoft.com/en-us/rest/api/billing/role-assignments/put?view=rest-billing-2019-10-01-preview&tabs=HTTP) page in the Microsoft Azure documentation.

2.  Run the API by selecting the **Try It** button.

3.  Select **Sign in**.

4.  On the login page, enter your Microsoft Azure account credentials to sign in to the tenant.

5.  On the API request parameters form, fill in the fields.

<table id="table_pzf_gps_32c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

billingAccountName

</td><td>

The Azure EA billing account ID.You can find the billing account ID on the Azure portal on the Cost Management + Billing overview page.

</td></tr><tr><td>

billingRoleAssignmentName

</td><td>

A unique ID to identify the name of the role that you want to assign.You can use a GUID generator website to generate a unique ID.

</td></tr><tr><td>

Body

</td><td>

The request body with parameters in JSON code. Enter the following JSON code in the body.`{ "properties": { "principalId": "{enterprise-application (or SPN) object-id}", "principalTenantId": "{tenant-id}", "roleDefinitionId": "/providers/Microsoft.Billing/billingAccounts/{ea-account-id}/billingRoleDefinitions/24f8edb6-1668-4659-b5e2-40bb5f3a7d7e" } }`

In this code:

-   principalID: object ID of the EA account
-   principalTenantID: tenant \(directory\) ID of the EA account
-   roleDefinitionId: ID of the role definition, for example, 24f8edb6-1668-4659-b5e2-40bb5f3a7d7e is the role definition ID of the enrollment reader role
For details on the object ID and tenant ID, see [Microsoft documentation](https://learn.microsoft.com/en-us/azure/cost-management-billing/manage/assign-roles-azure-service-principals#find-your-service-principal-and-tenant-ids).

**Important:** Replace only the `ea-account-id` string with the actual EA billing account ID.

</td></tr></tbody>
</table>    **Note:** You must not change the values in the **api-version** and **Content-Type** fields.

6.  Complete the role assignment for the Azure EA account by selecting **Run**.


## What to do next

[Schedule and manage the jobs that download Azure billing data](schedule-azure-billing-job.md)

