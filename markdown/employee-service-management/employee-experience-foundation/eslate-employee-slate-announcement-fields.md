---
title: Employee Slate announcement form
description: Field descriptions for creating and configuring Employee Slate announcements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-employee-slate-announcement-fields.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-04-02"
reading_time_minutes: 2
keywords: [announcement fields, Employee Slate, content library, form reference]
breadcrumb: [Employee communications, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Employee Slate announcement form

Field descriptions for creating and configuring Employee Slate announcements.

## Announcement details

To create an announcement, see [Create an announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Headline

</td><td>

Short title that appears in the Employee Comms widget and in any chat promotion.

</td></tr><tr><td>

Body copy

</td><td>

Supporting text displayed when an employee opens the announcement.

</td></tr><tr><td>

Image

</td><td>

Thumbnail image with an adjustable focal point. The focal point controls how the image renders correctly across widget aspect ratios.

</td></tr><tr><td>

Focal point

</td><td>

Positioning coordinates for the image focal point. You can set this by clicking and dragging within the image preview or entering precise coordinates.

</td></tr><tr><td>

Link

</td><td>

Link to a knowledge article, catalog item, or external URL. Links are managed through the ServiceNow reusable links table.

</td></tr><tr><td>

Link label

</td><td>

Label text for the link. This appears in accessibility contexts and promotional channels but not in the main widget display.

</td></tr><tr><td>

Link target

</td><td>

Specifies whether the link opens in the current tab or a new tab.

</td></tr><tr><td>

Content priority

</td><td>

Priority level that controls ordering in the widget carousel. Options include Critical, High, Medium, and Low. Priority combines with freshness to determine display order.

</td></tr><tr><td>

Start date

</td><td>

Start date for the announcement visibility.

</td></tr><tr><td>

Start time

</td><td>

Time to make the announcement visible on the start date.

</td></tr><tr><td>

End date

</td><td>

Date when the announcement stops being visible.

</td></tr><tr><td>

End time

</td><td>

Time when the announcement stops being visible on the end date.

</td></tr><tr><td>

Audience

</td><td>

Audience targeting for the announcement. When no audience is set, the user criteria on the linked knowledge article or catalog item apply.

</td></tr><tr><td>

Chat promotion

</td><td>

Selected to promote the announcement through configured chat channels such as Microsoft Teams.**Note:** For chat promotion, verify that the channel is integrated with Virtual Agent and channel notification is enabled.

</td></tr><tr><td>

Promotion title

</td><td>

Title text for chat promotion. This field appears only when chat promotion is selected.

</td></tr><tr><td>

Promotion body

</td><td>

Body text for chat promotion. This field appears only when chat promotion is selected.

</td></tr><tr><td>

Promotion schedule

</td><td>

Date and time when the chat promotion is sent. This can be independent of the publishing window.

</td></tr></tbody>
</table>## Content priority levels

To create an announcement through chat, see [Conversational authoring for announcements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-conversational-authoring-announcements.md).

|Priority level|Behavior|
|--------------|--------|
|Critical|Highest priority level. Critical announcements appear first in the carousel, but newer high-priority content can still appear ahead of older critical content.|
|High|High priority level. Balances with content freshness to determine position in the carousel.|
|Medium|Default priority level for announcements created from existing content.|
|Low|Lowest priority level. Low-priority announcements typically appear later in the carousel unless they are very recent.|

