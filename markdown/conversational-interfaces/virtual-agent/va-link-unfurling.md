---
title: Using link unfurling in Virtual Agent
description: Virtual Agent supports link unfurling on the chat widget, mobile devices, and various channels. Link unfurling generates a content-rich preview when a supported link is shared in a conversation with a user, a virtual agent, or in a text-based bot response.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [Using, link, unfurling, Virtual Agent, chat widget, mobile devices, preview]
breadcrumb: [Exploring other Virtual Agent features, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Using link unfurling in Virtual Agent

Virtual Agent supports link unfurling on the chat widget, mobile devices, and various channels. Link unfurling generates a content-rich preview when a supported link is shared in a conversation with a user, a virtual agent, or in a text-based bot response.

If the link is supported on the chat widget or channel, the generated content-rich previews can include text, images, and videos.

**Note:** Factors such as website availability, security policies, or response time of the link you want to unfurl are unpredictable. As a result, link unfurling may be delayed or unavailable. However, these performance-related issues don’t impact the user and don't affect the conversation flow.

## How to determine if a link is supported

The ServiceNow user interface currently supports link unfurling for OG tags only. A link is supported only if all the following conditions are met:

-   The host or domain is included in the Hostname allow list table.
-   The link uses standard, compliant [Open Graph \(OG\) tags](https://ogp.me/) in the page header as metadata. For example, og:image.
-   The link was shared in a conversation with a user, a virtual agent, or in a text-based bot response.

    **Note:** These conditions apply only to the chat widget and mobile devices on the ServiceNow® platform. Support requirements and conditions for clients on other platforms can vary. For client-specific support and requirement conditions, see the documentation for the client you're using.


**Tip:** Admins can add OG tags to ServiceNow UI pages by following the instructions in the [Adding meta tags to ServiceNow UI Pages](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0792431) Knowledge Base article.

When a link meets the specified criteria, the ServiceNow software does the following:

-   Asynchronously fetches, if available, the OG tag at the provided link.
-   Attaches a card-based, content-rich preview of the link based on the OG tag.

The time required to complete these and any other required tasks can vary, depending on your network configuration and system performance.

## Supported OG tags

The ServiceNow user interface supports image, video, and text-based OG tags. When both an image OG tag and a video OG tag are fetched, the video is used instead of the image in the card-based, content-rich preview.

**Note:** The specific OG tags supported on channels can vary. For example, the OG tags supported on Slack may be different from the OG tags supported on Microsoft Teams, or Workplace from Facebook. For details about the OG tags supported on channels, see the documentation for the channel you're using.

## Disabling link unfurling

Link unfurling is automatically enabled by default. To turn it off, Maint users change the **com.glide.cs.enable\_link\_unfurling** system property to **False**.

-   **[Configure link unfurling using the Hostname allow list table](../task/configure-link-unfurling-hostname-allow-list.md)**  
Use the Hostname allow list \[sys\_cs\_hostname\_allow\_list\] table to identify the list of hosts and domains that can be unfurled.

**Parent Topic:**[Exploring other Virtual Agent features](exploring-other-vad-features.md)

