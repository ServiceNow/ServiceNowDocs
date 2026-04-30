---
title: SNMPResponse - Global
description: The SNMPResponse script include provides methods to wrap an SNMP payload response instance with methods to safely and easily retrieve SNMP singleton fields or tables.Builds an index to all SNMP entities in the current object.Builds references to actual instances for all identified indexes \(in the discovery\_snmp\_ref table\) that can be resolved.Returns an array of OIDs that match the given ref\_base and which have a defined, non-null ref\_leaf.Returns the integer contained in the OID object with the given MIB name.Retrieves the OID object with the given MIB name from the response.Returns a hashmap of table entries under the given parent MIB name, with the given entry MIB names.Returns the text contained in the OID object with the given MIB name.Resolves SNMP tables into hashmaps and OID values into primitives.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SNMPResponse- Global

The SNMPResponse script include provides methods to wrap an SNMP payload response instance with methods to safely and easily retrieve SNMP singleton fields or tables.

Use this script include to retrieve SNMP singleton fields or tables.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SNMPResponse - buildIndex\(Object cur, String name, String extName\)

Builds an index to all SNMP entities in the current object.

|Name|Type|Description|
|----|----|-----------|
|cur|Object|The current object|
|name|String|The index name|
|extName|String|The index extension|

|Type|Description|
|----|-----------|
|void| |

## SNMPResponse - buildReferences\(\)

Builds references to actual instances for all identified indexes \(in the discovery\_snmp\_ref table\) that can be resolved.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## SNMPResponse - getAmbiguousOIDs\(String refBase, String refLeaf\)

Returns an array of OIDs that match the given ref\_base and which have a defined, non-null ref\_leaf.

The last character of ref\_base may be a question mark; in that case, if the parent node is a table then all table entries are returned.

|Name|Type|Description|
|----|----|-----------|
|refBase|String|The reference base|
|refLeaf|String|The reference leaf|

|Type|Description|
|----|-----------|
|Array|An array of OIDs that match the given ref\_base and which have a defined, non-null ref\_leaf.|

## SNMPResponse - getOIDInt\(String name\)

Returns the integer contained in the OID object with the given MIB name.

|Name|Type|Description|
|----|----|-----------|
|name|String|The MIB name|

|Type|Description|
|----|-----------|
|Number|The integer contained in the OID object, or zero if the object could not be found or is empty.|

## SNMPResponse - getOIDObj\(String name\)

Retrieves the OID object with the given MIB name from the response.

This method does not work with numeric OID strings, only MIB names.

|Name|Type|Description|
|----|----|-----------|
|name|String|The MIB name|

|Type|Description|
|----|-----------|
|OID object|The OID object with the given MIB name, or null if the object could not be found or if any table entries are encountered while walking down the named elements.|

## SNMPResponse - getOIDTable\(String parentName, String entryName\)

Returns a hashmap of table entries under the given parent MIB name, with the given entry MIB names.

|Name|Type|Description|
|----|----|-----------|
|parentName|String|The parent MIB name|
|entryName|String|The entry MIB name|

|Type|Description|
|----|-----------|
|Hashmap|A hashmap of table entries under the given parent MIB name, with the given entry MIB names, or null if the parent does not exist.|

## SNMPResponse - getOIDText\(String name\)

Returns the text contained in the OID object with the given MIB name.

|Name|Type|Description|
|----|----|-----------|
|name|String|The MIB name|

|Type|Description|
|----|-----------|
|String|The text contained in the OID object. Returns null if the object could not be found, or if it has no text.|

## SNMPResponse - normalize\(Object cur\)

Resolves SNMP tables into hashmaps and OID values into primitives.

All SNMP numeric types convert to a JavaScript number. An SNMP null type converts to a JavaScript null. An SNMP IP Address value converts to a Java IPAddressV4 instance. All other values convert to a JavaScript string.

|Name|Type|Description|
|----|----|-----------|
|cur|Object|The SNMP table or OID value.|

|Type|Description|
|----|-----------|
|void| |

