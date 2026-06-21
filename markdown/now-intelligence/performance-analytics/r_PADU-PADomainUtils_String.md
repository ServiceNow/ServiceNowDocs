---
title: PADomainUtils - PADomainUtils\(String domainFrom\)
description: Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the specified domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/now-intelligence/performance-analytics/r\_PADU-PADomainUtils\_String.html
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation and Performance Analytics, Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - PADomainUtils\(String domainFrom\)

Instantiates a new PADomainUtils object to move or copy Performance Analytics records from the specified domain.

Use the PADomainUtils\(\) constructor instead when moving or copying from the global domain.

|Name|Type|Description|
|----|----|-----------|
|domainFrom|String|The domain to copy records from.|

```
// c90d4b084a362312013398f051272c0d is the sys id of the ACME domain
var acmeUtils = new SNC.PADomainUtils('c90d4b084a362312013398f051272c0d');
```

**Parent Topic:**[PADomainUtils - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/now-intelligence/performance-analytics/c_PADomainUtils.md)

