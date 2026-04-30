---
title: Mobile photo search
description: Configure photo search to give your users the ability to perform image-based searches using the objects around them.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Global search, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile photo search

Configure photo search to give your users the ability to perform image-based searches using the objects around them.

## Photo searches in your mobile apps

![A photo search used to identify a laptop.](../image/photo-search-example.png)

When photo search is configured on your instance, a photo icon \(![Photo search icon](../image/sg-icon-image-search.png)\) appears in your applet launcher search bar. Your users can tap this icon to use the camera on their mobile device to take a picture. The picture is identified using the Google Vision API, which returns one or more results. Users can select a result, which is used as their search query.

## Google Firebase account

To take advantage of image recognition in your mobile applications, you need a Firebase account with the Google Vision API enabled. Google Firebase and the Google Vision API are third-party services that must be subscribed to separately. Once you have a Firebase account, you can connect that account to your ServiceNow instance by entering your Firebase App ID and Web API key. For details on this process see [Configure photo search](../task/sg-configure-image-search.md).

## Third-party data usage

Images you take using the photo search feature are sent to Google for identification using Google Vision API. ServiceNow does not have control of the image once it has been sent. For details on how Google Vision API handles your image, see [https://cloud.google.com/vision/docs/data-usage](https://cloud.google.com/vision/docs/data-usage).

