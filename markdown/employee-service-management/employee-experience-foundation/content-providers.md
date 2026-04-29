---
title: Video hosting integrations framework
description: Connect Content Publishing with a video hosting service, to make the hosted videos available for content authoring and publishing.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup employee communications, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Video hosting integrations framework

Connect Content Publishing with a video hosting service, to make the hosted videos available for content authoring and publishing.

Content Publishing offers content managers the ability to build content using videos from a video hosting service. The following components must be configured to add the video hosting service as an option in the Content library.

**Note:** Depending on your organization, either the content admin or a third-party vendor performs these steps.

-   **Content provider**

    A content provider identifies the video hosting service.

    Content Publishing versions 33.0.9 and later include the out-of-the-box provider "other", which enables organizations to skip configuration. Content managers can use this provider to add publicly available videos to microsites and news articles.

-   **Content provider mapping**

    Content provider mapping makes the hosted videos available to a specific content type. Currently, only the rich content and news articles content types are supported.

    Each content provider mapping is associated with a content provider and appears in the related list.

-   **Content processor**

    Content processors provide an interface to configure API calls to the video hosting service. They are powered by subflows from the Flow Designer. For more information, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    There are two actions available:

    -   Authorize: enables employees to view private videos without providing credentials
    -   Search: adds a button to the Rich Content Editor interface that enables a content manager to view thumbnails of available videos, instead of copy-pasting the video URL.
    Each content processor is associated with a content provider mapping and appears in the related list.

-   **Content Rendering parameter**

    A content rendering parameter functions similarly to video hosting URL parameters, allowing content managers to customize the viewer's experience through an interface element in the Rich Content Editor. Depending on the hosting provider, this can include defining a checkbox for enabling full screen or autoplay, or a textbox for specifying the start time.

    Each content rendering parameter is associated with a content provider mapping and appears in the related list.


## Set up content providers

The following process overview guides you through setting up content providers so content managers can use videos from video hosting services when assembling content.

1.  The following domains are available out-of-the-box: youtube.com, player.vimeo.com, vimeo.com,players.brightcove.net, and brightcove.net.

    To configure an additional domain, the system admin must add the host domain to the `glide.html.enable_media_sites` system property. For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

2.  [Configure content provider and mapping](../task/configure-content-provider.md)
3.  \(Optional\) If the video hosting service contains private videos that require credentials, [Configure a video authorization](../task/configure-content-processor.md)
4.  \(Optional\) To provide content managers with an interface where they can select a video, [Configure video content search](../task/configure-content-search.md)
5.  \(Optional\) To add interface elements to the Rich Content Editor video picker, [Configure content rendering parameter](../task/configure-content-rendering-parameter.md)

