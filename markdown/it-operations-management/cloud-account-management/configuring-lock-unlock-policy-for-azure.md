---
title: Set up suspension of a subscription using Azure policy
description: Create the policy at the root level to lock or unlock an Azure account. As an Azure administrator, lock an Azure subscription, resource group, or resource to avoid accidental deletions and modifications.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up Azure cloud, Configuring cloud providers, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Set up suspension of a subscription using Azure policy

Create the policy at the root level to lock or unlock an Azure account. As an Azure administrator, lock an Azure subscription, resource group, or resource to avoid accidental deletions and modifications.

## Before you begin

Make sure you have already configured the permission. For more information, see [Configure account suspension in Azure](configuring-azure-suspension-permission.md).

Role required: Azure admin

## Procedure

1.  Sign in to the Azure organization.

2.  Search for and select **Users**.

3.  Under the user name list, select a user.

4.  From the navigation pane, select **Assigned roles**.

5.  Under the Administrative roles, add the **Global Administrator** role by selecting **Add Assignments**.

6.  Enter `Microsoft Entra ID` in the search box and select **Microsoft Entra ID** &gt; **Properties**.

7.  Under **Access Management for Azure resources**, set the toggle to **Yes**.

    Using this option, you can manage access to all Azure subscriptions and management groups in this tenant.

8.  Search for and select **Policy**.

9.  Select **+ Policy definition**.

10. Enter the following:

    1.  Select the tenant root group using the ellipsis on **Definition location**.

        You can select either a management group or a subscription. If you select the tenant root group, all child subscriptions can also be managed.

    2.  Enter the name of the policy definition. For example, LockAccount\_policy.
    3.  The description of what the policy definition is intended to do.
    4.  Under POLICY RULE, copy the following JSON code:

        ```
        {
            "properties": {
                "displayName": "CAM_LockAccount_Policy",
                "policyType": "Custom",
                "mode": "All",
                "description": "Blocks the creation of resources and configurations that fall under Azure Policy enforcement.",
                "parameters": {
                    "allowedResourceTypes": {
                        "type": "Array",
                        "metadata": {
                            "displayName": "Allowed Resource Types",
                            "description": "List of resource types that are allowed for creation. Any resource type not listed here will be blocked.",
                            "strongType": "resourceTypes"
                        },
                        "defaultValue": []
                    },
                    "allowedLocations": {
                        "type": "Array",
                        "metadata": {
                            "displayName": "Allowed Locations",
                            "description": "List of allowed Azure regions for resource creation."
                        },
                        "defaultValue": []
                    },
                    "effect": {
                        "type": "String",
                        "metadata": {
                            "displayName": "Effect",
                            "description": "The effect determines what happens when the policy rule is evaluated to match"
                        },
                        "allowedValues": [
                            "Audit",
                            "Deny",
                            "Disabled"
                        ],
                        "defaultValue": "Deny"
                    }
                },
                "policyRule": {
                    "if": {
                        "anyOf": [
                            {
                                "not": {
                                    "field": "type",
                                    "in": "[parameters('allowedResourceTypes')]"
                                }
                            },
                            {
                                "not": {
                                    "field": "location",
                                    "in": "[parameters('allowedLocations')]"
                                }
                            }
                        ]
                    },
                    "then": {
                        "effect": "[parameters('effect')]"
                    }
                }
            }
        }
        ```

    5.  Select **Save**.

        **Note:** To verify if the policy is created, go to PolicyDefinitions. Change the filter Scope and Policy type to find the policy.

    6.  Select the policy name and copy the **Definition ID**.
    **Note:** This Definition ID is required when you [Create a suspend account configuration](create-suspend-account-config.md).


## What to do next

[Setting up Cloud Account Management in Cloud Workspace](../concept/configuring-cloud-workspace.md)

[Add members to the group](add-member-group.md)

[Set up Azure connection](../concept/set-up-azure-connector.md)

[Set up scan configuration for data visualization](set-up-data-visualization.md)

