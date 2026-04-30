---
title: Cryptographic specification
description: The Cryptographic specification is the component that defines aspects of your cryptographic module, including its cryptographic purpose and which encryption algorithm to use.
locale: en-US
release: yokohama
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring the Key Management Framework, Key Management Framework, Encryption]
---

# Cryptographic specification

The Cryptographic specification is the component that defines aspects of your cryptographic module, including its cryptographic purpose and which encryption algorithm to use.

Cryptographic specifications can be tailored to a specified cryptographic purpose, covering both asymmetric and symmetric key-based cryptographic operations. Selection of a cryptographic purpose offers further choices, namely to a set of supported algorithms and key length configurations.

|Cryptographic Purpose|Algorithm|Key Information|
|---------------------|---------|---------------|
|Asymmetric Data Decryption|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Asymmetric Data Encryption|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Asymmetric Key Unwrapping|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Asymmetric Key Wrapping|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Signature Generation|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Signature Verification|RSA|Asymmetric – 2048-bit, 3072-bit, and 4096-bit key|
|Symmetric Authenticity|HMAC|Symmetric – 256-bit, 384-bit, and 512-bit key|
|Symmetric Data Encryption/Decryption\*|AES-CBC \*|Symmetric – 128-bit, 192-bit, 256-bit key|
|AES-CFB|
|AES-OFB|
|AES-CTR|
|AES-GCM \*\*|
|Symmetric Key Wrapping/Unwrapping\*|AES-CBC \*|Symmetric – 128-bit, 192-bit, 256-bit key|
|AES-CFB|
|AES-OFB|
|AES-CTR|
|AES-GCM \*\*|

\* AES-CBC supports equality-preserving options.  Field Encryption Enterprise utilizes AES-CBC.

\*\* AES-GCM has built-in data integrity.

The configuration of these parameters is covered in [Create a cryptographic module](../task/create-cryptographic-module.md).

**Parent Topic:**[Exploring the Key Management Framework](../../encryption/concept/explore-kmf.md)

