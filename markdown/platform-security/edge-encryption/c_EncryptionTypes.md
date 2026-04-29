---
title: Encryption configurations and patterns
description: With Edge Encryption, you can encrypt fields and tokenize strings.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Edge Encryption, Edge Encryption, Encryption]
---

# Encryption configurations and patterns

With Edge Encryption, you can encrypt fields and tokenize strings.

## Encryption configurations

You can encrypt individual fields using encryption configurations. Edge Encryption supports AES 128-bit encryption keys. If the Java Cryptography Extension \(JCE\) Unlimited Strength Jurisdiction Policy files are installed, Edge Encryption supports AES 256-bit encryption keys for each encryption type. Edge Encryption supports the following types of encryption configurations.

-   **Standard encryption**

    The encrypted value of a field is different each time the field is encrypted, even when the field value remains the same. Standard encryption is the most robust form of encryption. Fields using standard encryption cannot be sorted, grouped by, or filtered on.

-   **Equality-preserving encryption**

    The encrypted value of a field is the same when the field value remains the same. Supports equality comparisons and group by operations on a field.

    **Note:** When equality-preserving encryption is selected for a field that already contains data, performing a group by action on the field may not group fields with the same value if one is encrypted and the other is not.

-   **Order-preserving encryption**

    Uses tokens and encryption to secure data in your proxy database. Supports equality comparisons, group by operations, and the ability to sort data. The order preserving encryption type is only supported if there is a MySQL database configured for the Edge Encryption proxy server.

    **Note:** When using order-preserving encryption and the proxy database is down, updates can be made to fields using order-preserving encryption. However, the sort order will not be correct when trying to sort data based on those fields. Groups also will not work as expected. When the proxy database is again operational, schedule an order token repair job to repair missing tokens.


|Encryption type|Description|
|---------------|-----------|
|Standard AES 256|Fields cannot be filtered, sorted, or compared.|
|Standard AES 128|Fields cannot be filtered, sorted, or compared.|
|Equality preserving AES 256|Fields can be filtered using equality comparisons.|
|Equality preserving AES 128|Fields can be filtered using equality comparisons.|
|Order preserving AES 256|Fields can be sorted and equality comparison filtering can be used. Requires the use of a MySQL database in your network.|
|Order preserving AES 128|Fields can be sorted and equality comparison filtering can be used. Requires the use of a MySQL database in your network.|

## Encryption Patterns

You can secure sensitive data found in strings using encryption patterns. Once an encryption pattern is stored and activated, the Edge Encryption proxy server identifies strings that match the pattern in requests. Once located, the clear text string is stored in the proxy database and replaced on the instance with a token. Use encryption patterns to tokenize strings that match regular patterns such as social security and credit card numbers. While we recommend that encryption configurations be the primary method of encryption, use encryption patterns as a supplement to locate and secure sensitive information found outside of encrypted fields.

**Note:** The Edge Encryption proxy server requires a MySQL database in your network only if using order preserving encryption or encryption patterns. Clear text values are stored in the proxy database in your network. For this reason, it is critical that you secure and regularly back up your proxy database. For recommendations, see [Edge Encryption components](c_EdgeEncryptionProxy.md).

**Parent Topic:**[Exploring Edge Encryption](c_EdgeEncryptionOverview.md)

**Related topics**  


[Encrypt fields using encryption configurations](c_ConfigureCloudEdge.md#)

[Tokenize strings using encryption patterns](../task/t_ConfigureBasicEncryptionPatterns.md)

