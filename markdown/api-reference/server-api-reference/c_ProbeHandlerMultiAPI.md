---
title: ProbeHandlerMulti - Global
description: The ProbeHandlerMulti script include is a probe handler for multiprobes.Adds the probe parameters to the given XML parent element, taken from the given probe's parameter table.Adds the probes for this multiprobe to the document.Runs the probe.If the given probe's GlideRecord is present and contains a probe handler, runs the probe handler and adds any parameters it creates to the given parameter element.Sets the value of a given XML parameter element.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProbeHandlerMulti- Global

The ProbeHandlerMulti script include is a probe handler for multiprobes.

This script include does not work with probe parameters that have value\_scripts and does not work with JavaScript probes.

You can use this script include in any server-side script where you need to configure a multiprobe.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProbeHandlerMulti - addParameters\(String parent, String sysID, GlideRecord probe\)

Adds the probe parameters to the given XML parent element, taken from the given probe's parameter table.

|Name|Type|Description|
|----|----|-----------|
|parent|String|The XML parent element to add parameters to.|
|sysID|String|The sys\_id of the probe to get parameters from.|
|probe|GlideRecord|Optional GlideRecord of the probe. If present, and there is a probe handler, it is called.|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerMulti - addProbes\(String parent, String sysID\)

Adds the probes for this multiprobe to the document.

|Name|Type|Description|
|----|----|-----------|
|parent|String|The XML parent element to add the probes to.|
|sysID|String|The sys\_id of the multi-probe|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerMulti - run\(\)

Runs the probe.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerMulti - runProbeHandler\(String params, String sysID, GlideRecord probe\)

If the given probe's GlideRecord is present and contains a probe handler, runs the probe handler and adds any parameters it creates to the given parameter element.

|Name|Type|Description|
|----|----|-----------|
|params|String|The XML parameter element to add parameters to.|
|sysID|String|The sys\_id of the probe to get parameters from.|
|probe|GlideRecord|Optional GlideRecord of the probe. If present, and there is a probe handler, it is called.|

|Type|Description|
|----|-----------|
|void| |

## ProbeHandlerMulti - setParameter\(String parent, String name, String value\)

Sets the value of a given XML parameter element.

|Name|Type|Description|
|----|----|-----------|
|parent|String|The XML parent element to add the parameter to.|
|name|String|The name of the parameter to set|
|value|String|The value to set the parameter to.|

|Type|Description|
|----|-----------|
|void| |

