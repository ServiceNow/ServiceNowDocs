---
title: Security and compliance in offline mode
description: Learn how to manage offline mode access and determine which users can use it, helping to secure sensitive data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/security-offline.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Security and compliance in offline mode

Learn how to manage offline mode access and determine which users can use it, helping to secure sensitive data.

Offline mode stores data locally on the device. Configure offline rules to align data access with your security requirements. Use the glide.sg.offline.roles system property to restrict offline access to users who require it, limiting the amount of sensitive data stored on devices in the field.

The following system properties are available when managing attachments in offline mode:

|Property|Description|
|--------|-----------|
|glide.sg.ofﬂine.roles|A comma-separated list of role names that are allowed to work in ofﬂine mode.|
|glide.sg.ofﬂine.expiration|Defines how long an offline cache remains valid on the device.|

For more information on these and other related offline system properties, see [System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md).

-   **[General guidelines for offline mode security and compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/general-guidelines-offline-security.md)**  
When working offline mode, keep these security and compliance general guidelines in mind for usability and a good user experience.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)

