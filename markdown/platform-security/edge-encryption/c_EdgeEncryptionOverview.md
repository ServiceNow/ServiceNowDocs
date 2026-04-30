---
title: Exploring Edge Encryption
description: Edge Encryption is a network encryption system that resides on your network and that encrypts and decrypts sensitive data as it travels between your data center and the ServiceNow cloud.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Edge Encryption, Encryption]
---

# Exploring Edge Encryption

Edge Encryption is a network encryption system that resides on your network and that encrypts and decrypts sensitive data as it travels between your data center and the ServiceNow cloud.

## What is Edge Encryption

Also referred to as ‘client-side’ encryption, Edge requires all bi-directional user traffic to pass through proxies that are maintained on your infrastructure. You have the full control over your key management because the keys are stored within your proxy on your infrastructure. The ServiceNow AI Platform can’t decrypt your ciphertext to access your keys.

The Edge Encryption feature is an additional cost option that provides you with the ability to control the end-to-end encryption of your data and key management. Edge Encryption uses a proxy application, provided by ServiceNow and installed by you within your own network. This proxy application tokenizes specified data patterns or encrypts string fields, Date fields, Date/Time fields, and attachment data before it’s sent from your environment to your instance. The proxy application also decrypts the same data, again only within your own network, using keys stored only within your own network.

The relevant encryption keys and configuration exist only on the Edge proxy within your network and aren’t visible to ServiceNow. The data is encrypted from the moment that it leaves your environment and is only decrypted upon retrieval. At no point is the data accessible in plaintext by ServiceNow systems or personnel.

## Who uses Edge Encryption

Only a user logged in to the instance through a proxy server on your network can view encrypted data in clear text. Likewise, only a security\_admin user logged in to an instance through a proxy server in your network can configure and administer Edge Encryption.

Because the proxy server resides in your network, you own and manage the encryption keys, and they’re never sent to the instance. As a result, ServiceNow never shows sensitive data in clear text.

In addition to the Edge proxy configuration and management of rules, you’re responsible for the usual requirements of operating a server within your environment \(including hosting, routing, backup, DNS configuration, and so on\) to enable and support your Edge proxies.

## Encryption and tokenization

Edge Encryption supports both encryption \(through encryption configurations\) and tokenization \(through encryption patterns\) as a means of protecting your sensitive information.

-   **Encryption configurations**

    You can encrypt individual fields using encryption configurations. Edge Encryption supports AES 128-bit and AES 256-bit encryption keys. Edge Encryption supports standard, equality-preserving, and order-preserving encryption types.

    In addition to attachments, you can encrypt the following field types:

    -   Date
    -   Email
    -   Date/Time
    -   HTML
    -   IP Address
    -   Journal
    -   Journal Input
    -   Multi-line text
    -   Single-line text
    -   String
    -   URL
    **Note:**

    If a Journal field marked for encryption is added to the activity stream, all user input to the field is encrypted in the activity stream.

    Multi-byte characters within supported field types can be encrypted.

    You can also encrypt the following service catalog variable types:

    -   String Types
    -   -   Single-line text
-   Multi-line text
-   Wide single-line text
    -   Date
    -   Date/Time
    -   URL
    -   Email
    -   HTML
    -   IP Address
-   **Encryption patterns**

    You can use encryption patterns to tokenize strings that match regular patterns such as social security and credit card numbers. While encryption configurations should be the primary method of encryption, use encryption patterns as a supplement to secure sensitive information found outside of encrypted fields.


**Note:** The Edge Encryption proxy server requires a MySQL database in your network only if using order preserving encryption or encryption patterns. Clear text values are stored in the proxy database in your network. For this reason, it is critical that you secure and regularly back up your proxy database. For recommendations, see [Edge Encryption components](c_EdgeEncryptionProxy.md).

![Flow of data using Edge Encryption.](../images/edge-overview.png)

## Edge Encryption on the ServiceNow AI Platform

Edge Encryption acts as a gateway between your browser and your ServiceNow instance. Traffic from your browser passes through the gateway on its way to the ServiceNow instance. The gateway, in turn, is configured to encrypt outbound data that is marked for encryption. Inbound traffic is decrypted through the gateway, and the end user sees clear text in the browser. The advantage of this implementation from a security control perspective is that the encryption and key management are handled externally from ServiceNow.

## Pros and cons

As with Field Encryption Enterprise and Field Encryption, Edge Encryption imposes some functional limitations within an instance as a result of the additional security. The local Edge proxy does, however, also provide some additional functionality relating to sorting when compared to column-level encryption.

Pros:

-   Edge Encryption provides absolute control of who sees your information and prevents data breaches.
-   Information remains on your proxy server and never leaves your network unencrypted.
-   Information is encrypted in transit, before it even reaches the ServiceNow instance.
-   You hold and manage all your own encryption keys. No one else, not even ServiceNow personnel, can access your keys.
-   You can choose the strength of the encryption algorithm: AES-128 or AES-256.
-   Edge Encryption includes the ability to encrypt String text, Date and Date/Time fields, attachments, URLs, and journals.
-   Edge Encryption provides Standard, Equality Preserving, and Order Preserving encryption of data at rest within the database and instance.
-   Encryption rules enable you to write custom scripts that tell the proxy server specifically what to encrypt and where to put that encrypted information in the instance. These scripts are useful when the data structure doesn't exactly match the ServiceNow instance.
-   Encryption patterns enable you to tokenize information such as passwords.

Cons:

-   Edge Encryption requires an extra network hop through the Edge proxies cluster, and extra processing, which can add delay to traffic. The added processing delay of the Edge Encryption application is negligible compared to the network hop.
-   Maintaining your own encryption keys can be complex and time-consuming.
-   A maximum of two encryption keys can be active at any given time. You cannot assign different keys to specific subsets of columns, data categories, user roles, or access scopes. However, one key can encrypt certain columns while a different version of the same key can be used to decrypt others.
-   Edge Encryption has the side effect that the server or platform can't decrypt the data to perform any manipulation of the decrypted data. As a consequence, functionality and data processing on the ServiceNow AI Platform may be restricted when encrypting columns with Edge Encryption.

## What to know before you begin

Because encryption and tokenization change the nature of your data, Edge Encryption can affect other instance processes. Before using Edge Encryption, carefully consider the impact on your instance.

Because the proxy server is installed and maintained in your network, Edge Encryption requires network administration and management. Review the network requirements to ensure a smooth implementation.

Review the following topics to understand the impact of Edge Encryption on your instance:

-   [Planning for Edge Encryption](c_EdgeEncryptionPlanning.md)
-   [Edge Encryption system requirements](../reference/r_CloudEdgeSystemRequirements.md)
-   [Sizing your Edge Encryption environment](edge-environment-size.md)
-   [Calculate the order-preserving and tokenization database size](../task/size-db.md)
-   [Edge Encryption limitations](../reference/edge-encryption-limitations.md)
-   [Key management for Edge Encryption](c_EncryptionKeyManagement.md)

-   **[Edge Encryption components](c_EdgeEncryptionProxy.md)**  
Edge Encryption is composed of the Edge Encryption proxy server that runs on a server in your network, and the Edge Encryption plugin that must be installed on your ServiceNow instance. If using order-preserving encryption types or encryption patterns, a proxy database must also be installed in your network.
-   **[Edge Encryption clients](../reference/edge-clients.md)**  
Edge Encryption uses three clients to inform the instance that the proxy is running, to synchronize requests between the proxy and the instance, and to forward all end user requests to the instance after any potential encryption.
-   **[Key management for Edge Encryption](c_EncryptionKeyManagement.md)**  
You are responsible for providing and managing the encryption keys used by Edge Encryption.
-   **[Encryption configurations and patterns](c_EncryptionTypes.md)**  
With Edge Encryption, you can encrypt fields and tokenize strings.
-   **[Installed with Edge Encryption](../reference/installed-with-edge-encryption.md)**  
Edge Encryption installs tables to store encryption-related data, system properties to configure default behavior, and the edge\_encryption role to administer Edge Encryption.

**Parent Topic:**[Edge Encryption](../reference/edge-encryption.md)

