---
title: KMFCryptoOperation - Scoped, Global
description: The KMFCryptoOperation class provides methods for performing cryptographic operations using a Key Management Framework \(KMF\) cryptographic module or a Field Encryption encryption module.Creates a KMFCryptoOperation object for the specified module and operation.Performs the cryptographic operation defined by the current KMFCryptoOperation object on the supplied data and returns the result.Sets the additional input needed to perform the cryptographic operation.Sets the algorithm associated with the key material to wrap.Sets the data format for the input data on which the cryptographic operation will be performed. Uses the specified format when decoding the data.Sets the data format of the output data that is returned by the cryptographic operation. Uses the specified format when encoding the data.Sets the data type for the output data returned after the cryptographic operation is performed.Sets the sys\_id of the key to wrap on the KMFCryptoOperation object. Applicable to symmetric and asymmetric wrapping of keys.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# KMFCryptoOperation - Scoped, Global

The KMFCryptoOperation class provides methods for performing cryptographic operations using a Key Management Framework \(KMF\) cryptographic module or a Field Encryption encryption module.

To use this API, you must have already created and configured a KMF cryptographic module or a CLE encryption module. The module must have one or more cryptographic specifications and you must create or import its associated key. For details, see [Cryptographic modules](https://www.servicenow.com/docs/access?context=crypto-module-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

The KMFCryptoOperation object generated using this API represents a cryptographic operation, such as a Symmetric Encryption. Use the KMFCryptoOperations\(\) method to create this object, the builder methods to set properties on the object, and the doOperation\(\) method to execute the operation.

You can use this API in both scoped and global applications. You must always specify the `sn_kmf_ns` namespace when calling this API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## KMFCryptoOperation - KMFCryptoOperation\(String cryptoModuleName, String operationName\)

Creates a KMFCryptoOperation object for the specified module and operation.

This API leverages builder methods. Builder methods update properties on the KMFCryptoOperation object, such as changing the desired output format of the data. Not all builder methods are valid for all operations. The builder methods available for each operation are noted in the parameters table below.

The following builder methods are valid for all operation types:

-   [withInputFormat\(\)](KMFCryptoOperationBothAPI.md#)
-   [withOutputFormat\(\)](KMFCryptoOperationBothAPI.md#)
-   [withOutputType\(\)](KMFCryptoOperationBothAPI.md#)

**Important:** Base64 input values used in this document must be URL safe \(contains only A-Z, a-z, 0-9, dash\( - \) and underscore\( \_ \) characters\).

<table id="table_mth_p3t_tnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cryptoModuleName

</td><td>

String

</td><td>

Name of the Key Management Framework \(KMF\) cryptographic module or Field Encryption encryption module to use. You must create the module before calling this method. For details, see [Cryptographic module overview](https://www.servicenow.com/docs/access?context=crypto-module-overview&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

operationName

</td><td>

String

</td><td>

Name of the operation to perform.Valid values \(not case-sensitive\):

-   ASYMMETRIC\_DECRYPTION: Data decryption using an asymmetric-key algorithm. Requires a KMF cryptographic module with an Asymmetric Data Decryption cryptographic purpose.
    -   Additional builder methods: withAdditionalInput\(\)
    -   Default input format: Formatted - Formatted to the KMF specifications
    -   Default output format: KMFBase64 - Base64 encoded
    -   Default output type: String
-   ASYMMETRIC\_ENCRYPTION: Data encryption using an asymmetric-key algorithm. Requires a KMF cryptographic module with an Asymmetric Data Encryption cryptographic purpose.
    -   Additional builder methods: withAdditionalInput\(\)
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String . Output can also be an [KMFEncryptionPayload](KMFCryptoOperationBothAPI.md#KMFEncryptionPayload) object. RSA and EC-IES are compatible with both. For additional information on the KMFEncryptionPayload object, see [withAdditionalInput\(\)](KMFCryptoOperationBothAPI.md#KMFEncryptionPayload).
-   ASYMMETRIC\_UNWRAPPING: Key unwrapping using an asymmetric-key algorithm. Requires a KMF cryptographic module with an Asymmetric Key Unwrapping cryptographic purpose.
    -   Additional builder methods: withAlgorithm\(\)
    -   Default input format: Formatted - Formatted to the KMF specifications
    -   Default output format: KMFBase64 - Base64 encoded
    -   Default output type: String
-   ASYMMETRIC\_WRAPPING: Key wrapping using an asymmetric-key algorithm. Requires a KMF cryptographic module with an Asymmetric Key Wrapping cryptographic purpose.
    -   Additional builder methods: withAlgorithm\(\), withSysId\(\)
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String
-   MAC\_GENERATION: Generation of a Message Authentication Code \(MAC\). Symmetric-key algorithm based to provides data integrity and authentication. Requires a KMF cryptographic module with a Symmetric Authenticity cryptographic purpose.
    -   Additional builder methods: None
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String
-   MAC\_VERIFICATION: Verification of a MAC. Symmetric-key algorithm based to provide data integrity and authentication. Requires a KMF cryptographic module with a Symmetric Authenticity cryptographic purpose.
    -   Additional builder methods: withAdditionalInput\(\)
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: KMFNone - No decoding
    -   Default output type: Boolean
-   SIGNATURE\_GENERATION: Generation of a digital signature. Asymmetric-key algorithm based to provide data integrity and authentication. Requires a KMF cryptographic module with a Signature Generation cryptographic purpose.
    -   Additional builder methods: None
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String
-   SIGNATURE\_VERIFICATION: Verification of a digital signature. Asymmetric-key algorithm based to provide data integrity and authentication. Requires a KMF cryptographic module with a Signature Verification cryptographic purpose.
    -   Additional builder methods: withAdditionalInput\(\)
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: KMFNone - No decoding
    -   Default output type: Boolean
-   SYMMETRIC\_ENCRYPTION: Data encryption using a symmetric-key algorithm. If the algorithm is not equality preserving, only formatted output is allowed. Requires a KMF cryptographic module with a Symmetric Data Encryption/Decryption cryptographic purpose.
    -   Additional builder methods: None
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String
-   SYMMETRIC\_DECRYPTION: Data decryption using a symmetric-key algorithm. If the algorithm is not equality preserving, KMFBase64 input is allowed. Requires a KMF cryptographic module with a Symmetric Data Encryption/Decryption cryptographic purpose.
    -   Additional builder methods: None
    -   Default input format: Formatted - Formatted to the KMF specifications
    -   Default output format: KMFBase64 - Base64 encoded
    -   Default output type: String
-   SYMMETRIC\_WRAPPING: Key wrapping using a symmetric-key algorithm. If the algorithm is not equality preserving, only formatted output is allowed. Requires a KMF cryptographic module with a Symmetric Key Wrapping/Unwrapping cryptographic purpose.
    -   Additional builder methods: withAlgorithm\(\) and withSysId\(\)
    -   Default input format: KMFBase64 - Base64 encoded
    -   Default output format: Formatted - Formatted to the KMF specifications
    -   Default output type: String
-   SYMMETRIC\_UNWRAPPING: Key unwrapping using a symmetric-key algorithm. If the algorithm is not equality preserving, KMFBase64 input is allowed. Requires a KMF cryptographic module with a Symmetric Key Wrapping/Unwrapping cryptographic purpose.
    -   Additional builder methods: withAlgorithm\(\)
    -   Default input format: Formatted - Formatted to the KMF specifications
    -   Default output format: KMFBase64 - Base64 encoded
    -   Default output type: String

</td></tr></tbody>
</table>This example instantiates a KMFCryptoOperation object for the module global.sj\_cm to perform a Symmetric Encryption operation. You must include the namespace for both global and scoped applications.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SYMMETRIC_ENCRYPTION"); 
```

This example shows how to specify options to update the default output type and output format.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SYMMETRIC_ENCRYPTION")
  .withOutputType("STRING").withOutputFormat("FORMATTED");

var cipherText=op.doOperation("hi");
```

This example shows how to perform an Asymmetric Encryption operation using an Integrated Encryption Scheme \(EC-IES\). Note that long values, such as **signature**, have been truncated and replaced with an ellipse for readability.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","ASYMMETRIC_ENCRYPTION")
.withInputFormat("KMFNONE")
.withOutputType("PAYLOAD");

var cipherText = op.doOperation("hi");

/*
cipherText contains an object similar to this JSON: {
  "signature": "pkg…",
  "ephemeral_key": "BDi…",
  "ciphertext": "afFS…"
}
*/

```

This example shows how to perform an Asymmetric Decryption operation using EC-IES.

```
var op = new 
sn_kmf_ns.KMFCryptoOperation("global.sj_cm","ASYMMETRIC_DECRYPTION")
  .withAdditionalInput({
  "signature": "pkg… ",
  "ephemeral_key": "BDi…"
})
.withOutputFormat("KMFNONE");

var clearText = op.doOperation("afFS…");

```

## KMFCryptoOperation - doOperation\(Object data\)

Performs the cryptographic operation defined by the current KMFCryptoOperation object on the supplied data and returns the result.

|Name|Type|Description|
|----|----|-----------|
|data|Object|Required except if the withSysId\(\) builder method has previously been called on the associated KMFCryptoOperation object. Input data on which to perform the cryptographic operation.|

<table id="table_th4_4sl_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Depends on the operation type. -   **MAC\_VERIFICATION** and **SIGNATURE\_VERIFICATION**: Boolean
-   All others: String

</td><td>

Data results after performing the operation specified in the associated KMFCryptoOperation object.

</td></tr></tbody>
</table>This example uses the doOperation\(\) to create a MAC.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","MAC_GENERATION"); 
var data = "aGk="; 
var mac = op.doOperation(data);
```

## KMFCryptoOperation - withAdditionalInput\(Object additionalInput\)

Sets the additional input needed to perform the cryptographic operation.

For example, during a Message Authentication Code \(MAC\) verification, use this method to pass in the generated MAC tag. Similarly, during signature verification, use it to pass in the signature. You can also use this method to pass additional data, a KMFEncryptionPayload object, when performing an asymmetric operation with an integrated cipher, such as Elliptic Curve Integrated Encryption Scheme \(EC-IES.\)

**Note:** The additional input does not have to be in the same format that is currently set on the KMFCryptoOperation object.

<table id="table_exs_fhl_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additionalInput

</td><td>

String or Object

</td><td>

Optional, except for Asymmetric Decryption operations when using EC-IES. Additional input data needed to perform the cryptographic operation specified in the KMFCryptoOperation object.Supported string formats:

-   FORMATTED: Formatted to the Key Management Framework \(KMF\) specifications.
-   KMFBASE64: Base64 encoded.

 KMFEncryptionPayload object format:

 ```
{
  "ciphertext": String,
  "derivation_secret": String,
  "ephemeral_key": String,
  "ephemeral_key_format": String,
  "signature": String
}
```

</td></tr><tr><td>

additionalInput.ciphertext

</td><td>

String \(Base64\)

</td><td>

Required for Asymmetric Decryption, optional for all other operations.Valid values:

-   If using an RSA algorithm: RSA ciphertext
-   If using an EC-IES algorithm: Integrated AES ciphertext

 Available from the Asymmetric Encryption operation when the output type is set to **payload**.

</td></tr><tr><td>

additionalInput.derivation\_secret

</td><td>

String \(Base64\)

</td><td>

Optional, only used for the Asymmetric Encryption or Asymmetric Decryption operations with EC-IES. Shared secret to use during the key derivation process of the integrated scheme.

</td></tr><tr><td>

additionalInput.ephemeral\_key

</td><td>

String \(Base64\)

</td><td>

Required for the Asymmetric Decryption operation when using EC-IES, optional for all other operations. Ephemeral public key to use during the basic agreement process of the integrated scheme.Available from the Asymmetric Encryption operation when the output type is set to **payload**.

</td></tr><tr><td>

additionalInput.ephemeral\_key\_format

</td><td>

String

</td><td>

Optional, only used for the Asymmetric Encryption or Asymmetric Decryption operations with EC-IES. Overrides the format of the public key represented by the **ephemeral\_key** parameter.Valid values:

-   x962
-   der

</td></tr><tr><td>

additionalInput.signature

</td><td>

String \(Base64\)

</td><td>

Required for the Asymmetric Decryption operation with EC-IES, optional for all others. The signature of the ciphertext to validate using the signature verification process of the integrated scheme.Available from the Asymmetric Encryption operation when the output type is set to **payload**.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withAdditionalInput\(\) to add a string-based signature to the KMFCryptoOperation object.

```
var signature = "John Doe";
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SIGNATURE_VERIFICATION")
  .withAdditionalInput(signature);

var value = GlideStringUtil.base64Encode("Text to encode"); // Default input format is KMFBase64
var result = op.doOperation(String(value));
```

This example uses withAdditionalInput\(\) to add a signature and ephemeral key to the KMFCryptoOperation object. Note that long values, such as those in the doOperation\(\) call and **payload** description, have been truncated and replaced with an ellipse for readability.

```
var payload = new sn_kmf_ns.KMFEncryptionPayload();
payload.signature = "pkg...";
payload.ephemeral_key = " BDi...";
payload.ephemeral_key_format = "x962";

var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","ASYMMETRIC_DECRYPTION")
  .withAdditionalInput(payload)
  .doOperation("afFS...";

```

## KMFCryptoOperation - withAlgorithm\(String algorithm\)

Sets the algorithm associated with the key material to wrap.

<table id="table_kx1_r4l_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

algorithm

</td><td>

String

</td><td>

Algorithm to use.Valid values:

-   AES: Symmetric key type
-   EC: Asymmetric key type
-   HMAC: Symmetric key type
-   RSA: Asymmetric key type

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withAlgorithm\(\) to change the encryption algorithm used to EC.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","ASYMMETRIC_WRAPPING").withAlgorithm("EC");
var value = GlideStringUtil.base64Encode("Sample key"); // Default input format is KMFBase64
var result = op.doOperation(String(value));
```

## KMFCryptoOperation - withInputFormat\(String inputFormat\)

Sets the data format for the input data on which the cryptographic operation will be performed. Uses the specified format when decoding the data.

<table id="table_lvd_kxk_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputFormat

</td><td>

String

</td><td>

Format of the input data.Valid values:

-   FORMATTED: Formatted to the Key Management Framework \(KMF\) specifications.
-   KMFBASE64: Base64 encoded.
-   KMF\_GLIDE\_ENCRYPTER\_FORMATTED: Support decryptions of both KMF encrypted values and GlideEncrypter encrypted values.
-   KMFNONE: No encoding.

Default: Value determined by the operation specified when the KMFCryptoOperation object was instantiated. For more information, see [KMFCryptoOperation - KMFCryptoOperation\(String cryptoModuleName, String operationName\)](KMFCryptoOperationBothAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withInputFormat\(\) to change the input format to have no encoding.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SYMMETRIC_ENCRYPTION").withInputFormat("KMFNone");
var result = op.doOperation("Text with no encoding"); // Pass in unencrypted String
```

This example uses withInputFormat\(\) to change the input format to KMF\_GLIDE\_ENCRYPTER\_FORMATTED.

```
var encryptOp = new sn_kmf_ns.KMFCryptoOperation("<module_name>", "SYMMETRIC_DECRYPTION")
 .withInputFormat("KMF_GLIDE_ENCRYPTER_FORMATTED")
 .withOutputFormat("KMFNone"); 

var clear_text = encryptOp.doOperation(<encrypted_text>);
```

## KMFCryptoOperation - withOutputFormat\(String outputFormat\)

Sets the data format of the output data that is returned by the cryptographic operation. Uses the specified format when encoding the data.

<table id="table_ezl_gdl_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

outputFormat

</td><td>

String

</td><td>

Format of the output data.Valid values:

-   FORMATTED: Formatted to the Key Management Framework \(KMF\) specifications.
-   KMFBASE64: Base64 encoded.
-   KMFNONE: No decoding. Only supported for MAC\_VERIFICATION and SIGNATURE\_VERIFICATION.

 Default if this method is not called: Value determined by the operation specified when the KMFCryptoOperation object was instantiated. For more information, see [KMFCryptoOperation - KMFCryptoOperation\(String cryptoModuleName, String operationName\)](KMFCryptoOperationBothAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withOutputFormat\(\) to set the output format of the decryption to KMFNone \(default is KMFBase64.\)

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SYMMETRIC_DECRYPTION").withOutputFormat("KMFNone");
var clear_data = op.doOperation(<FORMATTED_data>); // Pass in default of FORMATTED data
```

## KMFCryptoOperation - withOutputType\(String outputType\)

Sets the data type for the output data returned after the cryptographic operation is performed.

**Note:** When you instantiate the KMFCryptoOperation object for **MAC\_VERIFICATION** or **SIGNATURE\_VERIFICATION** operations, you must also call this method, passing boolean, to set the correct output type or an exception is thrown when you execute the operation.

<table id="table_h5z_31l_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

outputType

</td><td>

String

</td><td>

Type of output data.Not all output types are applicable to all operations. For an unsupported type, an exception is thrown.

 Valid values \(not case-sensitive\):

-   String: Not valid for **MAC\_VERIFICATION** or **SIGNATURE\_VERIFICATION** operations.
-   Boolean: Only valid for **MAC\_VERIFICATION** or **SIGNATURE\_VERIFICATION** operations.
-   Payload: Only valid for the **ASYMMETRIC\_ENCRYPTION** operation. Use this output type for EC-IES.

 **Note:** When specifying an output of `Payload`, the output of the doOperation\(\) method is a KMFEncryptionPayload object. For more information on the structure of this object, see [withAdditionalInput\(\)](KMFCryptoOperationBothAPI.md#KMFEncryptionPayload).

 Default: Value determined by the operation, specified when the KMFCryptoOperation object was instantiated. For more information, see [KMFCryptoOperation - KMFCryptoOperation\(String cryptoModuleName, String operationName\)](KMFCryptoOperationBothAPI.md#).

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withOutputType\(\) to set the output type for MAC\_VERIFICATION to Boolean.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","MAC_VERIFICATION")
  .withOutputType("Boolean").withAdditionalInput(<MAC>);
var value = GlideStringUtil.base64Encode("Text to sign"); // Default input type is KMFBase64
var result = op.doOperation(String(value));
```

## KMFCryptoOperation - withSysId\(String sysId\)

Sets the sys\_id of the key to wrap on the KMFCryptoOperation object. Applicable to symmetric and asymmetric wrapping of keys.

<table id="table_ymp_jnl_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysId

</td><td>

String

</td><td>

Sys\_id of the key to wrap.Table: Module Key \[sys\_kmf\_module\_key\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses withSysId\(\) to define the key to wrap.

```
var op = new sn_kmf_ns.KMFCryptoOperation("global.sj_cm","SYMMETRIC_WRAPPING").withSysId("0d06ce525b231010f86d1b341d81c777");
var wrappedKey = operation.doOperation(); // No need to pass data when using withSysId()
```

