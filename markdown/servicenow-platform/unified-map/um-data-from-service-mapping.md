---
title: Service Mapping data that appears on maps
description: Service instances that are populated using Service Mapping methods are included in maps. Service Mapping provides significant information for mapped service instances \(application services\) \[cmdb\_ci\_service\_discovered\] such as relationships and grouping.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View service instances, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Mapping data that appears on maps

Service instances that are populated using Service Mapping methods are included in maps. Service Mapping provides significant information for mapped service instances \(application services\) \[cmdb\_ci\_service\_discovered\] such as relationships and grouping.

## Considerations

If Service Mapping is installed and the **sn\_sm\_scoped\_app.sa.unified\_map.enabled** system property is enabled, you can access Unified Map from the Service Mapping workspace. For more information, see [Access the Unified Map feature from the Service Mapping Workspace](https://www.servicenow.com/docs/access?context=view-unified-map-sm-workspace&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

If Service Mapping is not installed, only service instances that are populated by CMDB methods appear on maps. Unified Map traverses the CMDB hierarchical data both up and down using user-specified levels.

**Related topics**  


[Configuring Service Mapping](https://www.servicenow.com/docs/access?context=service-mapping-setup&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

