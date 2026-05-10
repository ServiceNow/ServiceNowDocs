---
title: On-board a Company
description: Review the following considerations to on-board customers or companies in a domain separated instance, for Cloud Provisioning and Governance services.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Domain separation in Cloud Provisioning and Governance - considerations for service providers, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# On-board a Company

Review the following considerations to on-board customers or companies in a domain separated instance, for Cloud Provisioning and Governance services.

## Domain separation for Cloud Provisioning and Governance overview

Domain separation for Cloud Provisioning and Governance is designed to give Service Providers a multi-tenant instance architecture that delivers offerings efficiently and securely to their clients. Strong universal process standards, data-driven process design, strict governance, and centralized administration maximize these benefits.

## Customer On-boarding by Service Providers

-   [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

    Domain Separation in Cloud Provisioning and Governance is achieved by installing and configuring one or more dedicated MID Servers for each company/ domain that you are managing in your instance. Specifying a MID Server for each domain/company, ensures that Config Items \(CIs\) are assigned to the intended domain. Each domain has one or more MID Servers setup for cloud discovery, provisioning, and other orchestration.

    **Note:** Create a MID Server in the global domain so that you can explore targets in other domains. For more information, see [Set up domain separation for MID servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerDomainSeparation.md)

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The MID Server enables communication and the movement of data between a ServiceNow® instance and external applications, data sources, and services.

    To communicate with the instance, MID Servers need a user ID and the appropriate role. Create the user ID for a MID Server and grant the ID the **mid\_server** role. To prevent MID Server validation failure, the system runs business rules to monitor the settings selected for MID Server users.

-   [Setting up the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

    For more information on setting up the MID Server, see:

    -   [Installing the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-installation.md)
    -   [Configuring MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerConfiguration.md)
-   [Resource Blocks in Cloud Provisioning and Governance](../concept/resource-blocks.md)

    Create Resource Blocks in global domain as there is a 1:1 relationship between CI and resource block. Do not create resource blocks in any of the child or leaf domains. Resource blocks act as a process record, so any template of a parent domain is visible and works in the child domain.

    Resource blocks act as a type of middleware component between catalog items, the Cloud API \(CAPI\), and the CMDB.

    -   -   If the blocks in the base system do not provide the cloud resources that you need to provision, you can [create a custom resource block](../task/create-resource-block.md).
-   In the Cloud Provisioning and Governance application, script execution is divided into cloud scripts and cloud script templates. Use scripts in catalog items, resource blocks, OS profiles, and use policy scripts to set request form attributes. Policy scripts cannot override user data. For more information, see [Cloud scripts and cloud script templates](../concept/cloud-scripts-and-templates.md).
-   [Map a script to an OS profile](../task/map-script-to-os-profile.md)

    To execute scripted actions during VM provisioning, you can map a script to an OS profile. The script runs on VMs that are created based on the image template in the OS profile.

    -   [Define Resource Profile](../concept/cloud-resource-profiles.md)

        Create resource profile definitions in the global domain, and create mappings to these definitions in the child \(leaf\) domains. Do not delete resource profiles without checking with all impacted companies. You can create domain-specific resource pools and pools filters for all supported cloud providers. As a Domain admin you can see global, domain and custom resource pools specific to sub-domains. A resource pool is a query or script that filters a table. You configure a resource pool to limit the values that are available to users when they request a catalog item. For domain separated resource pools only records of the relevant domain are returned.

        Resource profiles are cloud provider-agnostic definitions that specify the allowed attribute values for a resource. Resource profiles enable you to control the choices that the user sees when requesting a cloud resource. As a result, you do not need to define a unique blueprint for each variation of the resource.

-   Administer and set up Cloud Provisioning and Governance for Quota, Policies, Pools, Permissions. Governance refers to the limitations that you can set on available cloud resources. As an SP you could manage process separation in Cloud Provisioning and Governance policies, and permissions for each company or domain you are managing in your instance. Policies are recommended to be set up in global domain only. Process separation at a domain level is achievable for governance and policies. For customized policy enforcement, use company field in the policy rule condition to target a policy towards the particular domain.

    |Type|Description|
    |----|-----------|
    |[Quotas](../concept/quotas.md)|Quotas are limitations or requirements for groups and users on CIs or cloud resources. Use quotas to prevent wasteful resource usage in your cloud environment.|
    |[Policies](../concept/cloud-policy.md)|A cloud policy can override a property value set by a user, create an approval task, reserve an IP address, pre-populate or hide form fields, execute custom scripts, call the Cloud API, or start or abort subflows. A cloud policy gives you system-wide control over approvals, resource operations, blueprint operations, or catalog item settings.|
    |[Pools](../concept/pools.md)|A resource pool is a query or script that filters a table. You configure a resource pool to limit the values that are available to users when they request a catalog item.|
    |[Permissions](../concept/cloud-permissions.md)|Permissions are user group-level access rights to features in the Cloud Provisioning and Governance application and to specific records in the instance, such as blueprints or cloud accounts.|

    Permissions are user group-level access rights to features in the Cloud Provisioning and Governance application and to specific records in the instance, such as catalog items or cloud accounts. You could also set up basic governance policies, quotas, pools, and allow the cloud admin user to further customize them based on their needs. Create a user-group representing the domain users and associate permission to this user group, to set up permissions at a domain level. For more information on managing permissions for Cloud Provisioning and Governance roles, see [Manage Cloud Permissions](../concept/cloud-permissions.md).

-   Configure and manage policies and manage lease for provisioned stack. A policy rule is a collection of conditions and actions. ​If all conditions evaluate to true, the policy engine performs the actions. If any condition evaluates to false, the policy engine does not perform the actions.

    Set up policies in global domain only when you want the policies to apply to all domains. You can customize Cloud Provisioning and Governance and set policies specific to a customer or a domain, if you don't want global policies to apply to a domain. Use the domain field in policy rule condition to target policy towards the particular domain, to enable customized policy enforcement. When global and domain policies co-exist, both policies are executed in the sequence of the order configured for each policy. In case the values set in the order columns are same, the sequence in which the policy is executed is undetermined. Ensure that policy actions are domain separated, that is all action rules are within a single domain, and do not depend on rules in other domains.

    For more information, see:

    -   [Policy governance in Cloud Provisioning and Governance](../concept/cloud-policy.md)
    -   [Configure a cloud policy rule](../task/configure-cloud-policy-rule.md)
    -   [Create an action for an 'on Lease end' policy](../task/create-action-on-lease-end.md)
    -   [Cloud policy example](../task/policy-walkthrough.md)
-   [Create a cloud catalog item](../task/create-cloud-catalog-item.md)

    Create a cloud catalog item for provisioning, based on a template and publish the catalog item to provide a service.

    You can create common or global catalogs items based on templates, at the SP domain, making it available for all domains you're managing. You can also create custom catalog items for each domain/company based on your requirements. A user with domain admin/cloud designer roles, can update or delete cloud scripts and cloud script templates belongs to domain and sub-domains. You cannot use common catalogs with different pool-filter for each domain. Create a custom catalog for each domain instead.

    Deployment, post-provisioning, and Day-2 operations are domain separated. For example, if a cloud portal user from a specific company orders a VM, the stack, the request, virtual machine, and all components in the stack are stored in its respective domain. Subsequent operations for a domain are also handled in same manner. You can generate a catalog item based on Terraform configuration management template, or use Azure Resource Manager and AWS CloudFormation templates.

-   [Create Cloud Templates](../task/create-cloud-template.md)

    Do not add sensitive and private information such as CIDR values, IP addresses, credentials, etc, to the template content, if setting up the catalog item as a global catalog item. The sensitive information could be exposed to other cloud admins.

    Create a cloud template and associate the template with a catalog item. Once you've created a template, you can reuse the template to create additional catalog items for the services you want to provision.

-   [Set capacity limits on user requests for resources](../../cloud-management-v2-setup/task/set-capacity-limits-cloud-mgt.md)

    Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.

-   [Create a cloud quota definition](../task/create-cloud-quota.md)

    You can set up separate quota definitions for each domain you're managing in an instance.

    You apply quotas to a resource, such as a virtual server, datacenter, or a generic cloud resource, and to users of a particular group. You can set a per-user limit, and a total limit for the group for the resource. A cloud quota definition specifies the limitations on a resource block. You can use templates or manually create different types of configurations for each quota definition.

-   [Using the IPAM integration](../concept/IPAM-integration.md)

    IP address management \(IPAM\) in Cloud Provisioning and Governance supports domain separation.

    If you use an IP address management \(IPAM\) tool such as Infoblox, you can manage cloud IP addresses, networks, and subnets in your cloud catalog offerings.

-   [Business hours scheduling](../../cloud-management-v2-user/concept/business-hours-scheduling.md)

    Set up business hour scheduling on all virtual machines in a stack. Business hour scheduling can be set up on stacks at the time of provisioning or on existing stacks. Schedules can be set for when a stack should be started, stopped, and/or deprovisioned by defining parameters such as business hours, holidays, long weekends.

    You map a schedule profile to an instance schedule. The schedule profile applies to all newly provisioned resources that use the profile. For example, a schedule profile can specify the days of the week and times of day when a stack should start and stop.

    **Note:** Global Business schedules apply to all domains. You cannot set up domain-specific schedules if an active global schedule exists.

-   [Create a schedule profile](../task/create-schedule-profile.md)

    To set up domain-specific lease schedules ensure that no global lease schedules exist. You can only create a domain-specific lease or schedule when no active global policies exist. While you can have multiple leases or schedules in draft state, only one lease or schedule can be active.


## Next Steps

For more information on provisioning cloud resources, and making Cloud Provisioning and Governance life-cycle operations available for each domain that you are managing in your instance for, see [Domain admin considerations](domain-admin-workflow.md).

