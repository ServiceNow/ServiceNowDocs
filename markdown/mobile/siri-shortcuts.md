---
title: Siri shortcuts
description: Configure Siri shortcuts to give your users quick access to common app functions app using their iOS devices.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Siri shortcuts

Configure Siri shortcuts to give your users quick access to common app functions app using their iOS devices.

By default, your iOS users can use the following pre-configured shortcuts in the Now Mobile app:

-   Open a chat window \(see below note\)
-   Browser items and services
-   Open my tasks
-   Open my requests
-   Search in the ServiceNow instance \(see below note\)

**Note:**

-   To open a chat window in the Mobile Agent app, users can access Agent Chat if the following conditions are met:
    -   The Agent Chat plugin \(com.glide.interaction.awa\) must be installed on your instance. For details on configuration, see [Setting up Agent Chat](https://www.servicenow.com/docs/access?context=ac-configure-agent-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).
    -   The mobile app must have a chat launcher quick action enabled. For details on enabling chat launcher, see [Enable Live Agent in the Now Mobile app](https://www.servicenow.com/docs/access?context=va-in-me&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).
-   To search in the ServiceNow instance, the following conditions must be met:
    -   The instance must have global search set up. For details on configuration, see [Global search for mobile](mobile-search-config.md).
    -   The global search must be configured on the first tab in the mobile app.

For details about configuring a Siri shortcut on your instance, see [Configure a Siri shortcut](../task/config-siri-shortcuts-2.md).

-   **[Configure a Siri shortcut](../task/config-siri-shortcuts-2.md)**  
Change the destination screen of your Siri shortcuts to direct your users to a different screen than the default.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

