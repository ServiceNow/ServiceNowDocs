---
title: PADomainUtils - setFoundation\(Boolean foundation\)
description: Use this method to move or copy only foundational records in a hybrid domain configuration.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - setFoundation\(Boolean foundation\)

Use this method to move or copy only foundational records in a hybrid domain configuration.

You can implement a hybrid approach by maintaining some types of record in a parent domain and some types in child domains. Generally, the parent domain contains foundational records and the child domain contains higher-level records, such as widgets. The following types of record are considered foundational records.

-   Bucket groups
-   Buckets
-   Scripts
-   Breakdown sources
-   Indicator sources
-   Filters
-   Breakdowns
-   Managed sources
-   Manual breakdowns
-   Breakdown mappings
-   Breakdown relations

Other Performance Analytics records such as widgets and indicators are not foundational records. Set this method to false to move or copy these additional records as well.

|Name|Type|Description|
|----|----|-----------|
|foundation|Boolean|Indicates if only foundational records should be copied or moved by this PADomainUtils object.|

|Type|Description|
|----|-----------|
|PADomainUtils|The object calling this function.|

```
var pa = new SNC.PADomainUtils().setFoundation(true);
pa.copy('bb6b58b01f1310005a3637b8ec8b70dd');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

