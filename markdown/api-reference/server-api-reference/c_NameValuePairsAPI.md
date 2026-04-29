---
title: NameValuePairs - Global
description: The NameValuePairs script include provides methods to convert between maps and strings representing the name/value pairs in the map.Creates an instance of the class initialized with the specified string.Creates an instance of the class initialized with the specified hash map.Produces this.string from this.map.If the specified value contains double quotes, equals, commas, or spaces, this method surrounds the value with double quotes and doubles up any enclosed double quotes.Produces this.map from this.string.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# NameValuePairs- Global

The NameValuePairs script include provides methods to convert between maps and strings representing the name/value pairs in the map.

The string form is: `<name> = <value>, <name> = <value, ...` where `<name>` is a string name, optionally surrounded by double quotes \(Microsoft-style\), and `<value>` is a string value, also optionally surrounded by double quotes.

The following are all examples of valid name/value strings:

-   `name = value`
-   `name = "My Value", name = value`
-   `"My Name = this" = "My Value", "My Value, all the time", name = value`
-   `"My Name" = "This" "name""", name = value`

In the third example, the quoted values contain equals and commas. In the fourth example, the quoted value contains a quote.

Instances have the following properties initialized:

-   map: The map \(JavaScript object being used as a hashmap\) form of the name/value pairs, with Microsoft-style quotes removed
-   string: The string form of the name/value pairs, with Microsoft-style quoting.

Use with any server-side script where you need convert name/value pairs between maps and strings.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## NameValuePairs - NameValuePairs\(String stringForm\)

Creates an instance of the class initialized with the specified string.

|Name|Type|Description|
|----|----|-----------|
|stringForm|String|The values to use when creating the object.|

## NameValuePairs - NameValuePairs\(Object mapForm\)

Creates an instance of the class initialized with the specified hash map.

|Name|Type|Description|
|----|----|-----------|
|mapForm|Object|The map to use when creating the object.|

## NameValuePairs - mapToString\(\)

Produces `this.string` from `this.map`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## NameValuePairs - quotify\(Object value\)

If the specified value contains double quotes, equals, commas, or spaces, this method surrounds the value with double quotes and doubles up any enclosed double quotes.

|Name|Type|Description|
|----|----|-----------|
|value|Object|The value to process|

|Type|Description|
|----|-----------|
|String|The value with added quotes.|

## NameValuePairs - stringToMap\(\)

Produces `this.map` from `this.string`.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

