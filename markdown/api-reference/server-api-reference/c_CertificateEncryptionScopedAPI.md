---
title: CertificateEncryption - Scoped
description: The CertificateEncryption API provides methods for encrypting certificates in scoped applications.Instantiates a CertificateEncryption object in a scoped application.Generates the Message Authentication Code \(MAC\), which is used to authenticate a message.Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from Trust Store Cert.Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from the keystore entry.Signs the data using the private key and the specified algorithm.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CertificateEncryption- Scoped

The CertificateEncryption API provides methods for encrypting certificates in scoped applications.

Use these methods to generate a hash for the certificate, sign data using a private key, and generate a message authentication code.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CertificateEncryption - CertificateEncryption\(\)

Instantiates a CertificateEncryption object in a scoped application.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## CertificateEncryption - generateMac\(String key, String algorithm, String data\)

Generates the Message Authentication Code \(MAC\), which is used to authenticate a message.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key to use to sign the message. Must be Base64 encoded.|
|algorithm|String|Algorithm to use to generate the MAC: HmacSHA256, HmacSHA1, HmacMD5, and so on.|
|data|String|Data to process.|

|Type|Description|
|----|-----------|
|String|MAC in base64 format.|

This example shows how to a MAC using sample\_key as the data and HmacSHA256 as the algorithm.

```
var mac = new CertificateEncryption;
var key = "sample_key"; 
key = gs.base64Encode(key);
mac.generateMac(key, "HmacSHA256", "sample_data");
```

## CertificateEncryption - getThumbPrint\(String certificateID, String algorithm\)

Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from Trust Store Cert.

|Name|Type|Description|
|----|----|-----------|
|certificateID|String|Sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.|
|algorithm|String|Algorithm to use to create the hash, such as SHA-1, SHA-256, and so on.|

|Type|Description|
|----|-----------|
|String|Thumbprint in base64 format.|

This example shows how to generate the thumbprint \(hash\) for the AzureAAD certificate.

```
//Create a GlideRecord to the certificate table
var x509GR = new GlideRecord('sys_certificate');

//If there is a certificate of a name of AzureAAD, get the certificate thumbprint
if(x509GR.get('name', 'AzureAAD')){

//Use the sys_id and algorithm we want to create a thumbprint
var thumbPrint = CertificateEncryption.getThumbPrint(x509GR.getUniqueValue(), "SHA-1");

//Print the created thumbprint
gs.print("Thumbprint for " + x509GR.getDisplayValue() + " is " + thumbPrint);
}
```

Output:

```
V1X+aguDBTZVVbWMGTXxdzJLmaY=
```

## CertificateEncryption - getThumbPrintFromKeyStore\(String certificateID, String alias, String algorithm\)

Generates a hash \(SHA-1, SHA-256, and so on\) for the certificate from the keystore entry.

|Name|Type|Description|
|----|----|-----------|
|certificateID|String|Sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.|
|alias|String|Alias name for the certificate.|
|algorithm|String|Algorithm to use to create the hash, such as SHA-1, SHA-256, and so on.|

|Type|Description|
|----|-----------|
|String|Thumbprint in base64 format.|

## CertificateEncryption - sign\(String certificateID, String alias, String aliaspassword, String algorithm, String datatosign\)

Signs the data using the private key and the specified algorithm.

<table id="table_edb_rmv_js" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

certificateID

</td><td>

String

</td><td>

sys\_id of the certificate record in the X.509 Certificate \[sys\_certificate\] table.

</td></tr><tr><td>

alias

</td><td>

String

</td><td>

Private key name.

</td></tr><tr><td>

aliaspassword

</td><td>

String

</td><td>

Password for the private key.

</td></tr><tr><td>

algorithm

</td><td>

String

</td><td>

Algorithm to use. Must be one of the following values:-   NONEwithRSA
-   MD2withRSA
-   MD5withRSA
-   SHA1withRSA
-   SHA224withRSA
-   SHA256withRSA
-   SHA384withRSA
-   SHA512withRSA
-   NONEwithDSA
-   SHA1withDSA
-   SHA224withDSA
-   SHA256withDSA
-   NONEwithECDSA
-   SHA1withECDSA
-   SHA224withECDSA
-   SHA256withECDSA
-   SHA384withECDSA
-   SHA512withECDSA

</td></tr><tr><td>

datatosign

</td><td>

String

</td><td>

Data to sign.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Signed data in base64 format.|

```
var ce = new CertificateEncryption;
ce.sign("recordID", "alias", "password", "SHA1withRSA", "sign this data");
```

