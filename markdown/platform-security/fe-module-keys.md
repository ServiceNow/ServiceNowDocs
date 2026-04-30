---
title: Module keys for Field Encryption
description: The Module Keys tab shows you summary level information about your Field Encryption Data Encryption Key\(s\). You can view the Key alias, Key type, Algorithm, Key lifecycle state, and Key version.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Module keys for Field Encryption

The Module Keys tab shows you summary level information about your Field Encryption Data Encryption Key\(s\). You can view the Key alias, Key type, Algorithm, Key lifecycle state, and Key version.

## Accessing module key information

Access your module keys by from records in the Cryptographic Module \[sys\_kmf\_crypto\_module\] table. From a Cryptographic Module record, you can select the **Key alias** field in records in the **Module Keys** related list.

The information available depends on which version of Field Encryption you have active on your instance.

-   **Field Encryption Starter**

    Using Field Encryption Starter, you can view key usage audit data.

-   **Field Encryption Enterprise**

    You to perform manual key operations such as Renew, Revoke, Rotate, or Suspend, in addition to viewing key usage audit data.


## Module key information

Information on your module keys is displayed on the module key record in the fields listed here. These fields are read-only and used for information purposes only.

|Field|Description|
|-----|-----------|
|Generation date|When the Module key was generated|
|Activation date|When the Module key was activated.|
|Last renewal date|When the Module key was last renewed.|
|Last rotated date|When the Module Key was last rotated.|
|Deactivation date|When the Module Key was deactivated.|
|Destruction date|When the Module Key was destroyed.|
|Future activation date|When the Module Key will be activated.|
|Future renewal date|When the Module Key will be renewed.|
|Future rotation date|When the Module Key will be rotated.|
|Future destruction date|When the Module Key will be destroyed.|
|Key lifecycle state|Current the state of the Module Key.|

**Parent Topic:**[Configuring Field Encryption](../concept/configuring-column-level-encryption.md)

