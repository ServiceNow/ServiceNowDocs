---
title: GlideEncrypter - Global \(deprecated\)
description: The GlideEncrypter API provides methods to encrypt and decrypt strings using the Key Management Framework \(KMF\).Creates an instance of the GlideEncrypter class using a Key Management Framework \(KMF\) cryptographic module.Creates an instance of the GlideEncrypter class using a given encryption key.Decrypts a clear string using the KMF-based Advanced Encryption Standard \(AES\) algorithm.Encrypts a clear string using the Key Management Framework \(KMF\) algorithm.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideEncrypter- Global \(deprecated\)

The GlideEncrypter API provides methods to encrypt and decrypt strings using the Key Management Framework \(KMF\).

**Important:** The GlideEncrypter API no longer supports Triple Data Encryption Standard \(3DES\) due to NIST guidelines \(see [NIST 800-131A Rev 2](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-131Ar2.pdf)\). As a result, the following changes were implemented in the Zurich release:

-   For existing instances that upgrade to the Zurich release, the `GlideEncrypter` API is available for use but has been updated to automatically use the Key Management Framework \(KMF\) algorithm.
-   For all new instances created starting with the Zurich release, the `GlideEncrypter` API is no longer supported. Directly use the [Key Management Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/encryption.md) instead for all cryptography operations.

You can use this API in server scripts in the global scope. The GlideEncrypter class has two constructors:

-   GlideEncrypter\(\)
-   GlideEncrypter\(String key\)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideEncrypter - GlideEncrypter\(\)

Creates an instance of the GlideEncrypter class using a Key Management Framework \(KMF\) cryptographic module.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var encr = new GlideEncrypter(); 
```

## GlideEncrypter - GlideEncrypter\(String key\)

Creates an instance of the GlideEncrypter class using a given encryption key.

<table id="table_ogs_flj_1z" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Customer key to be used for encrypting or decrypting using Triple DES algorithm. Encryption key must be exactly 24 characters. A key longer than 24 characters will be truncated.

</td></tr></tbody>
</table>```
var encr = new GlideEncrypter(myKey); 
```

## GlideEncrypter - decrypt\(String encryptedString\)

Decrypts a clear string using the KMF-based Advanced Encryption Standard \(AES\) algorithm.

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

Encrypts a clear string using the Key Management Framework \(KMF\) algorithm.

|Name|Type|Description|
|----|----|-----------|
|clearString|String|String to be encrypted.|

|Type|Description|
|----|-----------|
|String|Encrypted string.|

The following example uses the GlideEncrypter\(\) constructor to encrypt a given string:

```
var encr = new GlideEncrypter(); 
var clearString = 'abcdefg'; 
var encrString = encr.encrypt(clearString); 
gs.print("Encrypted string = " + encrString);
```

Output:

```
Encrypted string = ﷮﷯﷮ febaf83bff31221093d7ffffffffff79﷬ 1﷬﷭BaXD6acaRjZLPUn_bZiZ-w==2c9-PNa0qouYXyBhJtV6-2E31Rm7mWg=﷮﷯ 
```

