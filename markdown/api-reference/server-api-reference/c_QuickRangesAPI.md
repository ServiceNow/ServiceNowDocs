---
title: QuickRanges - Global
description: The QuickRanges script include provides methods to generate IP network, range, and address entries from a convenient comma-separated input field using conventional Classless Inter-Domain Range \(CIDR\) network notation, hyphenated range entries, or individual IP addresses.Creates a new discovery range item.Returns the IP network, range, and address information to use when generating the entries.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# QuickRanges- Global

The QuickRanges script include provides methods to generate IP network, range, and address entries from a convenient comma-separated input field using conventional Classless Inter-Domain Range \(CIDR\) network notation, hyphenated range entries, or individual IP addresses.

You can use this script include with any server-side discovery script.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## QuickRanges - createItem\(String table, String id, String type\)

Creates a new discovery range item.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table where the item will be created.|
|id|String|The identifier to use for the new item.|
|type|String|The type of entries to generate: IP address, IP network, or IP range.|

|Type|Description|
|----|-----------|
|GlideRecord|The created entry|

## QuickRanges - onMakeRanges\(\)

Returns the IP network, range, and address information to use when generating the entries.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

