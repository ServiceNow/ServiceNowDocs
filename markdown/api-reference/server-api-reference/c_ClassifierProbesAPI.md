---
title: ClassifierProbes - Global
description: The ClassifierProbes script include provides a classifier probe launch facility. Encapsulates an array of probe information records, initialized either from a JavaScript array or the XML serialized version.Launches the next highest priority classifier from those in the list.Launches a supplementary probe.Returns the probe length.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClassifierProbes- Global

The ClassifierProbes script include provides a classifier probe launch facility. Encapsulates an array of probe information records, initialized either from a JavaScript array or the XML serialized version.

Use in any server-side script where you need to define a classifier probe launch facility.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClassifierProbes - launch\(\)

Launches the next highest priority classifier from those in the list.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if a classifier is launched; otherwise, false.|

## ClassifierProbes - launchSupplementary\(\)

Launches a supplementary probe.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ClassifierProbes - size\(\)

Returns the probe length.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The probe length|

