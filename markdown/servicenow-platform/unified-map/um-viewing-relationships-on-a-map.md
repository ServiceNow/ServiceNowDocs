---
title: Viewing relationships on a map
description: Both mapped service instances and CIs in the cmdb\_ci table appear on maps with related nodes and edges. In addition, the Service instances panel lists Service Mapping details for all associated service instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/unified-map/um-viewing-relationships-on-a-map.html
release: brazil
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing relationships on a map

Both mapped service instances and CIs in the cmdb\_ci table appear on maps with related nodes and edges. In addition, the **Service instances** panel lists Service Mapping details for all associated service instances.

## Viewing mapped service instances

Service instances that are populated using Service Mapping methods are included in maps. Service Mapping provides significant information for mapped service instances \(application services\) \[cmdb\_ci\_service\_discovered\] such as relationships and grouping. If Service Mapping is installed and the **sn\_sm\_scoped\_app.sa.unified\_map.enabled** system property is enabled, you can access Unified Map from the Service Mapping workspace. For more information, see [Access the Unified Map feature from the Service Mapping Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/view-unified-map-sm-workspace.md).

For a selected CI, the **Service instances** panel in Unified Map lists details from the Service Mapping application for all associated service instances \(formerly application services\). For more information, see [View service instances on Unified Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/unified-map/unified-map-show-app-service.md).

If Service Mapping is not installed, only service instances that are populated by CMDB methods appear on maps. Unified Map traverses the CMDB hierarchical data both up and down using user-specified levels.

## Viewing relationships for a CI in the cmdb\_ci table

Even though CIs in the cmdb\_ci table don't appear in Service Mapping data, CMDB CIs relationships appear on the map. For more information, see [View cmdb\_ci relationships in Unified Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/unified-map/u-map-show-rltships-for-cmdb-ci-cis.md)

**Related topics**  


[Configuring Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/service-mapping-setup.md)

