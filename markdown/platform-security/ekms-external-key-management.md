---
title: External Key Management Service
description: External Key Management Service \(EKMS\) enables you to integrate Field Encryption with your own external key management systems.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 4
breadcrumb: [Field Encryption, Encryption]
---

# External Key Management Service

External Key Management Service \(EKMS\) enables you to integrate Field Encryption with your own external key management systems.

External Key Management Service \(EKMS\) enables you to maintain direct control over the encryption keys that protect your data within the ServiceNow platform. Rather than storing keys within the infrastructure, you can generate, store, and manage them in a dedicated key management system. This approach permits you to adopt cloud-based enterprise services while maintaining control over your sensitive data.

You maintain authority over key lifecycle operations, including generation, rotation, and revocation allowing you to respond immediately to security events. This permits you to remove keys from your system, rendering your data cryptographically inaccessible.

## Supported providers

Currently, EKMS for Field Encryption supports AWS Key Management Service \(AWS KMS\). Future releases will include support for additional key management providers.

## Key limitations

-   Only one EKMS configuration can be created per instance.
-   Multi-region keys are not supported.
-   The AWS KMS key must be a symmetric key.

## How EKMS works

EKMS uses a key wrapping chain to secure data. See the EKMS key wrapping diagram below for a visual representation. When EKMS is configured:

1.  A Key Encryption Key \(KEK\) is generated in your instance. For EKMS, this key is called an External Key Encryption Key \(EKEK\).
2.  The EKEK is wrapped by an internal Instance Root Key \(IRK\), which is unique to your instance and stored securely in a ServiceNow-managed Hardware Security Module \(HSM\).
3.  The IRK-wrapped EKEK is then wrapped again by your AWS KMS key, which you manage in AWS.
4.  The wrapped EKEK is stored in the External Instance Keys table.
5.  Data Encryption Keys \(DEKs\) for a cryptographic module are wrapped by the EKEK and stored in the module key table. The DEKs are what encrypts your field data.
6.  Field data is encrypted using the cryptographic module's DEKs.

![External Key Management Service diagram](../image/ekms-diagram.png)This architecture ensures that your instance never has direct access to decrypt the data without access to the external AWS key.

## Key status synchronization

The EKMS Health Check background job runs every 30 minutes to synchronize the AWS key status with your instance. The synchronization ensures that key state changes in AWS \(enabled, disabled, pending deletion, deleted\) are reflected in the key's status in the EKMS configuration. Users with the security\_admin role can change this frequency by modifying the `com.glide.encryption.ekms.scheduler.health_check_interval`system property. See [Change synchronization frequency](../task/ekms-change-synchronization-frequency.md).

**Important:** AWS-deleted keys require a minimum of seven days before showing the deleted status, as this is controlled by AWS retention policies.

## Integration with Field Encryption Enterprise

EKMS integrates with Field Encryption Enterprise \(FEE\) through cryptographic modules. Cryptographic modules use your external AWS KMS key to wrap encryption keys, and Encrypted Field Configurations specify which data to encrypt.

## Access control

Module Access Policies \(MAPs\) determine which user roles can view encrypted data in clear text. Users without the proper role assignments will not be able to decrypt and view the protected information, even if they have access to the table.

## Get started

<table id="table_icw_nwv_f3c"><tbody><tr><td>

[Configuring External Key Management Service](ekms-configuring-external-key-management.md)

 [![](../../../reuse/icons/brand-icons/bus-sdlc.svg)](ekms-configuring-external-key-management.md)

 [Create and maintain Key Management components to customize and manage how cryptographic operations are performed on your ServiceNow instance.](ekms-configuring-external-key-management.md)

</td><td>

[External Key Management Service actions](ekms-using-external-key-management.md)

 [![](../../../reuse/icons/brand-icons/bus-optimize-manage.svg)](ekms-using-external-key-management.md)

 [Use EKMS to manage , revoke or rotate keys to secure sensitive data with the most up-to-date encryption materials and life cycle operations.](ekms-using-external-key-management.md)

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Activation information

To activate the External Key Management Service, you must first purchase a subscription to either Platform Encryption or ServiceNow Vault.

The ServiceNow Platform Encryption subscription bundle is a group commercial entitlement that includes Field Encryption Enterprise and Cloud Encryption.

Field Encryption Enterprise is the unlimited license of Field Encryption Starter. Field Encryption Enterprise is available with the activation of the com.glide.field.encryption.enterprise plugin. For details, see [Encryption and Key Management subscription bundle](../reference/encryption-sku.md).

Once you’ve installed the Field Encryption Enterprise plugin, install the EKMS plugin called “Platform Encryption External Key Management”. The plugin id is com.glide.encryption.external\_kms. See [Activate External Key Management Service](../task/ekms-activate-external-key-management.md) for more information.

-   **[Configuring External Key Management Service](ekms-configuring-external-key-management.md)**  
Set up External Key Management Service \(EKMS\) to control the encryption of your ServiceNow data using your Amazon Web Service Key Management System \(AWS KMS\).
-   **[Using External Key Management Service](ekms-using-external-key-management.md)**  
Manage and maintain your External Key Management Service \(EKMS\) configuration after initial setup

**Parent Topic:**[Field Encryption](field-encryption.md)

