---
title: PADomainUtils - copy\(String runAs\)
description: Copies Performance Analytics records to a different domain.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - copy\(String runAs\)

Copies Performance Analytics records to a different domain.

To copy dashboards or scheduled jobs, see [copyDashboard](PADU-copyDashboard_S_S.md) and [copyJob](r_PADU-copyJob_String_String.md).

|Name|Type|Description|
|----|----|-----------|
|runAs|String|User whose domain you want to copy records to.|

|Type|Description|
|----|-----------|
|void| |

```
// copy all the Performance Analytics records from global to user's domain
var pa = new SNC.PADomainUtils();
pa.copy('09ff3d105f231000b12e3572f2b4775d');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

