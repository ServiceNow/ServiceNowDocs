---
title: Additional Cloud Provisioning and Governance setup on day 2
description: After you have performed Day 1 setup, you can perform optional setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Additional Cloud Provisioning and Governance setup on day 2

After you have performed Day 1 setup, you can perform optional setup and configuration procedures as needed and in any order. Detailed instructions for each procedure follow this overview.

## Additional setup and configuration operations

Detailed instructions for each procedure follow this overview.

-   **Set up an additional cloud account**

    A cloud account is the logical representation in Cloud Provisioning and Governance of all or part of your managed cloud infrastructure. A cloud account can include multiple service accounts — even service accounts from different providers. For each service account, you specify which datacenters to include in the cloud account.

-   **Schedule discovery of all resources in a service account**

    Add a custom schedule for Discovery to discover all resources in each datacenter in a service account and then update the CMDB with the new information.

    You can use the discovery schedules as offered on the cloud discovery schedule page.

    **Note:**

    Starting Xanadu release, any new user will run Pattern-based discovery, by default. In scenarios where the latest patterns application is not installed, discovery fails and the System Admin is prompted to install or migrate from CAPI-based discovery.

    Installing Cloud Discovery Workspace triggers automatic installation of the latest patterns application.

    For more information, see [Migrate from CAPI to Patterns](../../discovery/task/migrate-from-capi-to-pattern.md).

-   **Discover all resources in a datacenter on-demand**

    At any time, you can run Discovery on a datacenter to update the CMDB.

-   **Set capacity limits on user requests for resources**

    Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.


## Next steps

When you have finished all Day-1 and Day-2 procedures in this setup guide, see the [Cloud Provisioning and Governance administration guide](../../cloud-management-v2/concept/cloud-configuration.md) for information on using the Cloud Provisioning and Governance application in your organization.

-   **[Set up an additional cloud account](../task/add-cloud-account-cloud-mgt.md)**  
 During initial installation, you set up one cloud account. To organize and compartmentalize your infrastructure, you can set up additional cloud accounts to include different providers or service accounts or datacenters.
-   **[Discover using Cloud Operations Workspace and Patterns](../task/discover-with-cloud-discovery-workspace-and-patterns.md)**  
You can now schedule and perform discovery using Cloud Discovery Workspace and Discovery and Service Mapping Patterns.
-   **[Discover all datacenters in a service account on-demand](../task/disco-datacntrs-in-srv-acct.md)**  
After you set up a service account, run Discovery to populate the datacenters in the account.
-   **[Schedule discovery of all resources in a service account](../task/sched-uni-disco-srvacct-cloudmgt.md)**  
Add a custom schedule for Discovery to discover all resources in each datacenter in a service account and then update the CMDB with the new information.
-   **[Discover all resources in a datacenter on-demand](../task/disco-resources-in-datacenter.md)**  
At any time, you can run Discovery on a datacenter to update the CMDB.
-   **[Set capacity limits on user requests for resources](../task/set-capacity-limits-cloud-mgt.md)**  
Capacity limits place restrictions on the attributes of cloud resources such as the number of virtual machines, virtual CPUs, or aggregate storage. You can set limits on resources separately for each logical datacenter in a cloud account.
-   **[Use owner and assignment groups](use-owner-and-assignment-groups.md)**  
You must set up and use the user groups in Cloud Provisioning and Governance as a part of the day-2 task.

**Parent Topic:**[Cloud Provisioning and Governance](../../cloud-management-v2/concept/cloud-management-v2-landing-page.md)

