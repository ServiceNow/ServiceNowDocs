---
title: Add F5 Pool Member activity
description: The Add F5 Pool Member activity adds a member to an F5 load balancer pool.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Add F5 Pool Member activity

The Add F5 Pool Member activity adds a member to an F5 load balancer pool.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Membership Management
-   **REST function**: post

## Input variables

|Variable|Description|
|--------|-----------|
|PoolName|Name of this pool, such as `testPool`.|
|F5IPAddress|IP address of the F5 console.|
|MemberName|Pool member IP address and port, such as 192.168.2.19:80.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|status\_code|The HTTP status code.|
|error|The REST error.|
|output|The REST output.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully added an F5 load balancer pool member.|
|Failure|Activity failed to add an F5 load balancer pool member.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

