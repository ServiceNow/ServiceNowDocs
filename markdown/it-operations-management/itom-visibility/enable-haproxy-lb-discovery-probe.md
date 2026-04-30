---
title: Enable HAProxy load balancer discovery with probes
description: If you prefer not to start using the default HAProxy pattern-based discovery, enable probe-based HAProxy discovery to continue using it instead.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HAProxy using probes, Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Enable HAProxy load balancer discovery with probes

If you prefer not to start using the default HAProxy pattern-based discovery, enable probe-based HAProxy discovery to continue using it instead.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **Processes**.

2.  In the **Name** field, search for `HAProxy`.

3.  Select the HAProxy classifier.

4.  In the **Triggers probe** related list, select **Edit**.

5.  Remove **Horizontal Pattern** from the Triggers probes List.

6.  From the Collection list, add **HAProxy - Get Configuration** and **HAProxy - Version** to the Triggers probe list.

7.  Select **Save**.


## What to do next

Schedule a horizontal discovery to discover HAProxy load balancer with probes. For more information, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#).

**Related topics**  


[HAProxy load balancer discovery using probes](../concept/c_LoadBalancerHAProxy.md)

