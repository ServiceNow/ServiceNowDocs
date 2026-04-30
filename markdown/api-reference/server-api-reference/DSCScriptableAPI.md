---
title: DSCScriptableAPI - Global
description: The DSCScriptableAPI provides methods for checking the health of your domain configuration for an instance.Instantiates a new DSCScriptable object.Checks a list of comma-separated tables for invalid domains.Checks a list of comma-separated tables for invalid domain paths.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DSCScriptableAPI- Global

The DSCScriptableAPI provides methods for checking the health of your domain configuration for an instance.

This API is part of the Domain Separation Center dashboard and is available in the `SNC` global namespace.

The com.glide.domain.msp\_extensions.installer plugin must be activated for Domain Separation Center dashboard availability.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DSCScriptableAPI - DSCScriptableAPI\(\)

Instantiates a new DSCScriptable object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## DSCScriptableAPI - chkDataInvalidDomainForTables\(String tableNames\)

Checks a list of comma-separated tables for invalid domains.

View records that reference invalid domains in the Domain Log \[syslog\_domain\] table.

|Name|Type|Description|
|----|----|-----------|
|tableNames|String|Comma-separated list of table names.|

|Type|Description|
|----|-----------|
|String|GUID of any invalid references; OK otherwise|

```
var dsc = new SNC.DSCScriptableAPI();
dsc.chkDataInvalidDomainForTables('task, sys_user');
```

## DSCScriptableAPI - chkDataInvalidPathForTables\(String tableNames\)

Checks a list of comma-separated tables for invalid domain paths.

Records that have an invalid domain path are logged in the syslog\_domain table.

|Name|Type|Description|
|----|----|-----------|
|tableNames|String|Comma-separated list of table names.|

|Type|Description|
|----|-----------|
|String|GUID if there are invalid paths; OK otherwise|

```
var dsc = new SNC.DSCScriptableAPI();
dsc.chkDataInvalidPathForTables('task, sys_user');
```

