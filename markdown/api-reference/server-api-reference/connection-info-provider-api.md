---
title: ConnectionInfoProvider - Scoped, Global
description: The ConnectionInfoProvider API provides methods to select connection information through the connection alias.Selects connection information through the connection alias.Retrieves a ConnectionInfo object identified by the given aliasID in the current domain.Retrieves a ConnectionInfo object identified by the given aliasID for a specific domain.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ConnectionInfoProvider - Scoped, Global

The ConnectionInfoProvider API provides methods to select connection information through the connection alias.

You can use this API in scoped applications or within the global scope. In scoped scripts, use the `sn_cc` namespace identifier.

This function retrieves connection information identified by the given connection alias.

```
var provider = new sn_cc.ConnectionInfoProvider();

// get a jdbc connection in the current domain with the alias ID
//     "6219afbf9f03320021dd7501942e70fc"
var connectionInfo = provider.getConnectionInfo("6219afbf9f03320021dd7501942e70fc");
if (connectionInfo != null) {
  // get data map
  var datamap = connectionInfo.getDataMap();
  gs.info(datamap["name"]);
  gs.info(datamap["connection_url"]);

  // get the same values using getAttribute
  gs.info(connectionInfo.getAttribute("name"));
  gs.info(connectionInfo.getAttribute("connection_url"));

  // get credential attributes
  gs.info(connectionInfo.getCredentialAttribute("user_name"));
  gs.info(connectionInfo.getCredentialAttribute("password")); 

  // get extended attributes
  var extendedAttributes = connectionInfo.getExtendedAttributes();  
  gs.info(extendedAttributes["name1"]);
 }

 // get a jdbc connection in the ACME domain with the alias ID
 //      "cd5923ff9f03320021dd7501942e70bb"
 connectionInfo = provider.getConnectionInfoByDomain("cd5923ff9f03320021dd7501942e70bb",
        "c90d4b084a362312013398f051272c0d");
 if (connectionInfo != null) {
   // get data map
   var datamap = connectionInfo.getDataMap();
   gs.info(datamap["name"]);
 }

```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ConnectionInfoProvider - ConnectionInfoProvider\(\)

Selects connection information through the connection alias.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## ConnectionInfoProvider - getConnectionInfo\(String aliasID\)

Retrieves a ConnectionInfo object identified by the given aliasID in the current domain.

|Name|Type|Description|
|----|----|-----------|
|aliasID|String|Sys\_id of a connection alias.|

|Type|Description|
|----|-----------|
|ConnectionInfo|Information about the connection.|

```
var provider = new sn_cc.ConnectionInfoProvider();

// get a jdbc connection in the current domain with the alias ID
//     "6219afbf9f03320021dd7501942e70fc"
var connectionInfo = provider.getConnectionInfo("6219afbf9f03320021dd7501942e70fc");
```

## ConnectionInfoProvider - getConnectionInfoByDomain\(String aliasID, String domainID\)

Retrieves a ConnectionInfo object identified by the given aliasID for a specific domain.

|Name|Type|Description|
|----|----|-----------|
|aliasID|String|Sys\_id of a connection alias.|
|domainID|String|Sys\_id of a domain or `global`.|

|Type|Description|
|----|-----------|
|ConnectionInfo|Connection information.|

```
var provider = new sn_cc.ConnectionInfoProvider();

// get a jdbc connection in the ACME domain with the alias ID
 //      "cd5923ff9f03320021dd7501942e70bb"
 connectionInfo = provider.getConnectionInfoByDomain("cd5923ff9f03320021dd7501942e70bb",
        "c90d4b084a362312013398f051272c0d");
```

