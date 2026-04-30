---
title: Add F5 Virtual Server activity
description: The Add F5 Virtual Server activity adds a virtual server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Add F5 Virtual Server activity

The Add F5 Virtual Server activity adds a virtual server.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 POOL Membership Management
-   **REST function**: post

## Input variables

|Variable|Description|
|--------|-----------|
|name|The virtual server's name, such as `testVIP`.|
|description|Description of this virtual server.|
|ipProtocol|Protocol used for this virtual server, such as `tcp`.|
|destination|Virtual server IP address and port number, such as 192.168.4.20:80.|
|mask|Subnet mask for this virtual server, such as 255.255.255.255.|
|F5IPAddress|IP address of the F5 console.|
|sourceAddressTranslation|Source address translation mode.|

## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|status\_code|The HTTP status code.|
|error|The REST error.|
|output|The REST output.|

## Conditions

|Condition|Decription|
|---------|----------|
|Success|Acitivty successfully added a virtual server.|
|Failure|Activity failed to add a virtual server.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

