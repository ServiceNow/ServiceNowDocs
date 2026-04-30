---
title: Deprecate GlideEncrypter usage of 3DES for password2 fields
description: Deprecate GlideEncrypter usage of 3DES encryption standard on your instance ensure that your instance uses the more secure Advanced Encryption Standard \(AES\) exclusively for the encryption and decryption of your Password2 data.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework, Encryption]
---

# Deprecate GlideEncrypter usage of 3DES for password2 fields

Deprecate GlideEncrypter usage of 3DES encryption standard on your instance ensure that your instance uses the more secure Advanced Encryption Standard \(AES\) exclusively for the encryption and decryption of your Password2 data.

Beginning in Rome, password2 data is protected using the Key Management Framework, which uses the more modern Advanced Encryption Standard \(AES\) algorithm. However, some configurations and fallbacks in password2 logic can still use the 3DES algorithm for encryption and decryption.

In the Vancouver release, administrators can choose to deprecate the 3DES algorithm entirely. After completing this change, your instance uses AES encryption exclusively for all encryption and decryption tasks relating to password2 data. This change provides better instance security than compared with 3DES encryption, and is necessary to remain NIST compliant.

## Considerations before deprecation

-   **Transferring password2 data between instances**

    When transferring password2 encrypted texts to other instances, you must ensure that KMF Key Exchange is enabled between source and target instances. This configuration ensures that the keys used to encrypt password2 texts are available on both instances to decrypt the password2 encrypted texts. Before deprecating 3DES, Consider the following use cases that can impact password2 data between instances.

    -   If you have applications on your instance that use password2 data, ensure that KMF Resource Exchange is installed on that instance. KMF Resource Exchange ensures that instance level keys used to encrypt the password2 data on the source instance are available on the target instances for decryption. For more information, see [Key Management Framework Resource Exchange](../reference/resource-exchange.md).
    -   If you plan on exporting password2 data through XML or Data Sources, ensure that the target instance has KMF Key Exchange enabled. This configuration ensures that the instance level keys used to encrypt the password2 data on the source instance are available on the target instances for decryption. For details on this configuration, see [Key Management Framework Key Exchange](../reference/kmf-key-exchange-overview.md).

        **Important:** The examples above are more common scenarios, but if you’re using any other means of transferring password2 encrypted text between instances, you must configure KMF Resource Exchange to ensure the target instance can decrypt password2 data.

-   **Downgrading an instance after the 3DES deprecation**

    The following only applies for instances that have password2 fields have input lengths greater than 125 characters and you have already deprecated 3DES encryption.

    To downgrade an instance to release earlier than Vancouver via Instance Cloning, take the following steps before initiating the clone.

    1.  Check if data preservation is configured to preserve password2 field data.
    2.  If yes, then before requesting a clone, contact ServiceNow support to disable 3DES deprecation. In the **Reason** field, use “Clone downgrade pre-requisite for password2 support.”
-   **Legacy password2 fields**

    Your instance uses 3DES encryption to convert password2 data to legacy \(pre-Rome\) password2 data. After deprecating 3DES encryption, this option is no longer available. If you still need this feature, request partial deprecation \(see details in the next section\).


## How to deprecate 3DES

After you’ve reviewed the preceding use cases, enable either partial or complete deprecation depending on your needs. For either option, you can access the form to control deprecation by navigating to **All** &gt; **System Security** &gt; **Security Compliance** &gt; **Password2 Triple DES Deprecation**.

**Important:** You must elevate to security admin to see the **Security Compliance** module and perform these steps. For details on that process, see [Elevate to a privileged role](../../security/task/t_ElevateToAPrivilegedRole.md).

![Password2 Triple DES Deprecation form](../image/3des-form.png)

The **Password2 Triple DES Deprecation** form contains information on the process for both complete and partial 3DES deprecation. Select the options for complete or partial deprecation and select **Save**.

-   **Complete deprecation**

    Enabling complete deprecation removes the usage of 3DES for all the password2 fields in your instance. If all the prerequisites are met, then there are no configuration or scenarios where 3DES is used in password2 fields.

    To enable complete deprecation:

    -   Select **Do you want to opt-in for 3DES deprecation for password2 fields?**
    -   De-select **Do you want to continue using 3DES in legacy password2 fields?**
-   **Partial deprecation**

    Enabling partial deprecation removes the usage of 3DES for all the password2 fields except legacy configured fields. Legacy configuration password2 fields continue to use 3DES encryption. Select this option only when you must continue to use 3DES for legacy configured fields.

    To enable partial deprecation:

    -   Select **Do you want to opt-in for 3DES deprecation for password2 fields?**
    -   Select **Do you want to continue using 3DES in legacy password2 fields?**

## After GlideEncrypter deprecation

After the deprecation process is complete, the following information applies to your instance.

-   password2 fields still support decryption \(but not encryption\) of 3DES encrypted data.
-   Existing 3DES encrypted data in password2 fields remain as is until the field value is updated by a user or workflow.
-   Any update to the value of a password2 field removes 3DES encrypted text and replaces it with the text encrypted by KMF using AES.
-   In some situations, your instance may display an error when saving password data:

    `Action Aborted: Password value cannot be saved due to technical issue. Please see KB1296997 for help.`

    If you see this error refer to support information in knowledge base article [KB1296997](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1296997).


**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

