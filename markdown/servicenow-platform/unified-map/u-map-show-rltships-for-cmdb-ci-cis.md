---
title: View cmdb\_ci relationships in Unified Map
description: Even though CIs in the cmdb\_ci table don't appear in Service Mapping data, CMDB CIs relationships appear on the map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/unified-map/u-map-show-rltships-for-cmdb-ci-cis.html
release: brazil
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Viewing relationships, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View cmdb\_ci relationships in Unified Map

Even though CIs in the cmdb\_ci table don't appear in Service Mapping data, CMDB CIs relationships appear on the map.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

The **unified\_map\_exclude\_class\_service\_map** property in the **sn\_cmdb\_ws\_config\_property** table specifies the CMDB CI classes that display relationships on maps:

-   Dynamic CI Group \[cmdb\_ci\_query\_based\_service\]
-   Connection Service Instance \[cmdb\_ci\_connection\_service\_instance\]
-   Data Service Instance \[cmdb\_ci\_data\_service\_instance\]
-   Facility Service Instance \[cmdb\_ci\_facility\_service\_instance\]
-   Network Service Instance \[cmdb\_ci\_network\_service\_instance\]
-   Network Function \[cmdb\_ci\_network\_function\_instance\]
-   Operational Process Service Instance \[cmdb\_ci\_operational\_process\_service\_instance\]
-   OT System Service \[cmdb\_ci\_ot\_system\_service\]

## Procedure

1.  Specify any CI that is in the cmdb\_ci table as the home node.

    The map displays the CI and its related CIs.

    \[Omitted image "um-cmdb\_ci-relationships.png"\] Alt text: Service instances for the selected CI.


