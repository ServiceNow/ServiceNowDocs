---
title: Turn off next-hop route data collection for BGP routers
description: You can turn off Next Hop Routing Rule \[dscy\_route\_next\_hop\] table collection for BGP-enabled routers to reduce MID Server memory load during router discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/turn-off-bgp-next-hop-collection.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [BGP discovery, network router discovery, SNMP routing pattern, next-hop route data, MID Server performance]
breadcrumb: [Network router, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Turn off next-hop route data collection for BGP routers

You can turn off Next Hop Routing Rule \[dscy\_route\_next\_hop\] table collection for BGP-enabled routers to reduce MID Server memory load during router discovery.

## Before you begin

-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.
-   Navigate to `sys_properties.list` and verify that the **glide.discovery.bgp\_router\_disable** property is set to false.

Role required: discovery\_admin

## About this task

By default, the **glide.discovery.bgp\_router\_disable** property is set to true, blocking the entire BGP routing branch including interfaces and neighbors. Setting the property to false enables interface and neighbor collection but also triggers a full route-table walk. On routers with large route tables, this can cause MID Server memory and performance issues.

The **glide.discovery.disable\_next\_hop\_data** property controls route-table collection. When this property is set to true, Discovery collects the device, physical interfaces, and neighbors but skips populating the Next Hop Routing Rule \[dscy\_route\_next\_hop\] table. The default value is false.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `glide.discovery.disable_next_hop_data`.

3.  Select the **glide.discovery.disable\_next\_hop\_data** system property.

4.  In the **Value** field, enter `true`.

    To also collect next-hop route table data, set the value to `false`.

5.  Select **Update**.


## What to do next

Run Discovery again against a BGP-enabled router to apply the changes.

**Parent Topic:**[Network router discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/network-router-patterns.md)

**Related topics**  


[Network router discovery using patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/network-router-patterns.md)

