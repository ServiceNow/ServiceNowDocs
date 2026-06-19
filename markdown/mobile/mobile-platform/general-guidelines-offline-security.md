---
title: General guidelines for offline mode security and compliance
description: When working offline mode, keep these security and compliance general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/general-guidelines-offline-security.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Security and compliance, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for offline mode security and compliance

When working offline mode, keep these security and compliance general guidelines in mind for usability and a good user experience.

**Note:** Many of the issues discussed can be resolved using system properties. See the Perry system property file for more information.

-   **Offline data encryption**

    Offline data is encrypted if the user has a passcode enabled on their device. On Android, all data is encrypted regardless of whether a passcode is set.

-   **Restricting offline mode by role**

    Use the `glide.sg.offline.roles` system property to define which roles can access offline mode, such as field agents. If left empty, all users can use offline mode.

-   **PII protection and security compliance**

    ServiceNow supports the protection of personally identifiable information \(PII\) and is designed to align with organizational and regulatory security requirements.

    The following are examples of this policy:

    -   Data security policies: ServiceNow's data security framework governs the handling of PII across all mobile and platform experiences. These policies cover data at rest, data in transit, and offline access configurations.
    -   Data at REST: ServiceNow mobile apps do not store record data such as incidents and problems on the device unless your organization has specifically enabled offline syncing. Record data is encrypted using AES-256.
    -   Data in transit: All data transmitted between the mobile app and the ServiceNow instance is secured via SSL/TLS and encrypted using HTTPS.
    -   Offline access and cache configuration: Administrators can configure offline access by enabling cache downloads for designated workflows. Offline cached data is encrypted using native encryption and expires after a set period, typically 48 hours or upon user sign-out.
    -   Local protection: Offline data supports additional protection through local authentication and optional app-level PIN enforcement, helping to reduce unauthorized access to cached content.
-   **Data loss prevention**

    ServiceNow helps support data loss prevention through a combination of content restrictions, secure data transmission, and encryption protocols.

    Content restrictions:

    -   Copy/paste controls: Prevents unauthorized copying of sensitive information via MAM policy.
    -   PIN password enforcement: Strengthens access security on mobile devices.
    -   Attachment blocking: Allows administrators to block file attachments from mobile apps.
    Secure mobile traffic:

    -   All mobile data is transmitted over a secure SSL/TLS channel and encrypted using HTTPS, ensuring protection during transit.
    -   Data encryption:
        -   Local storage: Only non-sensitive app preference data are cached locally. For example, favorites, home screen layouts, and navigator items.
        -   Offline mode: When enabled, record data and related mobile tables, like screens, are encrypted using  AES-256, providing protection for data at rest.
-   **Offline cache expiration**

    Set the `glide.sg.offline.expiration` system property to define how long cached data remains on the device. The default is 48 hours, after which data is automatically deleted, reducing risk if a device is lost or stolen and ensuring data stays fresh.

-   **Conditions for cached data deletion**

    Cached data is only deleted under the following conditions:

    -   Expiration: The cache automatically clears when it reaches its expiration time.
    -   Manual deletion: The user manually deletes the cache.
    -   Logout: The user logs out of the app.
    **Note:** A new cache download only updates the existing cache.


**Parent Topic:**[Security and compliance in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/security-offline.md)

