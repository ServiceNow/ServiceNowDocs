---
title: Employee Slate announcement form
description: Field descriptions for creating and configuring Employee Slate announcements in the content library.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 2
keywords: [announcement fields, Employee Slate, content library, form reference]
breadcrumb: [Employee communications, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Employee Slate announcement form

Field descriptions for creating and configuring Employee Slate announcements in the content library.

## Announcement details

To create an announcement, see [Create an Employee Slate announcement](../task/eslate-create-announcement.md)

|Field|Description|
|-----|-----------|
|Headline|Short title that appears in the Employee Comms widget and in any chat promotion.|
|Body copy|Supporting text displayed when an employee opens the announcement.|
|Image|Thumbnail image with an adjustable focal point. The focal point controls how the image renders correctly across widget aspect ratios.|
|Focal point|Positioning coordinates for the image focal point. You can set this by clicking and dragging within the image preview or entering precise coordinates.|
|Link|Link to a knowledge article, catalog item, or external URL. Links are managed through the ServiceNow reusable links table.|
|Link label|Label text for the link. This appears in accessibility contexts and promotional channels but not in the main widget display.|
|Link target|Specifies whether the link opens in the current tab or a new tab.|
|Content priority|Priority level that controls ordering in the widget carousel. Options include Critical, High, Medium, and Low. Priority combines with freshness to determine display order.|
|Start date|Date when the announcement becomes visible.|
|Start time|Time when the announcement becomes visible on the start date.|
|End date|Date when the announcement stops being visible.|
|End time|Time when the announcement stops being visible on the end date.|
|Audience|Audience targeting for the announcement. When no audience is set, the user criteria on the linked knowledge article or catalog item apply.|
|Chat promotion|Selected to promote the announcement through configured chat channels such as Microsoft Teams.|
|Promotion title|Title text for chat promotion. This field appears when chat promotion is selected.|
|Promotion body|Body text for chat promotion. This field appears when chat promotion is selected.|
|Promotion schedule|Date and time when the chat promotion is sent. This can be independent of the publishing window.|

## Content priority levels

To create an announcement through chat, see [Conversational authoring for announcements](../concept/eslate-conversational-authoring-announcements.md).

|Priority level|Behavior|
|--------------|--------|
|Critical|Highest priority level. Critical announcements appear first in the carousel, but newer high-priority content can still appear ahead of older critical content.|
|High|High priority level. Balances with content freshness to determine position in the carousel.|
|Medium|Default priority level for announcements created from existing content.|
|Low|Lowest priority level. Low-priority announcements typically appear later in the carousel unless they are very recent.|

