---
title: MIDServerSelector - Global
description: The MIDServerSelector script include provides methods to find a MID Server based on capabilities and target IP address.Creates an instance of MIDServerSelector.Finds the MID server based on the capabilities and target IP address.Gets the error messages for the current MID server.Gets the warning messages for the current MID server.Sets the technologies for which to look.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerSelector- Global

The MIDServerSelector script include provides methods to find a MID Server based on capabilities and target IP address.

Use in server scripts to find a MID Server with specific capabilities.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerSelector - MIDServerSelector\(\)

Creates an instance of MIDServerSelector.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## MIDServerSelector - findAgent\(String target\)

Finds the MID server based on the capabilities and target IP address.

|Name|Type|Description|
|----|----|-----------|
|target|String|The target IP address|

|Type|Description|
|----|-----------|
|void| |

```
var mss = new MIDServerSelector();
var capab = ["ssh","wmi","snmp"];
mss.setCapabilities(capab);
mss.findAgent('100.101.10.10');
```

## MIDServerSelector - getError\(\)

Gets the error messages for the current MID server.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mss = new MIDServerSelector();
var capab = ["ssh","wmi","snmp"];
mss.setCapabilities(capab);
mss.findAgent('100.101.10.10');
mss.getError();
```

## MIDServerSelector - getWarning\(\)

Gets the warning messages for the current MID server.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mss = new MIDServerSelector();
var capab = ["ssh","wmi","snmp"];
mss.setCapabilities(capab);
mss.findAgent('100.101.10.10');
mss.getWarning();
```

## MIDServerSelector - setCapabilities\(Array capabilities\)

Sets the technologies for which to look.

|Name|Type|Description|
|----|----|-----------|
|capabilities|Array|A list of capabilities, for example - capabilities = \["ssh","wmi","snmp",\{"os\_domain":"disco"\},\{"phase":1\}\];|

|Type|Description|
|----|-----------|
|void| |

```
var mss = new MIDServerSelector();
var capab = ["ssh","wmi","snmp"];
mss.setCapabilities(capab);
```

