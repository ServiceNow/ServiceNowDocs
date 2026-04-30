---
title: Password2 encryption with the Key Management Framework \(KMF\)
description: Supported by the Key Management Framework, use the Password2 \(2-way encrypted\) field type to encrypt and decrypt custom fields with segregation of duties, key protection, and life-cycle management. It works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Key Management Framework, Encryption]
---

# Password2 encryption with the Key Management Framework \(KMF\)

Supported by the Key Management Framework, use the Password2 \(2-way encrypted\) field type to encrypt and decrypt custom fields with segregation of duties, key protection, and life-cycle management. It works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.

Password2 is a text field that stores passwords with two-way encryption. The two-way encryption stores passwords as a secure encrypted value that can be decrypted within the instance.

**Tip:** Beginning in the Vancouver release, administrators can deprecate 3DES encryption on password2 fields in favor of the newer Advanced Encryption Standard \(AES\). For details, see [Deprecate GlideEncrypter usage of 3DES for password2 fields](password2-3des-deprecation.md).

## Activation

Password2 functionality is active by default. It’s controlled by the **glide.kmf.encrypter.enabled** property, which is set to **true** for all new instances and upgrades. You don’t need to enable Column Level Encryption Enterprise to use Password2.

## How Password2 works

The Key Management Framework provides a base system parent cryptographic module **cm\_glide\_encrypter**. This module provides a cryptographic specification and a key that can decrypt legacy Password2 fields.

![Cryptographic Module for Password2.](../image/cm_glide_encrypter.png "Cryptographic Module for Password2")

This cm\_glide\_encrypter module can have submodules, each with their own module key and specification. If a submodule is present with the same application scope as the application where the Password2 field is, the system uses the submodule. For example, if a table in the ServiceNow® Customer Service application has a submodule, and you write information to a Password2 field on a table in the Customer Service application scope, the cryptographic process calls the Customer Service submodule. The process also uses that submodule's key for encryption and decryption with a unique AES 256 GCM encryption key. One submodule per application scope is allowed. Parent module isn’t always used for global scope. Generally, new fields use instance\_level\_glide\_encrypter.

**Note:** You can’t create your own submodules in Xanadu. Submodules are provided in various application plugins on the ServiceNow AI Platform. You can rotate keys on submodules, but not the parent cm\_glide\_encrypter module.

## Domain separation and on-premise customers

KMF Password2 doesn’t support domain separation. You can use Password2 with on-premise instances.

## Legacy Password2 and the current Password2

In Xanadu, the existing Password2 field has been upgraded.

The current implementation of Password2:

-   Uses the Key Management Framework in accordance with [NIST 800-57](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57pt1r5.pdf) key wrapping guidelines and provides [FIPS 140-2-L3](https://csrc.nist.gov/publications/detail/fips/140/3/final) protection for the entire key hierarchy.
-   Includes capabilities to create dedicated and unique KMF Password2 submodules for specific applications, providing control through application scope. Each submodule has its own unique AES 256 GCM encryption key.

## Password2 fields in scripts

When accessing Password2 fields with a script, run the script under the same scope as the table scope. Use `setDisplayValue()` to encrypt Password2 values and `getDecryptedValue()` to decrypt and read the value.

**Note:** Don’t use the `GlideEncrypter()` API on Password2 fields.

This example script shows you how to encrypt `my@Password` in the password2 column of table 'table\_xyz'.

```

var  gr =  new GlideRecord(‘table_xyz’);
gr.pwd2column_name.setDisplayValue('my@Password');
 
gr.insert();

```

**Important:** You can’t use the `setValue()` API for the Password2 field.

This example script shows you how to decrypt the same field to retrieve the value:

```

var  gr =  new GlideRecord(‘table_xyz’);
gr.query();
gr.next();
var ge=gr.getElement('pwd2column_name');
var ged1 = ge.getDecryptedValue(); 

```

**Important:** The `getDecryptedValue()` API isn’t scoped. It’s available globally.

1.  When you encrypt data in a Password2 field, the system determines the scope of the application where the Password2 field resides.
2.  The system then looks for a submodule of the **cm\_glide\_encrypter** parent module with the same scope as the application if the property is set to **true**.

    **Note:** If a submodule with the same scope is present, it uses the submodule specification and key to perform the encryption.


This illustration explains how your instance decrypts data in Password2 fields:

![Password2 decryption flow.](../image/pw2_decryption_flow.png "Password2 decryption flow")

## KMF Password2 migration job

A migration job is provided for customers upgrading from previous releases. It takes data encrypted with a legacy Password2 encryption and re-encrypts it with the key in a KMF Password2 submodule key. The re-encryption only applies to tables with Password2 fields in application scopes that also have submodules created for that scope. For example, a legacy Password2 field in **XYZ\_example** application \(with **XYZ\_example** application scope\) is re-encrypted only if a submodule for the **XYZ\_example** application scope exists under the cm\_glide\_encrypter parent module.

The KMF Password2 encryption keys in the submodule are protected \(envelope encrypted\) in the KMF key hierarchy.

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

