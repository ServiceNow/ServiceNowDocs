---
title: Understand the Content Operations dashboard
description: The Content Operations dashboard is a launchpad for content authors, where they can create content, view engagement metrics for published content, content publishing calender, incoming content requests, and review ownership for pages and widgets.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Managing content requests, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Understand the Content Operations dashboard

The Content Operations dashboard is a launchpad for content authors, where they can create content, view engagement metrics for published content, content publishing calender, incoming content requests, and review ownership for pages and widgets.

## Dashboard overview

Users with the Content Manager role can access the **My Content Operations** dashboard from Content Publishing, Content Experiences, or Content Governance as their starting point for creating or managing content.

**Note:** The admin must install the following plugins \(August 2024 store release or later\) to enable this dashboard:

-   Content Publishing
-   Content Governance
-   Content Experiences \(optional\)

For more information, see [Employee Center plugins](install-plugins.md).

## My Content

The my content tab contains metrics on the content you created. The display may vary depending on the plug-ins in your instance.

<table id="table_ayp_rpr_wbc"><thead><tr><th>

Card

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My Content

</td><td>

List of all the content you created.

</td></tr><tr><td>

Content Library and Campaigns

</td><td>

Provides a quick view of the status of your scheduled content and campaign content \(if the Content Experiences plugin is installed\) via the following cards:-   **Content to be published**: The number of your content items that are scheduled but not yet published on the portal or Now mobile app.

Click this card to open the Schedule content records.

-   **Content expiring within 7 days**: The number of your content items with a schedule end date within seven days.
-   **Campaign content to be published**: The number of your content items that are in a campaign bundle.
-   **Campaign content expiring within 7 days**: The number of your currently-published content items that are in bundles with an end date within seven days.

**Note:** The Content Admin can change the number of days for the **Content expiring** and **Campaign content expiring** fields by modifying the Content Governance properties. See [Properties installed with Content Governance](../reference/properties-installed-content-governance.md).

</td></tr><tr><td>

Content requests

</td><td>

Provides a quick view of content requests via the following cards:-   **Content requests unassigned**: Incoming content requests that do not have an assigned user.
-   **Content requests due within 7 days**: Assigned and unassigned content requests with a due date within seven days.
-   **Content requests in progress**: Content requests that have an associated content item and an **in progress** status.
-   **Content requests in review**: Content requests that are awaiting approval from the user who requested the content or from additional reviewers.
-   **Content requests ready to publish**: Approved content requests that have a content item with a content schedule record.

**Note:** The Content Admin can change the number of days for the **Content requests due** field by modifying the Content Governance properties. See [Properties installed with Content Governance](../reference/properties-installed-content-governance.md).

</td></tr></tbody>
</table>## Publishing Calendar

The publishing calender provides a single interface where content managers can view what content will be published and where, upcoming campaigns, and content requests by due date.

![The publishing calendar includes filters to narrow the content displayed](../images/content-ops-calendar.png)

<table id="table_lsx_pmr_wbc"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View type

</td><td>

Narrow the items displayed on the calendar to show:-   Content requests

The Content request appears on the Content request item due date. For more information, see [Managing content requests](ec-content-governance.md).

-   Content Library

Content appears based on the content schedule record, with the exception of news articles and to-do content, which are explained in the **Channel type** section below.

**Note:** The calendar only displays content with configured start date. Content set to "Always active" will not appear in the calendar.

-   Campaign Content

The calendar displays content that is in a published campaign and in a bundle with either an immediate or fixed date trigger. For more information, see [Campaign bundle triggers](../reference/ecpro-triggers.md). The content appears in the calendar based on the bundle date, not the campaign start date.

**Note:** This option appears only if the Content Experiences plugin is installed.

-   Campaign Content

The calendar displays campaign content based on the bundle trigger configuration. For more information, see [Campaign bundle triggers](../reference/ecpro-triggers.md).

**Note:** This option appears only if the Content Experiences plugin is installed.


</td></tr><tr><td>

Channel type

</td><td>

The calendar uses different colors to distinguish between channel types, helping you easily differentiate them. Use the filter to narrow the items displayed on the calendar to show specific content delivery channels.-   Mobile content
-   News content displays based on the article publish start date
-   Notification content
-   Portal content
-   To-do content displays based on the **When to process** date

</td></tr><tr><td>

Page

</td><td>

Narrow the displayed content by portal page.

</td></tr><tr><td>

Widget

</td><td>

Narrow the displayed content by widget instance.The drop-down menu displays Content Publishing widgets. For more information, see [Employee Center widgets](employee-center-widgets-list.md).

</td></tr></tbody>
</table>## Ownership

The ownership tab provides an overview of content, pages, topics, and audience ownership. To learn more about ownership, see [Content Ownership](ecpro-content-restriction.md).

You can use filters to specify a group or user to view information by:

-   **Group**

    The drop-down menu for the group filter contains role-based groups \(Content admin and Content manager\), which include all users with the selected role. These role-based groups are configured at the platform level by a system admin.

-   **User**

    The drop-down menu for the user filter contains all the users with either a Content admin or Content manager role.


|Card|Description|
|----|-----------|
|Owned content|View all the content that you created or have ownership permissions for|
|Owned pages|View all the content that you created or have ownership permissions for|
|Owned topics|View all the topics that you have ownership permissions for|
|Owned audiences|View all the audiences that you have ownership permissions for|

