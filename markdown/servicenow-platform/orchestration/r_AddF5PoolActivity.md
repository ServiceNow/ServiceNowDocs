---
title: Add F5 Pool activity
description: The Add F5 Pool activity creates the F5 load balancer pool.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add F5 Pool activity

The Add F5 Pool activity creates the F5 load balancer pool.

Use this activity to verify that a pool member was created properly.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Management
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
|Success|Activity succeeded in creating the F5 load balancer pool.|
|Failure|Activity failed to create the F5 load balancer pool.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

