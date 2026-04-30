---
title: MIDServerFileSync - Global
description: The MIDServerFileSync script include provides methods to check to see if there are any changes to attachments on tables that are instances of MID Server synchronized files \(ecc\_agent\_sync\_file\) and, if so, notifies the MID Servers of a change.Creates an instance of MIDServerFileSync.Checks for any changes to attachments on the specified table that are instances of MID server synchronized files and, if so, notifies the MID servers of a change.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerFileSync- Global

The MIDServerFileSync script include provides methods to check to see if there are any changes to attachments on tables that are instances of MID Server synchronized files \(ecc\_agent\_sync\_file\) and, if so, notifies the MID Servers of a change.

The tables that extend the sync tables are MID Server JAR file \(ecc\_agent\_jar\) and MID Server MIB File \(ecc\_agent\_mib\).

Use in server scripts to notify MID Servers.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerFileSync - MIDServerFileSync\(\)

Creates an instance of MIDServerFileSync.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## MIDServerFileSync - notifyMIDServers\(String table\)

Checks for any changes to attachments on the specified table that are instances of MID server synchronized files and, if so, notifies the MID servers of a change.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table to check|

|Type|Description|
|----|-----------|
|void| |

```
var msfs = new MIDServerFileSync();
msfs.notifyMIDServers('ex.table.name');
```

