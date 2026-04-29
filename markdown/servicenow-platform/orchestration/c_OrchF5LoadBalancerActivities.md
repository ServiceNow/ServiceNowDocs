---
title: F5 Network Management activity pack
description: Orchestration provides custom activities for configuring elements of an F5 load balancer, including pools, pool members, and the virtual servers contained in the pool.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# F5 Network Management activity pack

Orchestration provides custom activities for configuring elements of an F5 load balancer, including pools, pool members, and the virtual servers contained in the pool.

All F5 custom activities are in the F5 Network Management Application [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US) and are activated by the Orchestration - F5 network management plugin, which must be [activated by request](../task/t_ActivateAnActivityPack.md).

ServiceNow provides custom F5 activities, built from the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#), that you can use to perform the following tasks:

-   Add, delete, or verify pools.
-   Add, delete, or identify pool members.
-   Add or delete virtual servers.
-   Add a profile to a virtual server.
-   Configure the virtual server for vlans, irules, pool, and persistence.

-   **[Add F5 Pool Member activity](../reference/r_AddF5PoolMemberActivity.md)**  
The Add F5 Pool Member activity adds a member to an F5 load balancer pool.
-   **[Get F5 Pool Member activity](../reference/r_GetF5PoolMemberActivity.md)**  
The Get F5 Pool Member activity returns the pool members and verifies the pool's status.
-   **[Delete F5 Virtual Server activity](../reference/r_DeleteF5VirtualServerActivity.md)**  
The Delete F5 Virtual Server activity deletes a virtual server from an F5 load balancer pool.
-   **[Check F5 Pool activity](../reference/r_CheckF5PoolActivity.md)**  
The Check F5 Pool activity checks the status of a pool to determine if it is available to accept traffic.
-   **[Add F5 Profile to Virtual Server activity](../reference/r_AddF5ProfileToVirtualServerActivity.md)**  
The Add F5 Profile to Virtual Server activity adds a profile to a virtual server assigned to an F5 load balancer pool.
-   **[Modify F5 Virtual Server activity](../reference/r_ModifyF5VirtualServerActivity.md)**  
The Modify F5 Virtual Server activity configures a virtual server assigned to an F5 load balancer pool with irules and a vlan.
-   **[Add F5 Virtual Server activity](../reference/r_AddF5VirtualServerActivity.md)**  
The Add F5 Virtual Server activity adds a virtual server.
-   **[Delete F5 Pool Member activity](../reference/r_DeleteF5PoolMemberActivity.md)**  
The Delete F5 Pool Member activity deletes an F5 load balancer pool member.
-   **[Delete F5 Pool activity](../reference/r_DeleteF5PoolActivity.md)**  
The Delete F5 Pool activity deletes an F5 load balancer pool.
-   **[Add F5 Pool activity](../reference/r_AddF5PoolActivity.md)**  
The Add F5 Pool activity creates the F5 load balancer pool.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

