---
title: Installed with Edge Encryption
description: Edge Encryption installs tables to store encryption-related data, system properties to configure default behavior, and the edge\_encryption role to administer Edge Encryption.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Exploring Edge Encryption, Edge Encryption, Encryption]
---

# Installed with Edge Encryption

Edge Encryption installs tables to store encryption-related data, system properties to configure default behavior, and the edge\_encryption role to administer Edge Encryption.

## Tables installed with Edge Encryption

Edge Encryption adds the following tables.

-   **Edge Encryption Configuration \[sys\_encryption\_configuration\]**

    Contains encrypted fields and tables for which attachments are encrypted.

-   **Edge Encryption Rule \[sys\_encryption\_rule\]**

    Contains a record for each rule. A rule has a name, the condition when it is used, a script, and an order field.

-   **Edge Encryption Invalid Insert Log \[sys\_edge\_encryption\_invalid\_insert\_log\]**

    Contains log messages created for attempts to save unencrypted data to an encrypted field.

-   **Edge Encryption Proxy \[sys\_encryption\_proxy\]**

    Contains information about the encryption proxy application.

-   **Edge Proxy Encryption Type \[sys\_proxy\_encryption\_type\]**

    Used for enabling and disabling encryption types on the encryption form.

-   **Encryption Job Execution \[sys\_encryption\_job\_execution\]**

    Supports mass encryption jobs.

-   **Encryption Job Execution Chunk \[sys\_encryption\_job\_execution\_chunk\]**

    Supports mass encryption jobs.

-   **Scheduled Encryption Job \[sysauto\_encryption\_job\]**

    Lists scheduled jobs for encryption, decryption, key rotation, order token repair, and database recovery.

-   **Encryption Key Configuration \[sys\_encryption\_key\_configuration\]**

    Lists default encryption keys.

-   **Encryption Key \[sys\_encryption\_key\]**

    Lists available keys and key attributes.

-   **Proxy Encryption Key \[sys\_encryption\_proxy\_key\]**

    Lists proxy encryption keys.


## Properties installed with Edge Encryption

Edge Encryption adds the following properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

-   **glide.edge.pattern.disallowed.chars**

    A list of characters that are not allowed in patterns.

    -   **Type**: a string of a comma-separated list of values
    -   **Location**: System Properties \[sys\_properties\] table
-   **glide.edge.pattern.min.size**

    The minimum pattern size allowed. Allowing smaller patterns means finding more matches, which increases overhead.

    -   **Type**: number
    -   **Default value**: 5
    -   **Location**: System Properties \[sys\_properties\] table
-   **sn\_edge\_encryption.logging.destination**

    Where messages are logged.

    -   **Type**: string
    -   **Default value**: file
    -   **Location**: System Properties \[sys\_properties\] table
-   **sn\_edge\_encryption.logging.verbosity**

    The logging level to use.

    -   **Type**: string
    -   **Default value**: info
    -   **Location**: System Properties \[sys\_properties\] table
-   **sn\_edge\_encryption.encryption.proxy.buildtag**

    The proxy version registered with your instance.

    -   **Type**: string
    -   **Location**: System Properties \[sys\_properties\] table
-   **sn\_edge\_encryption.cleartext.allowed**

    When true, allows clear text to be saved in an encrypted field. This happens when a user is accessing the instance without going through the Edge Encryption proxy. When false, the system prevents clear text from being saved in an encrypted field.

    -   **Type**: Boolean
    -   **Default value**: false
    -   **Location**: System Properties \[sys\_properties\] table

**Parent Topic:**[Exploring Edge Encryption](../concept/c_EdgeEncryptionOverview.md)

