---
title: Add F5 Profile to Virtual Server activity
description: The Add F5 Profile to Virtual Server activity adds a profile to a virtual server assigned to an F5 load balancer pool.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, Creating integrations with applications]
---

# Add F5 Profile to Virtual Server activity

The Add F5 Profile to Virtual Server activity adds a profile to a virtual server assigned to an F5 load balancer pool.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 VIP Profile Management
-   **REST function**: post

## Input variables

|Variable|Description|
|--------|-----------|
|name|The virtual server's name, such as `testVIP`|
|F5IPAddress|IP address of the F5 console.|
|VirtualServerName|Name of the virtual server, such as `testVIP`.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|output|The REST output.|
|status\_code|The HTTP status code.|

## Condtions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully added the F5 load balancer profile to the virtual server.|
|Failure|Activity failed to add the F5 load balancer profile to the virtual server.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

