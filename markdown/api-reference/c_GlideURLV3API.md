---
title: GlideURLV3 - Client
description: The GlideURLV3 API provides methods for manipulating a URI.Creates an instance of the GlideURL class.Adds a query string name-value pair to the URL.Get the entire context path and query string parameters as a single URI.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideURLV3- Client

The GlideURLV3 API provides methods for manipulating a URI.

You can only use this API in client-side scripts using ListV2 and ListV3 APIs.

**Note:** This API is not supported by Service Portal, Now Mobile, or Agent Workspace.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideURLV3 - GlideURL\(String contextPath\)

Creates an instance of the GlideURL class.

|Name|Type|Description|
|----|----|-----------|
|contextPath|String|A relative path for the URL.|

## GlideURLV3 - addParam\(String name, String value\)

Adds a query string name-value pair to the URL.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the query string parameter.|
|value|String|Query string value.|

|Type|Description|
|----|-----------|
|String|The GlideURL|

```
var gu = new GlideURL('incident.do');
var url = gu.addParam('sys_id', '-1');

```

## GlideURLV3 - getURL\(Object additionalParams\)

Get the entire context path and query string parameters as a single URI.

|Name|Type|Description|
|----|----|-----------|
|additionalParams|Object|A name-value pair object that contains parameters that are added to this URL request only. These additional parameters are not saved to the GlideURL object.|

|Type|Description|
|----|-----------|
|String|The GlideURL with the specified additional parameters added to the end.|

