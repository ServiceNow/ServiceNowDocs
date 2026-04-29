---
title: MIDServerFinder - Global
description: The MIDServerFinder script include provides methods to find a list of MID Servers for specified IP addresses.Creates an instance of MIDServerFinder.Gets the names of MID servers available for a given range and capability.Gets the sys\_ids of MID servers available for a given range and capability.Gets the state of the finder operation.Sets whether to look for active or inactive MID servers. By default, searches are for active MID servers unless inactive is specified by this method.Sets the technologies for which to look.Turns debugging on or off.Sets the range of IP addresses for which to look.Determines if the input is a single IP or a hostname, and passes the IP or multiple IPs to the setRanges\(\) method.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServerFinder- Global

The MIDServerFinder script include provides methods to find a list of MID Servers for specified IP addresses.

Use in server scripts to get the MID Server list.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServerFinder - MIDServerFinder\(\)

Creates an instance of MIDServerFinder.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## MIDServerFinder - getMIDServers\(\)

Gets the names of MID servers available for a given range and capability.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of MID server names. If no MID servers are available, returns an empty array.|

```
var msf = new MIDServerFinder();
msf.setRanges('10.10.10.1-10.10.11.254');
var msnames = msf.getMIDServers();
 
for(var i=0; i<msnames.length; i++) {
  gs.print(msnames[i]);
};
```

## MIDServerFinder - getMIDServersBySysId\(\)

Gets the sys\_ids of MID servers available for a given range and capability.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of MID server sys\_ids. If no MID servers are available, returns an empty array.|

```
var msf = new MIDServerFinder();
msf.setRanges('10.10.10.1-10.10.11.254');
var msids = msf.getMIDServersBySysId();
 
for(var i=0; i<msids.length; i++) {
  gs.print(msids[i]);
};
```

## MIDServerFinder - getStatusMessage\(\)

Gets the state of the finder operation.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The status message|

```
var msf = new MIDServerFinder();
gs.print(msf.getStatusMessage());
```

## MIDServerFinder - setActive\(Boolean flag\)

Sets whether to look for active or inactive MID servers. By default, searches are for active MID servers unless inactive is specified by this method.

|Name|Type|Description|
|----|----|-----------|
|flag|Boolean|If true, look for inactive MID servers. If false, do not look for inactive MID servers.|

|Type|Description|
|----|-----------|
|void| |

```
var msf = new MIDServerFinder();
msf.setActive('true');
```

## MIDServerFinder - setCapabilities\(Array capabilities\)

Sets the technologies for which to look.

|Name|Type|Description|
|----|----|-----------|
|capabilities|Array|Contains a list of capabilities, for example - `capabilities = ["ssh","wmi","snmp",{"os_domain":"disco"},{"phase":1}];`|

|Type|Description|
|----|-----------|
|void| |

```
var msf = new MIDServerFinder();
msf.setRanges('10.10.10.1-10.10.11.254');
var capab = ["ssh","wmi","snmp"];
msf.setCapabilities(capab);
```

## MIDServerFinder - setDebug\(Boolean onOrOff\)

Turns debugging on or off.

|Name|Type|Description|
|----|----|-----------|
|onOrOff|Boolean|True to turn on debugging; false to turn debugging off.|

|Type|Description|
|----|-----------|
|void| |

```
var msf = new MIDServerFinder();
msf.setDebug('true');
```

## MIDServerFinder - setRanges\(String ranges\)

Sets the range of IP addresses for which to look.

<table id="table_uvk_jfl_zt" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ranges

</td><td>

String

</td><td>

A comma-separated list in one of these formats. -   IP addresses \(10.10.10.1, 10.10.10.2\)
-   IP networks \(10.10.10.0/23\)
-   IP ranges \(10.10.10.1-10.10.11.254\)

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var msf = new MIDServerFinder();
msf.setRanges('10.10.10.1-10.10.11.254');
```

## MIDServerFinder - setRangesByIPOrHostname\(String ipOrHostname\)

Determines if the input is a single IP or a hostname, and passes the IP or multiple IPs to the setRanges\(\) method.

If the value of ipOrHostname is an IP address, it is passed into the setRanges\(\) method. It the value is a hostname, we look up the DNS table \(cmdb\_ip\_address\_dns\_name\) to try resolving the hostname. The result, either an IP or multiple IPs, is then passes into the setRanges\(\) method.

|Name|Type|Description|
|----|----|-----------|
|ipOrHostname|String|The IP address, IP range, or host name.|

|Type|Description|
|----|-----------|
|void| |

```
var msf = new MIDServerFinder();
msf.setRangesByIPOrHostname('10.10.10.1-10.10.11.254');
```

