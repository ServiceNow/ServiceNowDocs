---
title: MIDServerAjax - Global
description: The MIDServerAjax script include provides AJAX functionality for sending a test probe to a MID ServerCreates an instance of MIDServerAjax.Sends a test probe to the MID server.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerAjax- Global

The MIDServerAjax script include provides AJAX functionality for sending a test probe to a MID Server

Use in server scripts to test a MID Server using AJAX.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerAjax - MIDServerAjax\(\)

Creates an instance of MIDServerAjax.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## MIDServerAjax - ajaxFunction\_testProbe\(\)

Sends a test probe to the MID server.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Contains the agent name, test probe ID, topic, name, and source.|

```
var msaj = new MIDServerAjax();
msaj.ajaxFunction_testProbe();
```

