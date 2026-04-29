---
title: MIDServerManage - Global
description: The MIDServerManage script include provides methods that allow you to manage a MID Server by sending messages to start, stop, upgrade, get logs, send test probes, and send system messages.Creates an instance of MIDServerManage.Gets the logs for the specified MID server.Restarts the specified MID server.Stops the specified MID server.Creates a system message for the specified MID server.Sends a test probe for the specified MID server.Upgrades the specified MID server.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerManage- Global

The MIDServerManage script include provides methods that allow you to manage a MID Server by sending messages to start, stop, upgrade, get logs, send test probes, and send system messages.

Use in server scripts to send messages to a MID Server.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerManage - MIDServerManage\(\)

Creates an instance of MIDServerManage.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## MIDServerManage - grab\_logs\(String agentName, String logs\)

Gets the logs for the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|
|logs|String|The type of log to get \(Optional\)|

|Type|Description|
|----|-----------|
|String|The log message|

```
var msm = new MIDServerManage();
msm.grab_logs('serv1');
```

Output: Background message, type:info, message: Grabbing MID Server Logs

## MIDServerManage - restart\(String agentName\)

Restarts the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|

|Type|Description|
|----|-----------|
|void| |

```
var msm = new MIDServerManage();
msm.restart('serv1');
```

## MIDServerManage - stop\(String agentName\)

Stops the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|

|Type|Description|
|----|-----------|
|void| |

```
var msm = new MIDServerManage();
msm.stop('serv1');
```

## MIDServerManage - system\_msg\(String agentName, String cmd, String name\)

Creates a system message for the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|
|cmd|String|The value of the probe source field|
|name|String|The name of the probe|

|Type|Description|
|----|-----------|
|void| |

```
var msm = new MIDServerManage();
msm.test_probe('mid.server.serv1', 'command', 'probe_id');
```

## MIDServerManage - text\_probe\(String agentName, String probeID, String topic, String ename, String source\)

Sends a test probe for the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|
|probeId|String|The ID of the probe to send|
|topic|String|The information for the topic field|
|ename|String|The name for the probe|
|source|String|The information for the source field|

|Type|Description|
|----|-----------|
|Object|The probe for the specified MID server|

```
var msm = new MIDServerManage();
msm.test_probe('mid.server.serv1', 'probe_id', 'topic text', 'name', 'source text');
```

## MIDServerManage - upgrade\(String agentName\)

Upgrades the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|agentName|String|The MID server name|

|Type|Description|
|----|-----------|
|void| |

```
var msm = new MIDServerManage();
msm.upgrade('serv1');
```

