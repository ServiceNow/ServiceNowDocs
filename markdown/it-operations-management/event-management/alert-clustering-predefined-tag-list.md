---
title: List of predefined alert grouping tags
description: A list of the predefined alert clustering tags provided with the Tag Based Alert Clustering Engine  application.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# List of predefined alert grouping tags

A list of the predefined alert clustering tags provided with the Tag Based Alert Clustering Engine  application.

|Name|Source|Match method|
|----|------|------------|
|CI|em\_alert.cmdb\_ci|Exact match|
|Description|em\_alert.description|Exact match|
|Metric Name|em\_alert.metric\_name|Exact match|
|Node|em\_alert.node|Exact match|
|Resource|em\_alert.resource|Exact match|
|Source|em\_alert.source|Exact match|
|Source instance|em\_alert.event\_class|Exact match|
|Type|em\_alert.type|Exact match|
|Assignment group|em\_alert.assignment\_group|Exact match|
|CI Class|cmdb\_ci.sys\_class\_name|Exact match|
|Dns domain|cmdb\_ci.dns\_domain|Exact match|
|ip address|cmdb\_ci.ip\_address|Exact match|
|Location|cmdb\_ci.location|Exact match|
|Environment|cmdb\_ci.environment|Exact match|
|CI name|cmdb\_ci.name|Exact match|
|Namespace|cmdb\_ci.namespace|Exact match|

|Name|Description|Default mapping from CMDB|
|----|-----------|-------------------------|
|t\_ip\_address|IP address|cmdb\_ci.ip\_address|
|t\_application|Application|-|
|t\_region|Region|-|
|t\_location|Location|cmdb\_ci.location|
|t\_environment|Environment|cmdb\_ci.environment|
|t\_namespace|Namespace|cmdb\_ci.namespace|

**Parent Topic:**[Event Management reference](event-management-reference.md)

