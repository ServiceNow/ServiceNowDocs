---
title: Cryptographic summary fields
description: The fields displayed in the Cryptographic summary of an asset vary by asset type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/cryptographic-summary-fields.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-07-25"
reading_time_minutes: 1
breadcrumb: [Reference, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Cryptographic summary fields

The fields displayed in the Cryptographic summary of an asset vary by asset type.

## Certificate

|Field|Description|
|-----|-----------|
|Quantum resistant|Whether the certificate uses a quantum-resistant algorithm.|
|Algorithm|Signing algorithm of the certificate, such as SHA1withRSA.|
|Key strength|Size of the key in bits.|
|Hash function|Hash function used by the certificate, such as SHA-384.|

## AWS KMS key

|Field|Description|
|-----|-----------|
|Object ID|Unique identifier of the key.|
|Key usage|Cryptographic operations the key supports.|
|Key state|Current state of the key in AWS KMS.|
|Origin|Source of the key material.|
|MAC algorithms|Message Authentication Code \(MAC\) algorithms associated with the key.|
|Key ID|Identifier of the key in AWS KMS.|
|Multi region|Whether the key is a multi-region key.|
|Multi region key type|Type of multi-region key, such as primary or replica.|

## Azure Key Vault key

|Field|Description|
|-----|-----------|
|Object ID|Unique identifier \(URI\) of the key in Azure Key Vault.|
|Key type|Type of cryptographic key, such as RSA.|
|Key size|Size of the key in bits.|
|Curve|For elliptic curve fields the elliptic curve of the key.|
|Algorithm|Cryptographic algorithm associated with the key.|
|Key operations|Operations the key can perform, such as encryption and decryption.|
|Enabled|Whether the key is enabled in the source.|
|Recovery level|Azure Key Vault recovery level, which indicates whether the key can be recovered or is purge able after deletion.|
|Vault URI|URI of the Azure key vault that stores the key.|

