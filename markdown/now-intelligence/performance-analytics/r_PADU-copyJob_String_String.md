---
title: PADomainUtils - copyJob\(String paJob, String runAs\)
description: Copies a Performance Analytics scheduled data collection job record to another domain.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PADomainUtils - Global, Domain separation, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PADomainUtils - copyJob\(String paJob, String runAs\)

Copies a Performance Analytics scheduled data collection job record to another domain.

|Name|Type|Description|
|----|----|-----------|
|paJob|String|Sys\_id of a Performance Analytics scheduled data collection job \[sysauto\_pa\] record.|
|runAs|String|User whose domain you want to copy the job to.|

|Type|Description|
|----|-----------|
|String|Error message if an error occurs, or an empty string if there is no error.|

```
// No source domain needs to be set
var pa = new SNC.PADomainUtils();
// copy the '[PA Incident] Daily Data Collection job'
// set the 'run as' of the new record to be the 'acme.itil' user
// first argument is the sys_id of the sysauto_pa record
// the second is the sys_id of the acme.itil user record
pa.copyJob('82ba2023d7101100b96d45a3ce6103cd','797d14341f1310005a3637b8ec8b7010');
```

**Parent Topic:**[PADomainUtils - Global](../concept/c_PADomainUtils.md)

