---
title: MIDServerCluster - Global
description: The MIDServerCluster script include provides methods to find MID Server clusters for a given MID Server and reassigns the jobs if necessary.Brief description of the method.Determines if a cluster exists.Gets the cluster agent.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerCluster- Global

The MIDServerCluster script include provides methods to find MID Server clusters for a given MID Server and reassigns the jobs if necessary.

If the MID Server agent is up, this class gathers all MID Servers \(including the original agent\) in the load balance clusters that the original agent is part of. If the MID Server agent is down and the cluster is load balanced, the class gathers the other agents. If the server agent is down, and the cluster is failover, it gathers the next failover agent. The class then randomly returns the MID Server in the final list of MID Servers.

Use in server scripts to get MID Server cluster information.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerCluster - MIDServerCluster\(GlideRecord agent\)

Brief description of the method.

|Name|Type|Description|
|----|----|-----------|
|agent|GlideRecord|The MID server agent|

|Type|Description|
|----|-----------|
|void| |

## MIDServerCluster - clusterExists\(\)

Determines if a cluster exists.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if a cluster exists; otherwise, false.|

```
var midgr = new GlideRecord("ecc_agent");
midgr.addQuery("name", "al1winmid");
midgr.query();
midgr.next();
 
var mscl = new MIDServerCluster(midgr);
gs.print(mscl.clusterExists());
```

Output: true

## MIDServerCluster - getClusterAgent\(\)

Gets the cluster agent.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The agent name|

```
// Assuming "mid1" and "mid2" are in a cluster
var midgr = new GlideRecord("ecc_agent");
midgr.addQuery("name", "mid1");
midgr.query();
midgr.next();
 
var mscl = new MIDServerCluster(midgr);
gs.print(mscl.getClusterAgent());
```

Output: mid2

