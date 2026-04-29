---
title: ConnectionInfo - Scoped, Global
description: The ConnectionInfo API enables you to get connection attribute information through the connection and credential alias.Returns the value of a ConnectionInfo attribute with the specified property name.Returns the value of credential attributes for a specified connection.Returns the connection attributes as a collection of key-value pairs.Returns the extended attributes as a collection of key-value pairs.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ConnectionInfo- Scoped, Global

The ConnectionInfo API enables you to get connection attribute information through the connection and credential alias.

You can use this API in scoped applications or within the global scope. In scoped scripts, use the `sn_cc` namespace identifier.

For more information on connections and credentials, see [Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

This function retrieves connection attribute information identified by the given connection and credential alias.

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

## Scoped ConnectionInfo - getAttribute\(String name\)

Returns the value of a ConnectionInfo attribute with the specified property name.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of a ConnectionInfo object property.|

|Type|Description|
|----|-----------|
|String|Value of a specified ConnectionInfo property.|

```
  // get the same values using getAttribute
  gs.info(connectionInfo.getAttribute("name"));
  gs.info(connectionInfo.getAttribute("connection_url"));

```

## Scoped ConnectionInfo - getCredentialAttribute\(\)

Returns the value of credential attributes for a specified connection.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Key-value pair map of credential attributes.|

```
 // get credential attributes
  gs.info(connectionInfo.getCredentialAttribute("user_name"));
  gs.info(connectionInfo.getCredentialAttribute("password")); 

```

## Scoped ConnectionInfo - getDataMap\(\)

Returns the connection attributes as a collection of key-value pairs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Key-value pair map of connection attributes.|

```
 // get data map
  var datamap = connectionInfo.getDataMap();
  gs.info(datamap["name"]);
  gs.info(datamap["connection_url"]);

```

## Scoped ConnectionInfo - getExtendedAttributes\(\)

Returns the extended attributes as a collection of key-value pairs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Key-value pair map of extended attributes.|

```
// get extended attributes
  var extendedAttributes = connectionInfo.getExtendedAttributes();  
  gs.info(extendedAttributes["name1"]);
 }

```

