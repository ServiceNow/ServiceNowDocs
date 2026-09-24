---
title: Encryption release notes
description: The ServiceNow Encryption application protects your sensitive data and helps you meet regulatory requirements and standards. See the following sections for release notes by version.Encryption updates for the Brazil Early Availability release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/encryption-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [encryption, edge encryption, field encryption, cloud encryption, database encryption, key management, certificates, encryption, edge encryption, Java 21]
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Encryption release notes

The ServiceNow® Encryption application protects your sensitive data and helps you meet regulatory requirements and standards. See the following sections for release notes by version.

## About Encryption

The ServiceNow® Encryption application protects your sensitive data and helps you meet regulatory requirements and standards. Encryption provides multiple solutions to safeguard your instance, including Key Management Framework, Field Encryption, Cloud Encryption, Edge Encryption, Database Encryption, and certificate management.

## Activation and other requirements

-   **Activation information**

    Platform Encryption Key Management Framework is available with activation of the com.glide.encryption.external\_kms, which requires a separate subscription. For details, see [Encryption and Key Management subscription bundle](https://www.servicenow.com/docs/access?context=encryption-sku&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Important information for upgrading to Brazil**
    -   If you're using scheduled upgrade to upgrade your Edge Encryption proxy from a pre-Brazil release to Brazil, you must meet the following requirements before you attempt the upgrade:
        -   Upgrade the Java version to Java 21 or later.
        -   Ensure you're on Zurich Patch 13 \(ZP13\) or Australia Patch 6 \(AP6\) or later. If you're on an earlier version, scheduled upgrade will not work.
    -   If you're using command-line upgrade, you must upgrade the Java version to Java 21 or later.
    -   Java 17 is required to install Edge Encryption on versions Yokohama through Australia. Prior to upgrading to Brazil, you must upgrade to Java 21. See [Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_InstallEdgeEncryptionProxy.md) for installation details.

## Brazil Early Availability

Encryption updates for the Brazil Early Availability release.

### What's new

-   **Edge Encryption proxy now supports Java 21**

    Install and run the Edge Encryption proxy on systems with Java 21.0 or later. You can now use newer Java versions for enhanced security and performance benefits. Current supported versions are Java 21.0 or later in the 21.x version series, and Java 17.0.3 or later in the 17.x version series. For installation details, see [Installing Edge Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/c_InstallEdgeEncryptionProxy.md).


