---
title: Mobile photo search
description: Configure photo search to give your users the ability to perform image-based searches using the objects around them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/sg-mobile-image-search-user.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile search, Using the mobile apps, Mobile Platform]
---

# Mobile photo search

Configure photo search to give your users the ability to perform image-based searches using the objects around them.

## Photo searches in your mobile apps

\[Omitted image "photo-search-example.png"\] Alt text: A photo search used to identify a laptop.

When photo search is configured on your instance, a photo icon \(\[Omitted image "sg-icon-image-search.png"\] Alt text: Photo search icon\) appears in your launcher screen search bar. Your users can tap this icon to use the camera on their mobile device to take a picture. The picture is identified using the Google Vision API, which returns one or more results. Users can select a result, which is used as their search query.

**Note:** For details on how an administrator can configure photo search, see [Mobile photo search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/sg-mobile-image-search.md).

## Third-party data usage

Images you take using the photo search feature are sent to Google for identification using Google Vision API. ServiceNow does not have control of the image once it has been sent. For details on how Google Vision API handles your image, see [https://cloud.google.com/vision/docs/data-usage](https://cloud.google.com/vision/docs/data-usage).

