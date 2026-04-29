---
title: Edge Encryption dictionary attributes
description: Add dictionary attributes to tables and fields to control how they work with Edge Encryption.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption dictionary attributes

Add dictionary attributes to tables and fields to control how they work with Edge Encryption.

To set a dictionary attribute to true, you must enter `attribute=true` in the **Attributes** field. To add a dictionary attribute to a record, see [Altering tables and fields using dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

-   **Edge Encryption Excluded \[edge\_encryption\_excluded\]**

    Determines whether the field is excluded from encryption.

    When set to `true`, the field or table can’t be encrypted. When set to `false`, the field can be encrypted.

    -   Value: true/false
    -   Target element: field or table
    -   Default value: false
-   **Edge Encryption Enabled \[edge\_encryption\_enabled\]**

    Determines whether the field is eligible for encryption through an encryption configuration.

    When set to `true`, the field is eligible for encryption. When set to `false`, the field isn't eligible for encryption. Because this attribute is used by the system and can’t be modified, it isn’t displayed to the user.

    **Note:** This attribute doesn’t indicate that a field is encrypted, nor does it trigger any encryption logic on the field. Rather, the attribute determines the possibility of the field being encrypted by a user.

    -   Value: true/false
    -   Target element: field
    -   Default value: true for String fields
-   **Edge Encryption Clear Text Allowed \[edge\_encryption\_clear\_text\_allowed\]**

    Determines whether server-side scripts may append non-encrypted data to an encrypted string within the field for user actions performed through the proxy server, or any server-side automated scripts, such as scheduled jobs.

    When set to `true`, appending data is allowed. When set to `false`, appending data isn’t allowed.

    -   Value: true/false
    -   Target element: field
    -   Default value: false

**Parent Topic:**[Configuring Edge Encryption](../concept/edge-config.md)

