---
title: Check F5 Pool activity
description: The Check F5 Pool activity checks the status of a pool to determine if it is available to accept traffic.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Check F5 Pool activity

The Check F5 Pool activity checks the status of a pool to determine if it is available to accept traffic.

Use this activity to determine if a pool you just created is up and running with the proper configuration.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Management
-   **REST function**: get

## Input variables

|Variable|Description|
|--------|-----------|
|F5IPAddress|IP address of the F5 console.|
|PoolName|Name of this pool, such as `testPool`.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|status\_code|The HTTP status code.|
|error|The REST error.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully returned the status of the F5 load balancer pool.|
|Failure|Activity failed to return the status of the F5 load balancer pool.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

