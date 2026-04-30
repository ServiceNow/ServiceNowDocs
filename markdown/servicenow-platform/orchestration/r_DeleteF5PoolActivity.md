---
title: Delete F5 Pool activity
description: The Delete F5 Pool activity deletes an F5 load balancer pool.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete F5 Pool activity

The Delete F5 Pool activity deletes an F5 load balancer pool.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Management
-   **REST function**: delete

## Input variables

|Variable|Description|
|--------|-----------|
|F5IPAddress|IP address of the F5 console.|
|PoolName|Name of this pool, such as `testPool`.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|error|The REST error.|
|status\_code|The HTTP status code.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully deleted the F5 load balancer pool.|
|Failure|Activity failed to delete the F5 load balancer pool.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

