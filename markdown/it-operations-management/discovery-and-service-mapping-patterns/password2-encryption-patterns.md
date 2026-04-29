---
title: Password2 encryption for patterns
description: The Password \(two-way encrypted\) field type is used to encrypt and decrypt data. The field type works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Pattern Designer and related applications, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Password2 encryption for patterns

The Password \(two-way encrypted\) field type is used to encrypt and decrypt data. The field type works in accordance with NIST 800-57 guidelines and provides FIPS 140-2-L3 protection.

Password2 is a text field that stores sensitive data with two-way encryption. The two-way encryption stores the data as a secure encrypted value that can be decrypted within the ServiceNow AI Platform instance.

From Quebec, Key Management Framework enables you to manage keys used for Password2 fields. However, the implementation of Password2 is required on a ServiceNow AI Platform using the Rome release or later.

**Note:** Only newly created records containing Password2 fields are two-way encrypted. Existing data is not automatically converted to use Password2 encryption.

## Verify Password2 implementation

-   **Discovery and Service Mapping Patterns store app**

    Verify that the Discovery and Service Mapping Patterns store app \(version 1.0.76\) is installed.

-   **Verify Password2 is included in XML records**

    View the XML records in the ServiceNow AI Platform instance, and verify that the encryption looks similar to this example:![Password2 encryption](../image/password2-encryption-patterns.jpg)


**Parent Topic:**[Configuring Pattern Designer and related applications](../reference/configuring-pattern-designer-plugins.md)

