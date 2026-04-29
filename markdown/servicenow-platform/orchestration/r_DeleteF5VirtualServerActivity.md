---
title: Delete F5 Virtual Server activity
description: The Delete F5 Virtual Server activity deletes a virtual server from an F5 load balancer pool.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete F5 Virtual Server activity

The Delete F5 Virtual Server activity deletes a virtual server from an F5 load balancer pool.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 VIP Management
-   **REST function**: delete

## Input variables

|Variable|Description|
|--------|-----------|
|F5IPAddress|IP address of the F5 console.|
|name|The virtual server's name, such as `testVIP`.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|status\_code|The HTTP status code.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully deleted the virtual server from the F5 load balancer pool.|
|Failure|Activity failed to delete the virtual server from the F5 load balancer pool.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

