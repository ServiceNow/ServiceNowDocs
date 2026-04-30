---
title: HostnameJS - Global
description: The HostnameJS script include provides methods to format host names according to property settings.Formats the specified host name according to the property settings.Returns the DNS domain name.Returns the current system name.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# HostnameJS- Global

The HostnameJS script include provides methods to format host names according to property settings.

Use with any server-side script when you need to format host names.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## HostnameJS - format\(String hostname, String source\)

Formats the specified host name according to the property settings.

|Name|Type|Description|
|----|----|-----------|
|hostname|String|The host name to format|
|source|String|The property settings source|

|Type|Description|
|----|-----------|
|String|The system name|

## HostnameJS - getDomainName\(\)

Returns the DNS domain name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The domain name|

```
var hjs = new HostnameJS();
hjs.getDomainName();
```

## HostnameJS - getSysName\(\)

Returns the current system name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The system name|

```
var hjs = new HostnameJS();
hjs.getSysName();
```

