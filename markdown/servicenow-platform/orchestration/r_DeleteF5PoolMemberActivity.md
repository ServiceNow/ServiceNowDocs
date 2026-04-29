---
title: Delete F5 Pool Member activity
description: The Delete F5 Pool Member activity deletes an F5 load balancer pool member.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete F5 Pool Member activity

The Delete F5 Pool Member activity deletes an F5 load balancer pool member.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Membership Management
-   **REST function**: delete

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

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Acivity succeeded in deleting an F5 load balancer pool member.|
|Failure|Acivity failed to delete an F5 load balancer pool member.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

