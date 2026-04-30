---
title: Setting up push notifications on your ServiceNow instance
description: For each Mobile SDK application that incorporates the Virtual Agent service and leverages push notifications, you must complete the following configuration process on your ServiceNow instance.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Setting up push notifications on your ServiceNow instance

For each Mobile SDK application that incorporates the Virtual Agent service and leverages push notifications, you must complete the following configuration process on your ServiceNow instance.

-   Generate and retrieve an iOS push certificate.
-   Add a push application record in the Push Application \[sys\_push\_application\] table.
-   Add a push notification message content record in the Push Notification Message Content \[sys\_push\_notif\_msg\_content\] table.
-   Add a default push registration.
-   Add a push notification message in the Push Notification Message \[sys\_push\_notif\_msg\] table.
-   Modify the push notification record in the Notification \[sysevent\_email\_action\] table.

