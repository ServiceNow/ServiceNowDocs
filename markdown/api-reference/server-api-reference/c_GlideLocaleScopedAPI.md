---
title: GlideLocale - Scoped
description: The GlideLocale API provides information about display information for the local instance.Returns the GlideLocale object.Returns the decimal separator.Returns the grouping separator.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideLocale- Scoped

The GlideLocale API provides information about display information for the local instance.

There is no constructor for a GlideLocale object. Use the get\(\) method to obtain a GlideLocale object.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideLocale - get\(\)

Returns the GlideLocale object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideLocale|The GlideLocale object.|

```
var locale = GlideLocale.get();
```

## GlideLocale - getDecimalSeparator\(\)

Returns the decimal separator.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The decimal separator.|

```
var locale = GlideLocale.get();
var decimalSeparator = locale.getDecimalSeparator();
gs.info( "The decimal separator is " + decimalSeparator);
```

Output:

```
The decimal separator is .
```

## GlideLocale - getGroupingSeparator\(\)

Returns the grouping separator.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The grouping separator.|

```
var locale = GlideLocale.get();var groupingSeparator = locale.getGroupingSeparator();
gs.info( "The grouping separator is " + groupingSeparator);
```

Output:

```
The grouping separator is ,
```

