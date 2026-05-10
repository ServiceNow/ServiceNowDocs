---
title: Configure a user action for the article view page
description: Configure a user action for the Knowledge Management article view page in the Knowledge Management Service Portal.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a user action for the article view page

Configure a user action for the Knowledge Management article view page in the Knowledge Management Service Portal.

## Before you begin

Role required: sp\_admin or admin

## About this task

The article view page uses the Knowledge Article Content widget to provide user actions. Use the widget instance options to customize these actions.

Ensure that the application scope on the ServiceNow AI Platform is set to Knowledge Management Service Portal.

User actions available for the article view page appear in a menu after clicking the overflow icon \(![Overflow icon](../image/KnowledgeServicePortalOverflowIcon.png)\) in the article header. These actions enable users to flag an article, edit an article, or create an incident for an article.

## Procedure

1.  Navigate to the Knowledge Management Service Portal article view page.

2.  Control + right-click the article header.

3.  Click **Instance Options**.

4.  Configure the desired settings for the Knowledge Article Content widget.

<table id="table_KM_SP_filter_facet_widgets"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Bootstrap color

</td><td>

The color of the widget header.

</td></tr><tr><td>

CSS

</td><td>

Custom configurations that determine the look and feel of the elements in the widget. For more information, see [Service Portal SCSS Primer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/scss-primer.md).

</td></tr><tr><td>

Hide All Actions

</td><td>

Hides the user actions in the article header including the **Subscribe/Unsubscribe** button and the overflow icon.

</td></tr><tr><td>

Show Version Information

</td><td>

Displays version information for the selected article. Requires the Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\).

</td></tr><tr><td>

Show Create Incident Action

</td><td>

Displays the **Create Incident** user action when a user clicks the overflow icon in the article header.

</td></tr><tr><td>

Create Incident Action Label

</td><td>

The label for the user action that appears in the overflow icon menu. The default is **Create Incident**.

</td></tr><tr><td>

Create Incident Action URL

</td><td>

The target URL for the **Create Incident** user action. If no URL is specified, the system uses the URL in the **glide.knowman.create\_incident\_link** system property.

</td></tr><tr><td>

Redirect to the latest article

</td><td>

Redirects the article view page to the latest accessible version of the article, if available. Disable the **Show Version Information** option to hide the version information on the article view page because any version link will redirect to the latest version only.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

