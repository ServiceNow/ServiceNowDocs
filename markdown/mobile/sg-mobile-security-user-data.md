---
title: User data collection
description: ServiceNow mobile apps do not specifically collect any user data.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile security practices, Device security for ServiceNow Mobile apps, Mobile security, Configuring the Mobile Platform, Mobile Platform]
---

# User data collection

ServiceNow mobile apps do not specifically collect any user data.

Any user transactions or usage within an app is tracked on the ServiceNow instance just as it is on the web. For user credentials, after a user logs in, the mobile app negotiates an OAuth Token that is stored in the Apple Keychain or the Android Keystore. User credentials are never saved. If the user opts in, the following information is collected:

-   Location
-   Access to camera
-   Notifications

**Parent Topic:**[Mobile security practices](sg-mobile-security-practices.md)

