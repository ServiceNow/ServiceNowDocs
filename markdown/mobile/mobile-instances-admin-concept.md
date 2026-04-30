---
title: Mobile instances
description: Instances available on your ServiceNow mobile apps correspond to at least one instance on your ServiceNow platform web-based UI. According to your setup, the mobile instance contains some of the data and capabilities found on the web-based UI.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-15"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile instances

Instances available on your ServiceNow mobile apps correspond to at least one instance on your ServiceNow platform web-based UI. According to your setup, the mobile instance contains some of the data and capabilities found on the web-based UI.

A ServiceNow platform configuration can contain one or more instances. Each ServiceNow mobile app must be connected to at least one of these instances. If only one instance is added to the mobile apps, this is known as a single instance. Whereas if more than one instance is added, this is known as either multiple instance or multi-instance.

For information on user-side documentation regarding instances, see [Working with instances](instances-concept.md).

## Single instance

Users with a single instance are directly navigated to the login screen, bypassing the instance management page. This process shortens the login process. You can configure a branded landing page, which is a web page displayed to the user that contains a link to log in to a ServiceNow mobile app. For more information, see [Branded landing page for a single instance](branded-landing-page.md).

## Multiple instances

Users can add multiple instances from the instance management page. Users can switch from their current instance to other instances, without the need to log out of the current instance. The switch between instances occurs either through deep links, push notifications or by manually selecting an existing instance.

-   **Considerations for users when using multiple instances**
    -   Notifications: Notifications are received from all instances which the user is logged in to. This includes instances which the user is not currently interacting with.
    -   PIN code: Users must enter a PIN code when switching from an instance that doesn’t require a PIN to an instance that requires a PIN.
    -   Offline behavior: Users can't change instances while offline. To work with multiple instances, users must turn off the offline option.

