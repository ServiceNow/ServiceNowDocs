---
title: Notifications release notes
description: The ServiceNow Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Notifications release notes

The ServiceNow® Notifications application enables you to create, manage, and send custom notifications in workflows for important events, actions, and alerts. Notifications was enhanced and updated in the Xanadu release.

## Notifications highlights for the Xanadu release

-   Redact sensitive data from customer-initiated inbound emails.
-   Support for international characters in the email addresses.
-   Filter by category in system notifications and search for custom notifications.
-   Optimize SMTP sender job to enhance outbound email delivery.
-   Modify email retry logic for a better delivery experience according to RFC 5321.

See [Notifications](https://www.servicenow.com/docs/access?context=notifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **[Sensitive data redaction](https://www.servicenow.com/docs/access?context=sensitive-data-redaction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Redact sensitive data for inbound emails.

-   **International characters support**

    Support added for International characters in the email addresses.


## UI changes

-   **[Search button](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    A search button has been added for custom notifications within the notification preferences.

-   **[Category filter](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    A category filter for system notifications has been added to the notification preferences.

-   **[Inbound actions](https://www.servicenow.com/docs/access?context=sensitive-data-redaction&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    An additional check box has been added to enable redaction of sensitive data.


## Changed in this release

-   **[New search and category filter in notification preferences](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Notification preferences now include the ability to search within custom notifications and filter by category in system notifications.

-   **[Email unsubscribe](https://www.servicenow.com/docs/access?context=email-unsubscribe&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Unsubscribe from emails using the unsubscribe capability in the email header.

-   **[Language preferences](https://www.servicenow.com/docs/access?context=multilingual-email-notifications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Honor sys\_user language preferences set by users for email translations.


## Activation information

Notifications is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

Screen reader support has been extended to the aria labels in the notification preferences and the advanced preferences. The support provides an explanation for button actions, such as the toggle button.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

