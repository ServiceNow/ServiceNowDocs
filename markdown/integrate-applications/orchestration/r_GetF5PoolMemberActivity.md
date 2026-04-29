---
title: Get F5 Pool Member activity
description: The Get F5 Pool Member activity returns the pool members and verifies the pool's status.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Get F5 Pool Member activity

The Get F5 Pool Member activity returns the pool members and verifies the pool's status.

Use this activity to verify that a pool member was created properly.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Membership Management
-   **REST function**: get

## Input variables

|Variable|Description|
|--------|-----------|
|PoolName|Name of this pool, such as `testPool`.|
|F5IPAddress|IP address of the F5 console.|

## Output variables

|Variable|Description|
|--------|-----------|
|MembersArray|Array for the returned pool member IP address and port, such as 192.168.2.19:80.|
|status\_code|The HTTP status code.|
|error|The REST error.|
|result|Success or failure.|
|output|The REST output.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully returned the F5 load balancer pool members.|
|Failure|Activity failed to return the F5 load balancer pool members|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

