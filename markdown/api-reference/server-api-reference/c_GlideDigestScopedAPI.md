---
title: GlideDigest - Scoped
description: The scoped GlideDigest class provides methods for creating a message digest from strings or input streams using MD5, SHA1, or SHA256 hash algorithms.Creates an instance of scoped GlideDigest.Creates a message digest from a string using the MD5 algorithm. The output string is in Base64.Creates a message digest from an input stream using the MD5 algorithm. The output string is in Base64.Creates a message digest from a string using the MD5 algorithm. The output string is in hexadecimal.Creates a message digest from an input stream using the MD5 algorithm. The output string is in hexadecimal.Creates a message digest from a string using the SHA1 algorithm. The output string is in Base64.Creates a message digest from an input stream using the SHA1 algorithm. The output string is in Base64.Creates a message digest from a string using the SHA1 algorithm. The output string is in hexadecimal.Creates a message digest from an input stream using the SHA1 algorithm. The output string is in hexadecimal.Creates a message digest from a string using the SHA256 algorithm. The output string is in Base64.Creates a message digest from an input stream using the SHA256 algorithm. The output string is in Base64.Creates a message digest from a string using the SHA256 algorithm. The output string is in hexadecimal.Creates a message digest from an input stream using the SHA256 algorithm. The output string is in hexadecimal.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDigest- Scoped

The scoped GlideDigest class provides methods for creating a message digest from strings or input streams using MD5, SHA1, or SHA256 hash algorithms.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDigest - GlideDigest\(\)

Creates an instance of scoped GlideDigest.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## GlideDigest - getMD5Base64\(String source\)

Creates a message digest from a string using the MD5 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getMD5Base64(inputString));
```

## GlideDigest - getMD5Base64FromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the MD5 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getMD5Base64FromInputStream(inputStream));
```

## GlideDigest - getMD5Hex\(String source\)

Creates a message digest from a string using the MD5 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getMD5Hex(inputString));
```

## GlideDigest - getMD5HexFromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the MD5 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getMD5HexFromInputStream(inputStream));
```

## GlideDigest - getSHA1Base64\(String source\)

Creates a message digest from a string using the SHA1 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getSHA1Base64(inputString));
```

## GlideDigest - getSHA1Base64FromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the SHA1 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getSHA1Base64FromInputStream(inputStream));
```

## GlideDigest - getSHA1Hex\(String source\)

Creates a message digest from a string using the SHA1 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getSHA1Hex(inputString));
```

## GlideDigest - getSHA1HexFromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the SHA1 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getSHA1HexFromInputStream(inputStream));
```

## GlideDigest - getSHA256Base64\(String source\)

Creates a message digest from a string using the SHA256 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getSHA256Base64(inputString));
```

## GlideDigest - getSHA256Base64FromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the SHA256 algorithm. The output string is in Base64.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getSHA256Base64FromInputStream(inputStream));
```

## GlideDigest - getSHA256Hex\(String source\)

Creates a message digest from a string using the SHA256 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|source|String|The source string.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputString = "Her molasses flowed slowly down the hill.";
var digest = new GlideDigest();
gs.info(digest.getSHA256Hex(inputString));
```

## GlideDigest - getSHA256HexFromInputStream\( GlideScriptableInputStream inputStream\)

Creates a message digest from an input stream using the SHA256 algorithm. The output string is in hexadecimal.

|Name|Type|Description|
|----|----|-----------|
|inputStream|GlideScriptableInputStream|The source input stream.|

|Type|Description|
|----|-----------|
|String|The message digest.|

```
var inputStream = new GlideSysAttachment().getContentStream(attachmentSysID);
var digest = new GlideDigest();
gs.info(digest.getSHA256HexFromInputStream(inputStream));
```

