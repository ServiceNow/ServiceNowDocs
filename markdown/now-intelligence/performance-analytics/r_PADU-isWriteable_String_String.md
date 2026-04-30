---
title: PADomainUtils - isWriteable\(String table, String id\)
description: Evaluate if you can write to a specific record identified by table and sys\_id.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - isWriteable\(String table, String id\)

Evaluate if you can write to a specific record identified by table and sys\_id.

|Name|Type|Description|
|----|----|-----------|
|table|String|The name of the table containing the record to query, such as pa\_indicators.|
|id|String|The sys\_id of the record to query.|

|Type|Description|
|----|-----------|
|Boolean|Indicates that you can write to the specified record. Returns true if the record exists within the domain of the current user. Returns false if the record does not exist, or is in a different domain.|

```
var pa = new SNC.PADomainUtils();
pa.isWriteable('pa_incidents','cd8125b5140012007665a83e633b028d');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

