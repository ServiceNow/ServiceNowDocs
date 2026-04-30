---
title: PADomainUtils - copyDashboard\(String dashboardId, String runAs\)
description: Copy a dashboard to another domain.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - copyDashboard\(String dashboardId, String runAs\)

Copy a dashboard to another domain.

|Name|Type|Description|
|----|----|-----------|
|dashboardId|String|Sys\_id of the dashboard to copy.|
|runAs|String|User whose domain you want to copy the dashboard to.|

|Type|Description|
|----|-----------|
|void| |

```
//Copy Incident Management dashboard from global to user's domain
var pa = new SNC.PADomainUtils();
pa.copyDashboard('a64b7031d7201100b96d45a3ce610335','09ff3d105f231000b12e3572f2b4775d');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

