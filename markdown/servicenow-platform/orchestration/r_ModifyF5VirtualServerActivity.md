---
title: Modify F5 Virtual Server activity
description: The Modify F5 Virtual Server activity configures a virtual server assigned to an F5 load balancer pool with irules and a vlan.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [F5 Network Management activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Modify F5 Virtual Server activity

The Modify F5 Virtual Server activity configures a virtual server assigned to an F5 load balancer pool with irules and a vlan.

This activity was built using the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#). To access the activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Active Directory**.

## REST settings

-   **REST message**: F5 VIP Management
-   **REST function**: put

## Input variables

<table id="table_w5m_5dl_zt"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

The virtual server's name, such as `testVIP`.

</td></tr><tr><td>

F5IPAddress

</td><td>

IP address of the F5 console.

</td></tr><tr><td>

irules

</td><td>

The irules for the virtual server, such as `_sys_https_redirect`.-   **pool**: Name of the pool for the virtual server, such as `testPool`.
-   **persistent**: Persistent profile for the virtual server, such as `cookie`.

</td></tr><tr><td>

vlans

</td><td>

Vlans for the virtual server, such as `internal`.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|result|Success or failure.|
|status\_code|The HTTP status code.|
|output|The REST output.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully configured a virtual server assigned to an F5 load balancer pool.|
|Failure|Activity failed to configure a virtual server assigned to an F5 load balancer pool.|

**Parent Topic:**[F5 Network Management activity pack](../concept/c_OrchF5LoadBalancerActivities.md)

