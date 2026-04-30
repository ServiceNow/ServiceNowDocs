---
title: MonitorMIDServer - Global
description: The MonitorMIDServer script include provides methods to monitor MID Servers using the heartbeat probe to check for MID Servers that are down, sends heartbeat requests, and kills old heartbeat requests.Creates an instance of MonitorMIDServer.If there are any heartbeat probe requests that haven't been processed, cancels them so that they don't accumulate when a MID server is down for a while.Marks any non-responding MID servers as being down, by determining when the most recent heartbeat was sent and finding all non-responding servers.Performs the functions required for a scheduled MID server monitor cycle, including killing old requests, marking the MID servers that are down, and sending heartbeat requests to all servers.Sends heartbeat requests to all MID servers and notes when by updating the server status record.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MonitorMIDServer- Global

The MonitorMIDServer script include provides methods to monitor MID Servers using the heartbeat probe to check for MID Servers that are down, sends heartbeat requests, and kills old heartbeat requests.

Use this script include in a server script to monitor MID Servers.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MonitorMIDServer - MonitorMIDServer\(\)

Creates an instance of MonitorMIDServer.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## MonitorMIDServer - killOldRequests\(\)

If there are any heartbeat probe requests that haven't been processed, cancels them so that they don't accumulate when a MID server is down for a while.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mmsv = new MonitorMIDServer();
mmsv.killOldRequests();
```

## MonitorMIDServer - markDowners\(\)

Marks any non-responding MID servers as being down, by determining when the most recent heartbeat was sent and finding all non-responding servers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mmsv = new MonitorMIDServer();
mmsv.markDowners();
```

## MonitorMIDServer - monitor\(\)

Performs the functions required for a scheduled MID server monitor cycle, including killing old requests, marking the MID servers that are down, and sending heartbeat requests to all servers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mmsv = new MonitorMIDServer();
mmsv.monitor();
```

## MonitorMIDServer - sendHeartbeatRequests\(\)

Sends heartbeat requests to all MID servers and notes when by updating the server status record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var mmsv = new MonitorMIDServer();
mmsv.sendHeartbeatRequests();
```

