---
title: Device security for ServiceNow Mobile apps
description: This document applies to current ServiceNow apps for iOS and Android for Australia. This document may be subject to change for future mobile releases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Device security for ServiceNow Mobile apps

This document applies to current ServiceNow apps for iOS and Android for Australia. This document may be subject to change for future mobile releases.

-   **[Components and architecture](sg-mobile-security-components-architecture.md)**  
The ServiceNow mobile apps consist of the ServiceNow server instance and native apps for iOS and Android. The apps use fully native code and are not a hybrid approach. The mobile client applications communicate over a wireless connection with the server and pull live data for the end user.
-   **[Identity and access management](sg-mobile-ID-access-mgmt.md)**  
Learn about user authentication, third party authentication, and user session termination for mobile applications.
-   **[Mobile data flow for ServiceNow mobile apps](sg-security-mobile-data-flow.md)**  
Data can be retrieved, downloaded from, and written back to a mobile device.
-   **[Internal mobile app distribution](sg-mobile-security-app-distro.md)**  
Internal distribution of ServiceNow mobile apps is supported through all major EMM vendors.
-   **[Data security for ServiceNow mobile apps](sg-mobile-security-data.md)**  
ServiceNow mobile apps use SSL/TLS for Over-the-Air \(OTA\) communication encryption for data security. The OAuth authorization endpoints are HTTPS.
-   **[Push notifications](sg-mobile-security-push-notif.md)**  
Administrators create push notifications and users are able to receive them.
-   **[Mobile security practices](sg-mobile-security-practices.md)**  
Mobile security practices include mobile-specific system properties, attachment control, password reinforcement, security patching, and controlling shared data.
-   **[Edge Encryption for ServiceNow mobile](sg-edge-encryption.md)**  
Users can view and edit data protected with Edge Encryption within their mobile device. The data appears in readable form on the mobile device but is encrypted in the database.

