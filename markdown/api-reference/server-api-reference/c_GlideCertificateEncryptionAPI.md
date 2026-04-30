---
title: GlideCertificateEncryption - Global
description: The GlideCertificateEncryption API provides methods for encrypting certificates.Instantiates a GlideCertificateEncryption object.Generates the Message Authentication Code \(MAC\), which is used to authenticate a message.Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from Trust Store Cert.Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from the key store entry.Signs the data using the private key and the given algorithm.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideCertificateEncryption- Global

The GlideCertificateEncryption API provides methods for encrypting certificates.

Use these methods to generate a hash for the certificate, sign data using a private key, and generate a message authentication code.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideCertificateEncryption - GlideCertificateEncryption\(\)

Instantiates a GlideCertificateEncryption object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

### Scoped equivalent

To use the GlideCertificateEncryption\(\) constructor in a scoped application, use the corresponding scoped constructor: [CertificateEncryption\(\)](../../CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#).

## GlideCertificateEncryption - generateMac\(String key, String algorithm, String data\)

Generates the Message Authentication Code \(MAC\), which is used to authenticate a message.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key to use to sign the message. Must be Base64 encoded.|
|algorithm|String|Algorithm to use to generate the MAC: HmacSHA256, HmacSHA1, HmacMD5, and so on.|
|data|String|Data to process.|

|Type|Description|
|----|-----------|
|String|MAC in base64 format.|

```
var mac = new GlideCertificateEncryption;
var key = "sample_key"; 
key = GlideStringUtil.base64Encode(key);
mac.generateMac(key, "HmacSHA256", "sample_data");
```

### Scoped equivalent

To use the generateMac\(\) method in a scoped application, use the corresponding scoped method: [generateMac\(\)](../../CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#).

## GlideCertificateEncryption - getThumbPrint\(String certificateID, String algorithm\)

Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from Trust Store Cert.

|Name|Type|Description|
|----|----|-----------|
|certificateID|String|sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.|
|algorithm|String|SHA-1, SHA-256, and so on|

|Type|Description|
|----|-----------|
|String|Thumbprint in base64 format.|

### Scoped equivalent

To use the getThumbPrint\(\) method in a scoped application, use the corresponding scoped method: [getThumbPrint\(\)](../../CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#).

## GlideCertificateEncryption - getThumbPrintFromKeystore\(String certificateID, String alias, String algorithm\)

Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from the key store entry.

|Name|Type|Description|
|----|----|-----------|
|certificateID|String|sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.|
|alias|String|Alias name for the certificate.|
|algorithm|String|SHA-1, SHA-256, and so on.|

|Type|Description|
|----|-----------|
|String|Thumbprint in base64 format.|

### Scoped equivalent

To use the getThumbPrintFromKeystore\(\) method in a scoped application, use the corresponding scoped method: [getThumbPrintFromKeystore\(\)](../../CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#).

## GlideCertificateEncryption - sign\(String certificateID, String alias, String aliaspassword, String algorithm, String datatosign\)

Signs the data using the private key and the given algorithm.

|Name|Type|Description|
|----|----|-----------|
|certificateID|String|sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.|
|alias|String|Private key name.|
|aliaspassword|String|Password for the private key.|
|datatosign|String|Data to sign.|
|algorithm|String|SHA-1, SHA-256, and so on.|

|Type|Description|
|----|-----------|
|String|Signed data in base64 format.|

```
var gce = new GlideCertificateEncryption;
gce.sign("recordID", "alias", "password", "SHA-1", "sign this data");
```

### Scoped equivalent

To use the sign\(\) method in a scoped application, use the corresponding scoped method: [sign\(\)](../../CertificateEncryptionScoped/concept/c_CertificateEncryptionScopedAPI.md#).

