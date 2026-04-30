---
title: Configure account suspension in Azure
description: Manage an Azure subscription using the permission and by assigning the role to a user. The role must have the permission to execute the APIs for suspending and reactivating an Azure account.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up Azure cloud, Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Configure account suspension in Azure

Manage an Azure subscription using the permission and by assigning the role to a user. The role must have the permission to execute the APIs for suspending and reactivating an Azure account.

## Before you begin

Role required: Azure admin

## Procedure

1.  Sign in to the Azure organization.

2.  Search and select **Management groups**.

3.  Select **Tenant Root Group**.

4.  Select **Access Control** &gt; **Roles**.

5.  Select **Add** and then select **Add custom role**.

6.  In the **Custom role name** box, specify a name for the custom role.

    The name must be unique for the Microsoft Entra directory.

7.  Select **Next**.

8.  On the **Permissions** tab, select **Next**.

9.  On the **Assignable scopes** tab, you specify where your custom role is available for assignment, such as management group, subscriptions, or resource groups.

10. Select Add assignable scopes to open the Add assignable scopes pane.

11. On the **JSON** tab, paste the following code:

    ```
    {
        "properties": {
            "roleName": "Policy Lock/Unlock Manager",
            "description": "Allows locking and unlocking Azure Policy assignments at management group level",
            "assignableScopes": [
                "/providers/Microsoft.Management/managementGroups/<ManagementGroupId>” 
            ],
            "permissions": [
                {
                    "actions": [
                        "Microsoft.Authorization/policyAssignments/write",
                        "Microsoft.Authorization/policyAssignments/delete",
                        "Microsoft.Authorization/policyAssignments/read"
                    ],
                    "notActions": [],
                    "dataActions": [],
                    "notDataActions": []
                }
            ]
        }
    }
    ```

12. Select **Next** and then select **Create**.


## What to do next

You must assign the permission to a role. For more information, see [https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal](https://learn.microsoft.com/en-us/azure/role-based-access-control/role-assignments-portal).

Configure a lock/unlock policy. For more information, see [Set up suspension of a subscription using Azure policy](configuring-lock-unlock-policy-for-azure.md).

