---
title: Data security for ServiceNow mobile apps
description: ServiceNow mobile apps use SSL/TLS for Over-the-Air \(OTA\) communication encryption for data security. The OAuth authorization endpoints are HTTPS.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Device security for ServiceNow Mobile apps, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# Data security for ServiceNow mobile apps

ServiceNow mobile apps use SSL/TLS for Over-the-Air \(OTA\) communication encryption for data security. The OAuth authorization endpoints are HTTPS.

## Data stored in your mobile apps

Application preference data such as favorites, home screen, and the mobile navigator items are stored and cached locally on the mobile device. ServiceNow mobile apps do not store record data such as incidents and problems on the device unless your organization has specifically enabled offline syncing for Field Service. The record data is encrypted with AES 256.

Information stored in mobile apps

-   Databases
    -   User defined instances
    -   Favorite application IDs
    -   Push Notifications
    -   Geolocation updates
    -   Offline data
-   Preferences stored in mobile apps
    -   sys\_id, display name, username, and initials of the current user
    -   URL and name of the current instance
    -   Last activity timestamp
    -   Encrypted PIN code
    -   Offline cache warning period
    -   Server Properties
        -   LOCATION\_PROXIMITY
        -   IS\_PIN\_CODE\_REQUIRED
        -   IS\_BLURRED\_IN\_BACKGROUND
        -   IS\_BLOCK\_ATTACHMENT\_SHARING
        -   LOCATION\_TRACKED
        -   IS\_CLEARING\_CLIPBOARD\_IN\_BACKGROUND
        -   IS\_HIDE\_APPLICATIONS\_SCREEN\_IMAGE
        -   IS\_OFFLINE\_ENABLED
        -   LOCATION\_FREQUENCY
    -   key\_analytics\_initial\_app\_launch flag
-   Information stored in the system Account Manager
    -   Login date
    -   Instance URL
    -   Access Token
    -   Refresh Token

## Data in motion

Data in motion is over a secure SSL/TLS channel and encrypted with HTTPS.

## Offline access and data cache configuration

Choose specific screens and actions to be enabled offline from with Mobile App Builder. On the mobile device, your users can select offline and choose to “cache data" from Settings. The offline flows that you designate are downloaded and cached to the device.

You can encrypt offline cached data by using native encryption. This encryption expires at a specified period of time. The default is 48 hours or when a user signs out of the mobile app.

Offline data is protected by local-auth and the app PIN that can be optionally enabled by administrators. When enabled, users are required to enter a PIN on login, or when the application is inactive for five minutes.

## Disabling mobile attachments

You can disable attachments for mobile apps by using access control rules. For more details on this process see [Disable attachments in mobile apps](../task/sg-disable-mobile-attach.md).

**Parent Topic:**[Device security for ServiceNow Mobile apps](sg-mobile-security.md)

