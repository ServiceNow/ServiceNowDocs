---
title: MIDServer - Global
description: The MIDServer script include provides methods to encapsulate the notion of a MID Server.Returns the specified MID server.Returns the MID server associated with the specified schedule \(the MID server with the same name\). If there is no associated MID server, gets the next MID server in the ecc\_agent table.Returns the MID Server with the specified schedule and range set.The name of the MID server's host.The operating system of the MID server's host.The IP address of the MID server's host.Name of the MID server.The network containing the MID server's host.The IP address of the MID server host's default router.The MID server's status \("Up" or "Down"\).The sys\_id of the MID server record.The URL the MID server uses to contact the instance.Version of the MID server \(WAR name\).Windows domain of the MID server's host \(if it is a Windows machine\).
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MIDServer- Global

The MIDServer script include provides methods to encapsulate the notion of a MID Server.

Use these methods in server scripts to manage a MID Server using Ajax.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MIDServer - getByName\(String name\)

Returns the specified MID server.

|Name|Type|Description|
|----|----|-----------|
|name|String|The MID server name|

|Type|Description|
|----|-----------|
|GlideRecord|The record of the requested MID server.|

The following example shows how to access and display mid server details.

```
// Get a mid server object by name
var ms = MIDServer.getByName("windows_mid");

// Stringify the object for display purposes
gs.info(JSON.stringify(ms, null, 2));

// Show the value of each API property 
gs.info('hostmane ' + ms.hostname);
gs.info('hostOS ' + ms.hostOS);
gs.info('ip ' + ms.ip);
gs.info('name ' + ms.name);
gs.info('routerIP ' + ms.routerIP);
gs.info('status ' + ms.status);
gs.info('sysID ' + ms.sysID);
gs.info('url ' + ms.url);
gs.info('version ' + ms.version);
gs.info('windowsDomain ' + ms.windowsDomain);
```

Output:

```
*** Script: {
  "valid": true,
  "sysID": "3cb25f0f874b3410c3a99999cebb35ba",
  "name": "windows_mid",
  "url": null,
  "hostname": "myHostname.service-now.com",
  "hostOS": "Windows",
  "version": "fixed",
  "ip": "10.11.128.184",
  "routerIP": "10.11.128.1",
  "network": "10.11.128.0/22",
  "windowsDomain": null,
  "status": "Up",
  "validated": "true",
  "userName": "MID_Profile"
}
*** Script: hostname myHostname.service-now.com
*** Script: hostOS Windows
*** Script: ip 10.11.128.184
*** Script: name windows_mid
*** Script: routerIP 10.11.128.1
*** Script: status Up
*** Script: sysID 3cb25f0f874b3410c3a99999cebb35ba
*** Script: url null
*** Script: version fixed
*** Script: windowsDomain null

```

## MIDServer - getDefault\(DiscoverySchedule schedule\)

Returns the MID server associated with the specified schedule \(the MID server with the same name\). If there is no associated MID server, gets the next MID server in the ecc\_agent table.

|Name|Type|Description|
|----|----|-----------|
|schedule|DiscoverySchedule|The discovery schedule|

|Type|Description|
|----|-----------|
|GlideRecord|The MID server|

## MIDServer - getForPing\(DiscoverySchedule schedule, DiscoveryRange range\)

Returns the MID Server with the specified schedule and range set.

|Name|Type|Description|
|----|----|-----------|
|schedule|DiscoverySchedule|The discovery schedule|
|range|DiscoveryRange|The discovery range set|

|Type|Description|
|----|-----------|
|GlideRecord|The MID server|

## MIDServer - hostname

The name of the MID server's host.

|Name|Type|Description|
|----|----|-----------|
|hostname|String|The name of the MID server's host.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

q

## MIDServer - hostOS

The operating system of the MID server's host.

|Name|Type|Description|
|----|----|-----------|
|hostOS|String|The operating system of the MID server's host.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - ip

The IP address of the MID server's host.

|Name|Type|Description|
|----|----|-----------|
|ip|String|The IP address of the MID server's host.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - name

Name of the MID server.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the MID server|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - network

The network containing the MID server's host.

|Name|Type|Description|
|----|----|-----------|
|network|String|The network containing the MID server's host. For example, "10.10.10.0/24" or "10.10.10.0/255.255.255.0".|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - routerIP

The IP address of the MID server host's default router.

|Name|Type|Description|
|----|----|-----------|
|routerIP|String|The IP address of the MID server host's default router.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - status

The MID server's status \("Up" or "Down"\).

|Name|Type|Description|
|----|----|-----------|
|status|String|The MID server's status \("Up" or "Down"\).|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - sysID

The sys\_id of the MID server record.

|Name|Type|Description|
|----|----|-----------|
|sysID|String|The sys\_id of the MID server record.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - url

The URL the MID server uses to contact the instance.

|Name|Type|Description|
|----|----|-----------|
|url|String|The URL the MID server uses to contact the instance.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - version

Version of the MID server \(WAR name\).

|Name|Type|Description|
|----|----|-----------|
|version|String|Version of the MID server \(WAR name\).|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

## MIDServer - windowsDomain

Windows domain of the MID server's host \(if it is a Windows machine\).

|Name|Type|Description|
|----|----|-----------|
|windowsDomain|String|The Windows domain of the MID server's host.|

The following example shows how to execute and return all parameters of an available Mid server.

```
var getMIDServerAttributes = new MIDServer(<mid_sys_id>); //Pass the sys id of the MID server record
var midServerHostname = getMIDServerAttributes.hostname; //would return the Host name of the MID Server Record
var midServerHostOS = getMIDServerAttributes.hostOS; // would return the Host OS of the MID Server Record
var midServerIP = getMIDServerAttributes.ip; //would return the IP of the MID Server Record
var midServerName = getMIDServerAttributes.name; //would return the Name of the MID Server Record
var midServerRouterIP = getMIDServerAttributes.routerIP; //would return the router IP of the MID Server Record
var midServerStatus = getMIDServerAttributes.status; //would return the status of the MID Server Record (UP or Down)
var midServerSysID = getMIDServerAttributes.sysID; // Would return the Sys ID of the MID server record
var midServerURL = getMIDServerAttributes.url; // Would return the URL of the MID server record
var midServerVersion = getMIDServerAttributes.version; // Would return ServiceNow release version of the MID server record
var midServerwindowsDomain = getMIDServerAttributes.windowsDomain; // Would return windows domain of the MID server record

gs.info("\nMID Server Host Name - "+ midServerHostname +"\nMid Server Host OS - " + midServerHostOS + "\nMID Server IP - "+ midServerIP + "
\nMID Server Name - " + midServerName + "\nMID Server Router IP - " + midServerRouterIP + "\nMID Server Status - " +  midServerStatus  + 
"\nMID Server SYS ID - " + midServerSysID  + "\nMID Server URL - " + midServerURL  + "\nMID Server Version - " + midServerVersion + 
"\nMID Server Windows Domain - " + midServerwindowsDomain);
```

Output:

```
MID Server Host Name - midSvrName.service-now.com
Mid Server Host OS - Windows
MID Server IP - 10.11.999.999
MID Server Name - Windows MID
MID Server Router IP - 10.11.111.1
MID Server Status - Up
MID Server SYS ID - <mid_sys_id>
MID Server URL - null
MID Server Version - fixed
MID Server Windows Domain - null
```

