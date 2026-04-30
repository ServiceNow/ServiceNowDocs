---
title: PADomainUtils - setOverrides\(Boolean overrides\)
description: Use this method before copying records to set the sys\_override value of the new record to the original parent record.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - setOverrides\(Boolean overrides\)

Use this method before copying records to set the sys\_override value of the new record to the original parent record.

Using this method enables you to automatically override records in a parent domain. By overriding the parent records, the parent records do not impact the child domain. If the source domain is not the parent of the target domain when copying records, setting the sys\_override value will not have any impact on behavior. You can specify an override only when copying records, not when moving records.

|Name|Type|Description|
|----|----|-----------|
|overrides|Boolean|Indicates that copied records in a child domain should override the source record in the parent domain. This value is true by default.|

|Type|Description|
|----|-----------|
|PADomainUtils|The object calling this function.|

```
var pa = new SNC.PADomainUtils('c90d4b084a362312013398f051272c0d');
pa.setOverrides(false);
pa.copy('bb6b58b01f1310005a3637b8ec8b70dd');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

