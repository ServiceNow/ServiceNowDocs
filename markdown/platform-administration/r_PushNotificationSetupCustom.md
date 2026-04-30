---
title: Push notification setup with a custom push application for ServiceNow mobile apps
description: If you are using your own custom mobile or push application, you must configure your app for use and set up the push contents.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Push notification setup with a custom push application for ServiceNow mobile apps

If you are using your own custom mobile or push application, you must configure your app for use and set up the push contents.

Setting up a push notification infrastructure that uses a custom push app involves a push admin \(also called push app developer or mobile app developer\) and system administrator. When push admins create a customized push app, they also configure the app, its push message content \(payload generators\), and optional attributes, such as push action scripts. The admin creates and updates the push notifications for the custom push app. After users install the custom push app and initially log in to their instance from their mobile device, the system automatically creates a device \(channel\) for the custom app.

**Note:** These instructions are intended for users who develop their own customized push application. You do not need to configure the ServiceNow mobile push application.

This process describes configuration used in the ServiceNow mobile app. Push Notification configuration for the current ServiceNow mobile UI can be found at [Mobile push notifications](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&version=yokohama&pubname=yokohama-mobile&ft:locale=en-US)

![Push notification setup tasks for a custom push app](../image/CustomPushAppSetup.png "Push notification setup tasks for a custom push app")

## Before you begin

Complete the steps in [Activate push notifications](../task/t_ActivatePushNotifications.md).

Assign the push\_admin role to your organization's mobile app developer.

## What to do — push admin

Configure push notifications for your custom push app. This process differs for iOS and Android devices.

1.  \(iOS only\) [Upload a push certificate to your instance](../task/upload-push-cert.md)

    Upload a push certificate to your instance so that you can use it later to connect your iOS device to the push notification system.

2.  [Create a push application record for your custom app](../task/t_CreateAMobileApplication.md)

    Register your customized mobile application with your instance to receive push notifications for the application. The instance uses this push application record to identify the device + push application combination necessary to determine a push notification recipient.

3.  [Create push message content](../task/t_CreateAMobileMessageLayout.md)

    Create a JSON content payload for different types of push notifications. The content determines how a push notification appears on the push application, and whether the user can send a message in response to the push notification. The push admin can create attribute definitions that specify a default push action script or string, for use in the push message content.

4.  \(Optional\) [Create a push message attribute definition](../task/t_CreateAPushMessageAttribute.md)

    Push message attribute definitions allow you to create reusable properties for push message content specification.

5.  \(Optional\) [Create an attribute value or action for a push message](../task/t_CreateAPushMessageAttributeValue.md)

    You can create attribute values that override the default attribute definitions used in the push message content.

6.  \(Optional\) [Create a push action](../task/t_CreateAMobileActionScript.md)

    A push action is a server-side script that runs when the instance receives a response to an actionable push message.


## What to do — admin

Create the push messages and push notifications: The administrator [creates the push messages](../task/t_CreateAPushMessage.md), [sets up push notifications](../task/t_CreatePushNotification.md) for the custom push app, and if desired, the content.

## Next steps

Use the Push Installation API to opt users in to receive push notifications. For more information, see [Push Installation API](https://www.servicenow.com/docs/access?context=pushinstallation-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

