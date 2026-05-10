---
title: Displaying campaigns on ServiceNow mobile
description: Use campaigns to deliver messages and important information to your users. You can set up and display a campaign on ServiceNow mobile.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Displaying campaigns on ServiceNow mobile

Use campaigns to deliver messages and important information to your users. You can set up and display a campaign on ServiceNow mobile.

Mobile campaigns enable you to share curated content using a scrolling list of images. You can mix any of three card types in the carousel: video, image, and text. At the bottom of the campaign cards, dots represent up to eight cards and numbers more than eight cards. A mobile campaign, with its carousel format, is most effective when displayed at the top of the mobile home page.

**Note:**

To set up a campaign to display on mobile devices, you must have the Employee Center Pro Content Publishing plugin \[com.sn\_content\_delivery\] installed. For more information, see [Activate Content Publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/activate-content-delivery-plugin.md).

You create campaign content through Content Experiences with Employee Center Pro. For more information, see [Campaigns for Content Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-campaigns.md) and [Configure mobile content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ecpro-content-delivery-mobile.md).

![Mobile campaign example with an image, text, and video card](../image/campaigns-3-diff-egs.png "Examples of a mobile campaign with an image, text, and video card")

## Displaying mobile campaign process

Content for campaigns include videos, images \(banners\), and text cards.

You specify how to display the cards within a mobile campaign by first creating templates that provide information about the appearance of cards. Once you have defined the card appearances, you build and link components to use the data provided by the item views and display the content as a campaign on your mobile device.

This process involves multiple components contained in a content UI section:

-   An item view for each type of content card, which serves as a template for the appearance of the three types of cards: video, image, and text.
-   An item configuration for each type of content card, which contains the item view.
-   An item stream that contains the data item, which collects the relevant content for the campaign, and the item configuration.
-   An item stream container, which references the item stream.

