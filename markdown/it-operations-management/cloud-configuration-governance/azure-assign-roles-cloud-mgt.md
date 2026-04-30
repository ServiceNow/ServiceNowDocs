---
title: Assign roles to Azure users of Cloud Provisioning and Governance
description: You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Day 1 setup guide for Microsoft Azure Cloud on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Assign roles to Azure users of Cloud Provisioning and Governance

You assign Cloud Provisioning and Governance roles to user groups and to individual users based on user activities and responsibilities.

## Before you begin

Role required: user\_admin or admin

## Procedure

1.  Assign the following roles to groups and users as appropriate:

<table id="table_bvg_1fw_vy"><thead><tr><th>

Descriptive name and role name

</th><th>

Description and tasks

</th><th>

Access rights in Cloud Provisioning and Governance

</th></tr></thead><tbody><tr><td>

Root administrator `[sn_cmp.cmp_root_admin]`

</td><td>

Highest level of application access for Cloud Provisioning and Governance.

</td><td>

All

</td></tr><tr><td>

Cloud administrator `[sn_cmp.cloud_admin]`

</td><td>

Configures the Cloud Provisioning and Governance application and sets up the cloud infrastructure.

</td><td>

Cloud infrastructure:Service accounts and cloud account

 Networks and IPAM

 Settings for provider services that auto-update the CMDB:

-   AWS Config
-   Azure Alert
-   Google Cloud Logging
-   IBM Cloud Update
-   VMware Events


</td></tr><tr><td>

Governor`[sn_cmp.cloud_governor]`

</td><td>

Monitors overall cloud usage and enforces compliance of the organization's rules, quotas, and policies. Also manages tags and permissions to various objects.

</td><td>

Governance:-   Policies
-   Pools
-   Quotas
-   Permissions


</td></tr><tr><td>

Service Designer `[sn.cmp.cloud_service_designer]`

</td><td>

Creates blueprints, ARM and CloudFormation templates, and catalog items.

</td><td>

Cloud Service Design:-   Cloud templates
-   Blueprints
-   Blueprint catalog items
-   Resource blocks


</td></tr><tr><td>

Cloud user `[sn_cmp.cloud_service_user]`

</td><td>

Requests and manages stacks and resources.

</td><td>

Cloud User Portal.When you assign the role to a group, all members of the group share quota limitations and ownership of certain resources.

You can access all the task records, assigned to you or otherwise, if you have the cloud service user role.

</td></tr><tr><td>

Cloud operator`[sn_cmp.cloud_operator]`

</td><td>

Monitors and troubleshoots the Cloud Provisioning and Governance application.

</td><td>

Dashboards and reports:-   Cloud Operations Dashboard
-   Cloud Root Cause Analysis
-   Cloud Orchestration Trail
-   Cloud API Trail


</td></tr><tr><td>

Cloud Event Integration`[sn_cmp.cloud_event_integration]`

 **Note:** Not supported by IBM Cloud Connector.

</td><td>

Authorizes access to the instance for external services that auto-update the CMDB when cloud events occur. This role gives the access to the cloud event REST endpoint.

</td><td>

Cloud infrastructure:

-   Service accounts and cloud account
-   Networks and IPAM
 Settings for provider services that auto-update the CMDB:

-   AWS Config
-   Azure Alert
-   Google Cloud Logging
-   VMware Events


</td></tr><tr><td>

Cloud Group administrator`[sn_cmp.cloud_group_admin]`

</td><td>

Grants admin access to any group that you belong to.

</td><td>

 

</td></tr></tbody>
</table>
**Related topics**  


[Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

[Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

