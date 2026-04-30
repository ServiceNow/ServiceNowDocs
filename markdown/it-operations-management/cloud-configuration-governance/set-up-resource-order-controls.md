---
title: Set up resource order controls
description: Create quota definitions and policies mapped to cloud-template based catalog items. Use policy rules and actions to trigger an approval workflow or notification when the quota limit defined for the group or user exceeds.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Resource order controls for template-based cloud catalog items, Quotas and resource order controls, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Set up resource order controls

Create quota definitions and policies mapped to cloud-template based catalog items. Use policy rules and actions to trigger an approval workflow or notification when the quota limit defined for the group or user exceeds.

## Before you begin

You must have the following items:

-   One or more cloud policy groups.
-   Cloud template-based catalog items.
-   Ensure that your CMDB is updated through event-driven discovery for precise quota enforcement.
-   Ensure that you map quota to a catalog in the Cloud Template Resources related list, when you configure quota definitions.

Role required: sn\_cmp.cloud\_governor

## About this task

Consider the following points before you begin setting up resource order controls:

-   Quota is calculated only for the resource blocks that are bound to a CI class on the CMDB. If you create custom resource blocks that do not map to CI class on the CMDB, no quota calculation is performed for those resource types.
-   If you have configured both Resource Order Control policy and a blueprint provision approval policy, the blueprint provisioning policy takes precedence over the Resource Order Control approval policy.

## Procedure

1.  Define the quota or use a base system quota definition for a resource block.

    1.  In the Cloud Admin Portal, navigate to **Govern** &gt; **Quota** &gt; **Quota Definition**.

    2.  Specify quota definitions.

        The Resource Order Control base system policy has the default ServiceNow approval policy rule configured by default. If you want to trigger other actions such as notifications or a custom approval workflow when the resource limit is exceeded, you can either modify the base system policy action or create a custom policy for your instance.

    -   Modify a base system quota definition by specifying the default quota values per user and user group and the user groups to which the defined quota applies.

        The following predefined base system quotas have default quota definitions:

        -   **VM\_Count**
        -   **vCPUs Count**
        -   **StorageVolume\_Size**
        -   **Stack\_Count**
        -   **Network\_Count**

            **Important:** **Stack\_Count** is applicable only to template-based cloud resources.

    -   Create a quota definition.

        For more information see, [Create a cloud quota definition](create-cloud-quota.md).

2.  Map the quota to a template-based cloud catalog item.

    **Important:** If quota is not mapped to template-based catalogs when you configure quota definitions, quota calculations for those catalogs are not performed, even if user-define quotas exceed. For more information, see [Create a cloud quota definition](create-cloud-quota.md)

    1.  In the Cloud Template Resources related list, click **New**.

    2.  In the **Catalog Item** field, select the catalog item you want to map this quota definition to.

    3.  Click **Submit**.

3.  Configure a policy rule.

    1.  Navigate to **Govern** &gt; **Policies**.

    2.  Open the base system Resource Order Control policy.

        By default, the base system resource order control policy is in Draft state.

    3.  Navigate to the Rules related list and either modify a base system rule or configure a new rule if you have numerous customizations.

    -   Select the base system **approveresourcelimit** rule and modify it to include a policy action triggering a custom workflow or a notification.

        **Note:** By default, only the ServiceNow approval action is configured for the **approveresourcelimit** rule.

    -   Click **New** and configure a new policy rule.

        For more information, see [Configure a cloud policy rule](configure-cloud-policy-rule.md).

4.  Configure a policy rule action.

    -   Select the base system approve policy rule action in the Policy Rule Actions related list to include a notification or a custom approval workflow.
    -   Create a cloud policy rule action in the Policy Rule Actions related list, to trigger custom approval workflows or notifications, if you created a policy rule in the previous step.

        For more information, see [Create an action for 'on Resource Limit exceeded' policy](create-action-on-resource-limits-exceeded.md).

    **Note:** In the **Policy Group** field, ensure that the policy group you want this policy to apply to is selected.

5.  Publish the policy to activate resource order controls by clicking **Update** and then **Publish**.


## Result

Based on the Policy Rule action you configured for the Resource order control policy, either an email notification or an approval workflow or both will be triggered if the specified quota is exceeded.

If you have configured an approval policy, the requester receives a notification stating that the approval request has been sent to a designated approver on exceeding the specified quota. Typically, the assigned approver designed the template used to create the cloud resource and has the **sn\_cmp.cloud\_service\_designer** role.

**Parent Topic:**[Resource order controls for template-based cloud catalog items](../concept/resource-order-control-template-based-catalog.md)

