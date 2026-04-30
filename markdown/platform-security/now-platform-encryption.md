---
title: Field Encryption Enterprise
description: Field Encryption Enterprise uses the Key Management Framework \(KMF\) to enable you to customize and manage how fields and attachments are encrypted and decrypted on your instance. A subscription is required to use Field Encryption Enterprise.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-12-02"
reading_time_minutes: 8
breadcrumb: [Encryption]
---

# Field Encryption Enterprise

Field Encryption Enterprise uses the Key Management Framework \(KMF\) to enable you to customize and manage how fields and attachments are encrypted and decrypted on your instance. A subscription is required to use Field Encryption Enterprise.

**Important:** This topic covers the enterprise version of Field Encryption. For information on the standard version of Field Encryption, or to learn the differences between the two versions, see [Exploring Field Encryption](../../encryption/concept/exploring-fe.md).

Field Encryption Enterprise is premised with Field Encryption and uses the Key Management Framework and its full support of key management functions. Field Encryption Enterprise provides key-protection and key life-cycle management for application-level field encryption. All keys are protected with a key-wrapping hierarchy ultimately rooted in FIPS \(Federal Information Processing Standards\) 140-2-L3 Hardware Security Modules \(HSM\).

Field Encryption Enterprise gives you the ability to manage how supported fields are encrypted and decrypted in accordance with [NIST 800-57](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57pt1r5.pdf) practices. It also uses the most updated version of field-level encryption, including integration for proper key protection and management.

Specifically, Field Encryption Enterprise uses the KMF encryption modules, granting you more control of server-side encryption. KMF verifies proper data encryption key protection using key hierarchy and envelope encryption. Your instance encrypts data through cryptographic modules that you configure. You can create an access policy for each module then configure cryptographic specifications and access policies and control key life-cycle management control.

Field Encryption Enterprise supports module access policies based on:

-   Scope
-   Role
-   Script
-   Resource Exchange
-   System User

See [Create a module access policy](../../key-management-framework/task/create-module-access-policy.md) for additional information.

**Note:** For details on the supported features of Field Encryption and how to upgrade and subscribe to the Field Encryption Enterprise entitlement refer to [Encryption and Key Management subscription bundle](../../encryption/reference/encryption-sku.md).

## Encryption terms

<table id="table_ddr_sgb_54b"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Key management](../../key-management-framework/image/keys-on-ring.png "Key management")

</td><td>

Support for key managementFundamental to Field Encryption Enterprise is the Key Management Framework \(KMF\).

 Gain the following capabilities:

-   Key life-cycle management.
-   Key rotation. See [Rotate keys](../../encryption/task/rotate-cust-supplied-keys.md) for details.
-   Key protection and key generation with FIPS 140-2-L3 Hardware Security Modules \(HSMs\).
-   Segregation of roles and duties.
-   The secure transfer of data encryption keys between instances, such as production and non-production instances.
-   Customer Supplied Keys \(CSK\) with key-wrapping.
-   Non-deterministic encryption.
-   Mass encryption/decryption.
-   Auditing of key access/use.

 See [Key Management Framework Reference](../../key-management-framework/concept/understanding-kmf.md) for details.

</td></tr><tr><td>

![Customer-supplied key](../../key-management-framework/image/keys-on-ring-csk-icon.png "Customer-supplied key")

</td><td>

Support for customer supplied keysOne of the biggest benefits of Field Encryption Enterprise is that you can use your own keys for encryption. Administrators have the choice to use ServiceNow supplied keys or your own customer-supplied keys \(CSK\) for encryption on the ServiceNow AI Platform®.

 You can also manage the key life cycle and decide when to revoke, rotate, and inactivate the keys. After you enable customer-supplied keys and create a cryptographic module, you download a token and public ephemeral key. You use the token and public key to wrap your key and then upload to the instance. To use customer-supplied keys, see [Configure field encryption settings to select key type](../../key-management-framework/task/configure-field-encryption-settings.md) and [Using customer supplied keys with Field Encryption Enterprise](../../encryption/concept/csk-landing.md).

</td></tr><tr><td>

![Field Encryption](../../key-management-framework/image/lock-locked.png "Field Encryption")

</td><td>

Support for both field encryption and attachment encryptionBoth field encryption and attachment encryption use cryptographic modules and access policies through Encrypted Field Configurations. The Encrypted Field Configuration form is used to choose an encryption type of column or attachment encryption. See [Set encrypted field configurations](../../encryption/task/set-encrypted-field-config.md) for more information and supported field types.

</td></tr><tr><td>

![Non-deterministic encryption](../../key-management-framework/image/non-deterministic-encryption.png "Non-deterministic encryption")

</td><td>

Support for non-deterministic encryptionField Encryption Enterprise supports non-deterministic encryption for enhanced security. If the system encrypts the same data more than once, the ciphertexts are different each time. Non-deterministic encryption is available with Advanced Encryption Standard \(AES\) encryption with Cipher Block Chaining \(CBC\).

 You can enable this feature through the Equality Preserving option on the Algorithm Definition stage of the cryptographic specification. Create a cryptographic specification for a crypto module and define an algorithm for encryption and generate the key.

 See [Create a cryptographic module](../../key-management-framework/task/create-cryptographic-module.md) to define the mechanisms used for cryptographic operations and for more information on enabling non-deterministic encryption.

</td></tr><tr><td>

![Resource Exchange](../../key-management-framework/image/resource-exchange.png "Resource Exchange")

</td><td>

Resource Exchange Field Encryption Enterprise keys instance to instance in a secure manner using the KMF cryptographic APIs to provide confidentiality, integrity, authentication, and non-repudiation. Resource Exchange is a KMF feature that gives you the capability to exchange resources between instances in a secure manner. See [Key Management Framework Resource Exchange](../../key-management-framework/reference/resource-exchange.md) for details.

</td></tr></tbody>
</table>**Note:** If you choose not to activate Field Encryption Enterprise, you can still use Field Encryption. See [Exploring Field Encryption](../../encryption/concept/exploring-fe.md) for information.

Field Encryption Enterprise supports on-premise customers. It doesn’t support Domain Separation.

## Support for additional encrypted fields

The standard version of Field Encryption is limited to five encrypted columns. Field Encryption Enterprise supports an unlimited number of encrypted columns.

## Supported field information

The following field types can be encrypted:

-   Attachments
-   Date
-   Date/Time
-   Email
-   HTML
-   Journal
-   Journal Input
-   Journal List
-   Phone
-   String text
-   Translated Field
-   Translated HTML
-   Translated Text
-   URL

## Attachment Encryption

-   **Attachment encryption by default**

    Customers using Field Encryption have attachments encrypted by default in tables that have an active Encrypted Field Configuration \(EFC\) type of **Attachment**.

    This default encryption defined by the EFC configuration means that admins don’t need to manually declare that an attachment should be encrypted on upload for these tables.

-   **Administrators can disallow users from attaching unencrypted files**

    For details, see [Prevent users from attaching unencrypted files](../../encryption/task/attach-enc-property.md).

-   **Opt out of default encryption**

    If you don’t want attachments encrypted by default based on EFC configuration, you can opt out of this option by contacting ServiceNow support.

    To opt out of this feature, create a support case with ServiceNow support, and include this statement in a comment on the case record:

    `"I [customer name], understand that I am asking ServiceNow to turn off a recommended security best practice for attachments, and that [customer company] assumes any additional risk related to their configuration and use of unencrypted attachments in the ServiceNow application."`


## API support

Field Encryption Enterprise enables the following APIs.

**Note:** The API behavior described in the following table represents the default configuration for the latest base system package. If you are working with older package versions, you may experience different functionality.

<table id="table_jns_p3m_mhc"><thead><tr><th>

API

</th><th>

Description

</th><th>

Parameters

</th><th>

Return type

</th></tr></thead><tbody><tr><td>

``changeEncryptionContext()``

</td><td>

Updates an active Encryption Context \(EC\) used to encrypt an attachment. When CLE is enabled with the CLE Starter plugin using KMF Crypto Module \(CM\), the API locates the CM for the EC and uses it to encrypt the attachment.

**Note:** This API is only available in the Global scope.

</td><td>

-   sourceTable – Name of table that has the attachment.
-   sourceID – Table record system id.
-   attachmentID – The sys\_attachment record system id.
-   newEncryptionContextID - System ID of the new context.

</td><td>

Boolean

</td></tr><tr><td>

`changeCryptoModule()`

</td><td>

Updates an active encryption module used to encrypt an attachment.**Note:** This API is only available in the Global scope.

</td><td>

-   sourceTable – Name of table that has the attachment.
-   sourceID – Table record system id.
-   attachmentID – The sys\_attachment record system id.
-   newCryptoModuleId - System ID of the new encryption module to encrypt the attachment.

</td><td>

Boolean

</td></tr><tr><td>

`disableEncryption()`

</td><td>

Disable active encryption on an attachment.

</td><td>

-   sourceTable – Name of table that contains the attachment.
-   sourceID – Table record system id.
-   attachmentID – The sys\_attachment record system id.

</td><td>

Boolean

</td></tr><tr><td>

`getDisplayValue()`

</td><td>

Returns the cleartext display value of an encrypted field.

</td><td>

 

</td><td>

String

</td></tr><tr><td>

`getValue()`

</td><td>

Returns the cleartext value of an ecrypted field when glide\_encryption.set\_value\_support\_cle.disabled is false \(requires Module Access Policy \(MAP\)\). Returns the encrypted value of an encrypted field when glide\_encryption.set\_value\_support\_cle.disabled is true.

</td><td>

 

</td><td>

String

</td></tr><tr><td>

`setDisplayValue()`

</td><td>

Inserts encrypted data into an encrypted field for display purposes.

</td><td>

-   name – Field name.
-   value – Field value.

</td><td>

Boolean

</td></tr><tr><td>

`setValue()`

</td><td>

Inserts encrypted data into an encrypted field, controlled by a system property. Encrypts data when glide\_encryption.set\_value\_support\_cle.disabled is false \(requires MAP\); writes unencrypted data when set to true \(no MAP required\), when glide\_encryption.set\_value\_support\_cle.disabled is true.

</td><td>

-   name – Field name.
-   value – Field value.

</td><td>

Boolean

</td></tr></tbody>
</table>The following script illustrates API changes when the Incident short description is encrypted:

```

var gr = new GlideRecord('incident'); //creates a new incident
gr.setValue('short_description','test123'); //sets the value to **test123**
var sys_ID = gr.insert(); //inserts the record in the Incident table.
gs.info(gr.getValue('short_description')); //displays the unencrypted value

```

When the Field Encryption plugin is installed, `glide_encryption.set_value_support_cle.disabled` is set to false by default.

**Parent Topic:**[Encryption](../../security/concept/encryption-landing.md)

