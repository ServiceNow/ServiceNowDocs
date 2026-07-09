---
title: Encryption at rest for Hermes
description: Encryption at rest for Hermes topics protects message data stored on broker disks from unauthorized access. Hermes supports both ServiceNow-managed keys and keys you provide using the Bring Your Own Key \(BYOK\) model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/multi-instance-framework-hermes/encryption-at-rest.html
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: concept
last_updated: "2026-06-26"
reading_time_minutes: 2
keywords: [Encryption at rest, BYOK, Bring your own key, encrypt messages]
breadcrumb: [Explore, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Encryption at rest for Hermes

Encryption at rest for Hermes topics protects message data stored on broker disks from unauthorized access. Hermes supports both ServiceNow-managed keys and keys you provide using the Bring Your Own Key \(BYOK\) model.

Encryption at rest is an opt-in feature that encrypts message data before it is written to broker disks. Brokers handle all encryption and decryption internally. When you enable encryption on a topic that already contains messages, previously produced messages remain readable and all new messages are encrypted. No data migration is required.

When BYOK is enabled, your organization provides an external key through the Cloud Encryption service. Hermes uses that key to encrypt messages in the topic. The Cloud Encryption service handles key derivation and wrapping.

## Key benefits

-   Protect message data at rest without modifying producer or consumer applications.
-   Choose between ServiceNow-managed keys for simplified operations or BYOK for organizations with strict data compliance requirements.

## Key management for Hermes Encryption

\[Omitted image "hermes-byok-key-management.png"\] Alt text: ServiceNow-managed vs. BYOK key management flows for Hermes encryption at rest.

Wrapping keys are stored in the Cloud Encryption key management service \(KMS\), not on Hermes brokers. The service unwraps the keys at runtime over a secure connection. Because existing records remain decryptable, you can rotate your key without migrating data.

**Warning:** If you revoke your customer-supplied key, your instance might stop working because the database can't access the encrypted data. If the Cloud Encryption key management service is unreachable, message production is blocked until the connection is restored. For more information, see the [Key management operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/key-mgmt-operations-ce.md).

## Topics and encryption at rest

-   Each topic uses a data encryption key \(DEK\) that is protected by a wrapping key stored in the Cloud Encryption key management service.
-   You can enable or disable encryption on a topic at any time. Enabling encryption introduces CPU overhead because brokers must encrypt every message on write and decrypt every message on read. When you toggle encryption, previously produced records retain their original state, that is, encrypted records stay encrypted, unencrypted records stay unencrypted. Brokers automatically decrypt encrypted records and deliver plain text to consumers.
-   Because the encryption key is customer-specific, shared topics aren't supported.
-   Encryption at rest is not supported for compacted topics \(topics configured to retain only the latest value per key\).

To enable encryption at rest on a topic, see [Enable encryption at rest for a Hermes topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/multi-instance-framework-hermes/enable-encryption-at-rest-for-hermes.md).

