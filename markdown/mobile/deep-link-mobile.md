---
title: Deep linking for mobile
description: Mobile deep links are linking formats that direct users to specific content and locations within a mobile app. These links can be placed in email notifications, text messages, push notifications, launcher screens, and input form screens. You can also configure a mobile app login URL for multiple SSO identity providers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Deep linking for mobile

Mobile deep links are linking formats that direct users to specific content and locations within a mobile app. These links can be placed in email notifications, text messages, push notifications, launcher screens, and input form screens. You can also configure a mobile app login URL for multiple SSO identity providers.

You can activate mobile deep link URLs to navigate users into any screen type within a mobile app. The deep link consists of a specific structure, which points to a specific location within a defined mobile app. These links can then be placed wherever desired. Most commonly, deep links are used within push and email notifications.

-   For push notifications, deep link URLs are used to navigate the end user to a defined screen after tapping on the notification itself. For information on configuring a push notification, see [Mobile push notifications](sg-mobile-push-notifications.md).
-   For email notifications, deep link URLs can be placed within the email body. The end user taps on this link to launch the appropriate mobile app and automatically navigate to the desired screen. For information on configuring an email notification, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).

Mobile deep links are activated through the mobile deep link generator. The mobile deep link generator operates as a platform script include, within the global application scope. For additional information see, [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).

-   **[Mobile deep link structure](../reference/deep-link-mobile-structure.md)**  
Familiarize yourself with how to construct and use mobile deep links in any screen type within a mobile app.

**Parent Topic:**[Mobile URLs](mobile-urls.md)

