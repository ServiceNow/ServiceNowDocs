---
title: Field Encryption and system clones
description: Cloning an instance with Field Encryption installed automatically generates new field encryption module encryption keys on the target clone instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-10"
reading_time_minutes: 1
breadcrumb: [Configuring Field Encryption, Field Encryption, Encryption]
---

# Field Encryption and system clones

Cloning an instance with Field Encryption installed automatically generates new field encryption module encryption keys on the target clone instance.

If Field Encryption is installed on your instance, a new field encryption module encryption key is automatically generated on the target clone instance as a part of clone process. These keys are generated for all modules to which the user has access, and that does not have a key already.

Because of this, field encryption modules on the target clone instance may have two module encryption keys present:

-   An active module encryption key. This is the new key generated after clone, as long as the module is accessible to the user and has no prior keys.
-   A deactivated encryption module key \(from the automated key exchange transfer

    The active module encryption key is used to encrypt inserted data as needed on the target clone instance. The deactivated module is used to decrypt existing data that was cloned over as part of the system clone.

    To use a single key to decrypt and encrypt all data, you can run a module rekeying job. For more information about module rekeying jobs, see [Schedule mass encryption, decryption, and rekeying jobs](../../encryption/task/schedule-mass-jobs.md).


**Parent Topic:**[Configuring Field Encryption](../../encryption/concept/configuring-column-level-encryption.md)

