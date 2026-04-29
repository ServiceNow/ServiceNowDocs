---
title: Control specific app usage
description: To support your organization's authentication policies, admins can control which mobile apps can log in to ServiceNow instances.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Control specific app usage

To support your organization's authentication policies, admins can control which mobile apps can log in to ServiceNow instances.

To control which mobile apps can log in to ServiceNow instances, admins can choose either basic app allowance lists or advanced app allowance. The advanced allowance mode enables admins to add links to authorized apps. These two modes are described in the following sections.

**Important:**

-   The basic and the advanced app allowance modes should not both be configured on the same instance. If you configure both modes on the same instance, the system always prioritizes the advanced mode configuration over the basic mode configuration.
-   This feature is available on both on-premises and cloud instances.

## Basic app allowance lists

By configuring a system property, admins can create a list of mobile apps that can connect to ServiceNow instances. If a user tries to connect to an instance with an app that isn't on the list, the user receives an `Unable to log in …` message as shown in the following image.

![Mobile app login screen that shows the "Unable to log in" message.](../image/mobile-app-cant-connect2instance.png "Failed login by an unauthorized app")

## Advanced app allowance with links to permitted apps

Using Scripted Extension Points, admins can create a list of apps that can log in to ServiceNow instances. Admins can change the **Dismiss** link text to route the user to the appropriate mobile app. Using the link, end users can connect to an instance with an authorized mobile app.

