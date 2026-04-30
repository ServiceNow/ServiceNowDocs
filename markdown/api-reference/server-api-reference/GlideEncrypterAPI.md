---
title: GlideEncrypter - Global \(deprecated\)
description: The GlideEncrypter API provides methods to encrypt and decrypt strings using the Triple DES algorithm.Creates an instance of the GlideEncrypter class using a default \(static\) encryption key.Creates an instance of the GlideEncrypter class using a given encryption key.Decrypts a clear string using the Triple DES algorithm.Encrypts a clear string using the Triple DES algorithm.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideEncrypter- Global \(deprecated\)

The GlideEncrypter API provides methods to encrypt and decrypt strings using the Triple DES algorithm.

**Note:** The GlideEncrypter API uses the three-key Triple DES encryption standard which [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf) has recommended against using to encrypt data after 2023. Please take a moment to review the information below.

-   Starting with the Xanadu family release, the GlideEncrypter API is not recommended for use, as this API is deprecated according to NIST guidelines. With the Zurich release, the GlideEncrypter API will be upgraded to automatically use Key Management Framework.
-   New instance installations and re-installations using the GlideEncrypter API in the ServiceNow AI Platform will not be permitted in the Zurich release planned for September 2025. Use the [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) to identify where GlideEncrypter is used on your instance. Find this tool on your instance by navigating to **Instance Scan** &gt; **Suites** &gt; **GlideEncrypter**.
-   Review the following Knowledge Base article for migration guidance to the applicable replacement solution based on your current use case: [Alternatives to deprecated GlideEncrypter APIs](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1320986).

If the GlideEncrypter API is no longer used on your instance, you may deprecate 3DES. For details, see [Prepare your instance for GlideEncrypter deprecation](https://www.servicenow.com/docs/access?context=check-3des&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

You can use this API in server scripts in the global scope. The GlideEncrypter class has two constructors:

-   GlideEncrypter\(\)
-   GlideEncrypter\(String key\)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideEncrypter - GlideEncrypter\(\)

Creates an instance of the GlideEncrypter class using a default \(static\) encryption key.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var encr = new GlideEncrypter(); 
```

## GlideEncrypter - GlideEncrypter\(String key\)

Creates an instance of the GlideEncrypter class using a given encryption key.

|Name|Type|Description|
|----|----|-----------|
|key|String|Your encryption key must be exactly 24 characters. A key longer than 24 characters will be truncated.|

```
var encr = new GlideEncrypter(myKey); 
```

## GlideEncrypter - decrypt\(String encryptedString\)

Decrypts a clear string using the Triple DES algorithm.

|Name|Type|Description|
|----|----|-----------|
|encryptedString|String|String to be decrypted.|

|Type|Description|
|----|-----------|
|String|Clear text string.|

```
var encr = new GlideEncrypter(); 
var clearString = 'abcdefg'; 
var encrString = encr.encrypt(clearString);
var decrString = encr.decrypt(encrString);  
gs.print("Decrypted string = " + decrString);
```

Output:

```
Decrypted string = abcdefg
```

## GlideEncrypter - encrypt\(String clearString\)

Encrypts a clear string using the Triple DES algorithm.

|Name|Type|Description|
|----|----|-----------|
|clearString|String|String to be encrypted.|

|Type|Description|
|----|-----------|
|String|Encrypted string.|

```
var encr = new GlideEncrypter(); 
var clearString = 'abcdefg'; 
var encrString = encr.encrypt(clearString); 
gs.print("Encrypted string = " + encrString); 

```

Output:

```
Encrypted string = 3wjpvKtUIi4=
```

