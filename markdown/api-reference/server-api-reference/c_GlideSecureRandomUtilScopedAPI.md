---
title: GlideSecureRandomUtil - Scoped, Global
description: The GlideSecureRandomUtil API provides methods for generating integers, long values, and strings.Generates a pseudo-random integer.Generates a pseudo-random integer between 0 \(inclusive\) and the bound \(exclusive\) value that you pass into the method.Generates pseudo-random long value.Generates a random alpha-numeric String with the specified length.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSecureRandomUtil - Scoped, Global

The GlideSecureRandomUtil API provides methods for generating integers, long values, and strings.

There is no constructor for this class. Methods are accessed through the static object GlideSecureRandomUtil. The GlideSecureRandomUtil class is available in both global and scoped applications.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideSecureRandomUtil - getSecureRandomInt\(\)

Generates a pseudo-random integer.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The pseudo-randomly generated integer.|

```
gs.info(GlideSecureRandomUtil.getSecureRandomInt());

```

Output:

```
1976146969
```

## GlideSecureRandomUtil - getSecureRandomIntBound\(Number bound\)

Generates a pseudo-random integer between 0 \(inclusive\) and the bound \(exclusive\) value that you pass into the method.

|Name|Type|Description|
|----|----|-----------|
|bound|Number|The bound value.|

|Type|Description|
|----|-----------|
|Number|The pseudo-randomly generated integer.|

```
gs.info(GlideSecureRandomUtil.getSecureRandomIntBound(100));
```

Output:

```
55
```

## GlideSecureRandomUtil - getSecureRandomLong\(\)

Generates pseudo-random long value.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|The pseudo-randomly generated 64-bit integer.|

```
gs.info(GlideSecureRandomUtil.getSecureRandomLong());

```

Output:

```
792836514424092500
```

## GlideSecureRandomUtil - getSecureRandomString\(Number length\)

Generates a random alpha-numeric String with the specified length.

|Name|Type|Description|
|----|----|-----------|
|length|Number|The length of the string in number of characters.|

|Type|Description|
|----|-----------|
|String|The randomly generated string.|

```
gs.info(GlideSecureRandomUtil.getSecureRandomString(12));
```

Output:

```
1XzVI0sLfVlT
```

