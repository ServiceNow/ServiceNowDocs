---
title: Generate and retrieve an iOS push certificate
description: You must retrieve your unique iOS push certificate from your Apple Developer account so that you can associate it to your Mobile SDK applications that leverage push notifications.
locale: en-US
release: yokohama
product: Developer Guides
classification: developer-guides
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up push notifications on your ServiceNow instance, Configure push notifications, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Generate and retrieve an iOS push certificate

You must retrieve your unique iOS push certificate from your Apple Developer account so that you can associate it to your Mobile SDK applications that leverage push notifications.

## Before you begin

Role required: admin

You must already have an Apple Developer account set up. For information on how to create an Apple Developer account and download the corresponding SDK, refer to the [Apple Developer](https://developer.apple.com/) website.

## Procedure

1.  From your Apple Developer account, select **Identifiers**, and then select your application's bundle ID from the displayed list.

    A screen similar to the following appears.

    ![Apple Developer account Identifiers](../image/mobsdk-ios-retrieve-cert-1.png)

2.  Select the **Push Notifications** check box and then select **Edit**.

3.  Using the instructions provided by Apple, create a production SSL certificate.

4.  Once created, double-click the downloaded certificate, which saves it to the KeyChain Access application.

5.  From your Applications folder, open the Keychain Access application, and locate the certificate that you created.

6.  Right-click the certificate and then select the **Export** option.

    ![Export Apple Push Services](../image/mobsdk-ios-cert-export.png)

7.  Ensure that the **File Format** field is set to `Personal Information Exchange (.p12)`.

8.  Enter a secure password for the certificate.


