---
title: Quotas and resource order controls
description: Quotas are limitations or requirements for groups and users on CIs or cloud resources. Use quotas to prevent wasteful resource usage in your cloud environment.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Quotas and resource order controls

Quotas are limitations or requirements for groups and users on CIs or cloud resources. Use quotas to prevent wasteful resource usage in your cloud environment.

You apply quotas to a resource, such as a virtual server, datacenter, or a generic cloud resource, and to users of a particular group. You can set a per-user limit, and a total limit for the group for the resource. For example, a quota might limit the number of virtual servers allowed for users in the **Database** group.

After this kind of quota is set, users who try to provision additional virtual servers will receive an error message and they will not be able to proceed with provisioning virtual servers until the resource count is under the quota limit. If a user belongs to more than one group, they receive the total quota limit from both groups combined.

**Note:** You can also set per-datacenter limitations on resources by using capacity limits in cloud accounts. See [Set capacity limits on user requests for resources](../../cloud-management-v2-setup/task/set-capacity-limits-cloud-mgt-1.md).

## Resource block types, quota types, and attributes

You can assign quotas to users or groups for the following resource block types:

-   Virtual Servers
-   Storage Volume Size
-   Network
-   Stacks

Quota types include:

-   **Sum**

    The sum of all attributes for a resource, such as the sum of all virtual CPUs.

-   **Count**

    The total number of attributes for a resource, such as the number of virtual machines.


