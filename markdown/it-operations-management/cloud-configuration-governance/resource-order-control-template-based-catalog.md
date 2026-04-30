---
title: Resource order controls for template-based cloud catalog items
description: Use resource order controls to perform quota checks for template-based catalog items using quota definitions and policies. Quota limits enable you to control provisioning or ordering resources for users and groups. Configure policy actions to trigger notifications, an approval workflow, or both.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Quotas and resource order controls, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Resource order controls for template-based cloud catalog items

Use resource order controls to perform quota checks for template-based catalog items using quota definitions and policies. Quota limits enable you to control provisioning or ordering resources for users and groups. Configure policy actions to trigger notifications, an approval workflow, or both.

## Resource Order Controls

Resource order controls enable you to control the quota limit of resources provisioned through template-based catalogs. Quota checks for cloud template-based catalog items are available beginning with the Xanadu release.

You can now map quota limits to template-based catalogs and trigger notifications or an approval workflow when the resource limit or quota definitions you specify for a user or user group is exceeded. For more information, see [Resource Quota](../../cloud-management-v2-user/concept/resource-quota.md).

Use resource controls to perform the following actions:

-   Calculate quota and capacity for template-based catalog items.
-   Set limits for stack quota during provisioning for the cloud user.
-   Create a policy to be triggered when a quota limit is exceeded.
-   Add a policy notification and request for approval when a quota limit is exceeded.
-   Show user and user group quotas for template-based catalogs in the Cloud User portal.

## How resource order controls work

Resource order control applies only when the quota has exceeded. If the quota exceeds during catalog provisioning for the first time after resource order controls are configured, the cloud resources continue to be provisioned. However, if the cloud user tries to provision a resource that breaches the configured quota limits again, the Resource order limit exceeded policy action set up for the Resource Order Control policy is triggered.

**Note:** If quota is not mapped to a template-based catalog, quota calculations for that catalog are not performed, even if users exceed their quota limits.

For example, say you specify a quota limit of 20 GB for a storage volume for a cloud user and the user provisions a 40 GB storage volume. The first time, the storage volume is provisioned even though it exceeds the quota limit. However, provisioning will fail the next time the user attempts to provision a cloud resource over 20 GB.

## Stack count quota

The stack count quota introduces a default base system quota for template-based cloud catalog items. The Stack count quota counts all active stacks \(identified by the **Stack** CI class\) provisioned by users and user groups. The stack count quota applies to all template-based cloud resources and you do not need to map catalog items to quota definitions. Once the stack quota is enabled, whenever a user from the group mapped to the stack quota provisions a cloud resource, the quota is calculated. When users from the mapped group try to provision resources beyond the limit defined in the quota definition for stacks, the Resource Order Control policy and **on Resource Limit exceeded** policy action is triggered.

**Note:** The base system stack count quota does not have predefined default quotas to preserve stacks that might have been created prior to upgrading to Xanadu. You must specify default quota limits for users and user groups to enable the Stack count quota.

## Resource Order Control Policy

The Resource Order Control policy is a base system policy that is in the Draft state by default. You can customize the default policy to meet your requirements and publish it, or create a new policy and define quotas, rules and actions to enable resource order controls. The 'on Resource Limits exceeded' policy action triggers the Resource Order Control policy when any resource exceeds the defined quota limit. You can determine whether to initiate an approval workflow, a notification, or a combination of both when the resource limit exceeded policy is triggered. For more information, see [Create an action for an 'on Resource Limit exceeded' policy](../task/create-action-on-resource-limits-exceeded.md).

**Note:** You cannot provision catalog items once the user or user group quota is exceeded without the policy being published because the existing quota behavior disables further provisioning and does not process the request further.

## Next Steps

-   **[Set up resource order controls](../task/set-up-resource-order-controls.md)**  
Create quota definitions and policies mapped to cloud-template based catalog items. Use policy rules and actions to trigger an approval workflow or notification when the quota limit defined for the group or user exceeds.

**Parent Topic:**[Quotas and resource order controls](quotas.md)

