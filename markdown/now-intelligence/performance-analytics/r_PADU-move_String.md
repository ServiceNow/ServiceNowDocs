---
title: PADomainUtils - move\(String runAs\)
description: Moves Performance Analytics records to a different domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/performance-analytics/r\_PADU-move\_String.html
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - move\(String runAs\)

Moves Performance Analytics records to a different domain.

|Name|Type|Description|
|----|----|-----------|
|runAs|String|The user whose domain you want to copy records to.|

|Type|Description|
|----|-----------|
|void| |

```
// move all the Performance Analytics records from the global to the customers domain
var pa = new SNC.PADomainUtils();
pa.move('774190f01f1310005a3637b8ec8b70ef')
```

**Parent Topic:**[PADomainUtils - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/performance-analytics/c_PADomainUtils.md)

