---
title: Components installed with Content Publishing
description: Several types of components install with the activation of the Content Delivery \[com.sn\_content\_delivery\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
---

# Components installed with Content Publishing

Several types of components install with the activation of the Content Delivery \[com.sn\_content\_delivery\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Content Publishing \[com.sn\_content\_delivery\] plugin activates the sn\_cd.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Content Publishing admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles installed

The following roles are included when you install Employee Center application \(sn\_ex\_sp\):

<table id="table_qyy_dv2_sqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Content Publishing Admin\[sn\_cd.content\_admin\]

</td><td>

Grants access to all Content Publishing information and privileges.Can access read and write records to the content publishing tables.

 Can add or edit content type.

 Can create or edit Content templates.

Can schedule content for the service portal or Employee Center.

</td><td>

-   Content Publishing Manager \[sn\_cd.content\_manager\]
-   Template Manager \[sn\_cd.content\_template\_owner\]

</td></tr><tr><td>

Content Publishing Manager\[sn\_cd.content\_manager\]

</td><td>

Can create and schedule content for Content Publishing.

</td><td>

None

</td></tr><tr><td>

Template Manager \[sn\_cd.content\_template\_owner\]

</td><td>

Can create and view content templates for news articles.

</td><td>

None

</td></tr><tr><td>

Campaign manager \[sn\_ca.campaign\_manager\]

</td><td>

Provides access to all Content Experiences content. This includes:Creating and scheduling content for the Employee Center and campaigns.

</td><td>

-   sn\_esign.config\_manager
-   sn\_cda.analytics\_reader
-   sn\_cd.content\_approver

</td></tr><tr><td>

Content Publishing Analytics Admin\[sn\_cda.analytics\_admin\]

</td><td>

Required to set up an analytics profile.

</td><td>

None

</td></tr><tr><td>

Content Publishing Analytics Reader\[sn\_cda.analytics\_reader\]

</td><td>

Can access and view analytics reports.

</td><td>

None

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content Publishing: Send Notifications

</td><td>

Sends email notification for a specified audience and specified date.Runs every hour by default.

</td></tr><tr><td>

Content Publishing: Post to Forums

</td><td>

Posts community content to community forums.Runs every hour by default.

</td></tr><tr><td>

Content Publishing: Process To-dos

</td><td>

Creates to-do tasks for assigned audience.Runs every hour by default.

</td></tr><tr><td>

Content Publishing: Send MS Teams Notifications

</td><td>

Sends a scheduled notification to employees in MS TeamsRuns every hour by default.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Audience \[sn\_cd\_audience\]

</td><td>

A targeted group of users.

</td></tr><tr><td>

Audience Data \[sn\_cd\_audience\_data\]

</td><td>

Used when **Audience type** is **Upload File** from the Audience form. Where you store uploaded users.

</td></tr><tr><td>

Block Content\[sn\_cd\_block\]

</td><td>

Reusable content for notifications, rich-text announcements, or community posts \(when you install communities\).

</td></tr><tr><td>

Community Content \[sn\_cd\_content\_community\]

</td><td>

Content posted to a topic or forum in a community. Community content can be:-   Blog
-   Event
-   Video
-   Post list

</td></tr><tr><td>

To-do Content \[sn\_cd\_content\_todo\]

</td><td>

Defines the to-do content.To-do content are tasks assigned to employees that can be a part of a campaign. To-dos can also trigger additional content after completing the initial task.

 Users verify task completion by:

-   Button click
-   Video launch
-   Link click

</td></tr><tr><td>

Content Task \[sn\_cd\_task\]

</td><td>

Extends the HR task \[sn\_hr\_core\_task\] table and where you create tasks for the Employee Center to-dos.

</td></tr><tr><td>

Org Chart Configuration \[sn\_cd\_config\_org\_chart\]

</td><td>

What information appears on the Org Chart.

</td></tr><tr><td>

User Display Configuration \[sn\_cd\_user\_display\_configuration\]

</td><td>

Controls when users display on the Org Chart page and HRI My Team widget in the Employee Center.

</td></tr><tr><td>

Content \[sn\_cd\_content\_base\]

</td><td>

Base table for fields common to Content tables.

</td></tr><tr><td>

News Content \[sn\_cd\_content\_news\]

</td><td>

Company news and announcements published to the portal via widgets.

</td></tr><tr><td>

Notification Content \[sn\_cd\_content\_notification\]

</td><td>

Defines an email blast announcing important news and links directing the user to the service portal.

</td></tr><tr><td>

Portal Content \[sn\_cd\_content\_portal\]

</td><td>

Content or information you make available to your employees on the Employee Center. Content can be a banner, calendar, event, image-based link, rich text, URL, or video.

</td></tr><tr><td>

Content Type \[sn\_cd\_content\_type\]

</td><td>

Classifies the content you want to appear on the Employee Center.Examples are:

-   Community content
-   Portal content
-   Notification content
-   To-do content

</td></tr><tr><td>

Schedule Content \[sn\_cd\_content\_visibility\]

</td><td>

Determines what content appears on the Employee Center, for what audience, and when.

</td></tr><tr><td>

Link Content \[sn\_cd\_url\_asset\]

</td><td>

URL links to information to appear on the Employee Center.

</td></tr></tbody>
</table>## Widgets installed

<table id="table_jm3_3kr_rdb"><thead><tr><th>

Widget

</th><th>

ID

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Announcements \(CD\)

</td><td>

cd-announcements

</td><td>

Shows portal content with content type of Rich Text. Generally, a brief broadcast message and shows in a carousel when there are multiple items.

</td></tr><tr><td>

Category News Feed

</td><td>

cd-news-feed-category

</td><td>

Shows previews of news articles for a specific category.

</td></tr><tr><td>

Content Experience

</td><td>

cd-content-experience

</td><td>

Delivers targeted, actionable communications to employees. For more information, see [Creating campaigns with Content Experiences](../concept/ecpro-campaigns.md).

</td></tr><tr><td>

Content To-do \(CD\)

</td><td>

cd-content-todo

</td><td>

This widget is part of the HR to-do completion process used in the Employee Service Center, but cannot be used as a standalone widget.

</td></tr><tr><td>

Event Calendar \(CD\)

</td><td>

cd-event-calendar

</td><td>

Shows portal content with content type of Calendar. Shows schedules.

</td></tr><tr><td>

Featured News

</td><td>

cd-news-featured

</td><td>

Shows highlighted articles at the top of the News Center.

</td></tr><tr><td>

Information Links \(CD\)

</td><td>

cd-information-links

</td><td>

Shows portal content with content type of URL. Shows hyperlinks.

</td></tr><tr><td>

News Article Detail

</td><td>

cd-news-article-detail

</td><td>

Appears on the Article details page and holds the article body as created in the Rich Content Editor.

</td></tr><tr><td>

News Dataloader

</td><td>

cd-news-dataloader

</td><td>

Can be added to the Article details page to facilitate data sharing between the widgets on the page, which reduces the page loading time.

</td></tr><tr><td>

News Feed

</td><td>

cd-news-feed

</td><td>

Appears on the home page, News Center, and article details pages and holds previews of news articles.

</td></tr><tr><td>

News Header

</td><td>

cd-news-header

</td><td>

Appears on the Article details page and holds the headline, subheadline and image thumbnail.

</td></tr><tr><td>

News Info

</td><td>

cd-news-info

</td><td>

Appears on the Article details page and holds the news article publication date and Copy Link button.

</td></tr><tr><td>

Organization Chart \(CD\)

</td><td>

cd-orgchart

</td><td>

Shows an organization chart of an employee.

</td></tr><tr><td>

Preview Mobile Content \(CD\)

</td><td>

cd-preview-mobile-content

</td><td>

Notifications that show up in mobile view.

</td></tr><tr><td>

Preview of Content To-do \(CD\)

</td><td>

preview\_content\_todos

</td><td>

Shows a preview of to-do content.

</td></tr><tr><td>

Quick Links \(CD\)

</td><td>

cd-quick-links

</td><td>

Shows portal content with content type of Image-based Link. Shows a row of clickable images.

</td></tr><tr><td>

Rich Content \(CD\)

</td><td>

cd-richcontent

</td><td>

Allows you to publish rich content like a long-form article within a widget on the portal \(page or topic\). Shows previews of three pieces of rich content. Appears as a carousel when are there more than three published pieces of rich content.

</td></tr><tr><td>

Styled Content \(CD\)

</td><td>

cd-styled-content

</td><td>

Shows portal content with content type of Styled Content. Shows informative banners or text.You can configure color, alignment, and other options for text and background.

 Appears as a carousel when there are multiple items.

</td></tr><tr><td>

Upcoming Events \(CD\)

</td><td>

cd-upcoming-events

</td><td>

Shows portal content with content type of Event. Shows upcoming events.

</td></tr><tr><td>

Video Carousel \(CD\)

</td><td>

cd-video-carousel

</td><td>

Shows portal content with content type of Video. Multiple videos show in a carousel. You can show a scrolling list of videos using this widget.**Note:** Only YouTube and Vimeo embedded links are supported.

</td></tr><tr><td>

Welcome Banner \(CD\)

</td><td>

cd-banner

</td><td>

Shows portal content with content type of Banner. Generally used to show informative banners/text. Shows in a carousel when there are multiple items.

</td></tr></tbody>
</table>**Note:** These widgets support the Content Experience widget; they are not mean to be used directly in the portal: CD Preview widget, CE Banner content, CE Carousel Layout, CE List Layout, CE Styled Content, and CE Tile Layout.

**Parent Topic:**[Employee Center reference](emp-center-reference.md)

**Related topics**  


[Activity Configuration form](ec-activity-configuration-form.md)

[Activity Configuration Detail form](activity-configuration-detail-form.md)

[Approvals experience reference](approval-hub-ootb.md)

[Block content form](block-content-form.md)

[Browser Extension for Employee Center forms](../concept/ecbe-forms.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Connected Content form](connected-content-form.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Default Employee Profile Header Configuration record](default-profile-header.md)

[Employee Center widgets](../concept/employee-center-widgets-list.md)

[Employee Profile form](employee-profile-fieldconfig.md)

[Employee Profile Header Configuration form](profile-header-config-form.md)

[Employee Profile portal configuration form](profile-portal-config-form.md)

[Employee Profile upgrade scenarios](emp-profile-upgrade.md)

[Enhanced Requests Experience forms](req-concept-ec.md)

[External Link form](external-link-form.md)

[Featured Content form](featured-content-form.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Footer form](ec-footer-form.md)

[Footer Menus form](ec-footer-menus.md)

[Guided Self-Service reference](gss-guided-self-service-reference-info.md)

[Link content form](link-content-form.md)

[Menu Item form](menu-item-form.md)

[Configuring translation for Content Publishing after upgrade](../concept/ec-multiple-language-support.md)

[Notification content form](notification-content-form.md)

[Employee Profile Overview section form](profile-overview-section-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Quick Link form](ec-quick-link-form.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[Tab widget mapping form](tab-widget-mapping-form.md)

[Taxonomy form](taxonomy-form.md)

[To-do content form](to-do-content-form.md)

[Topic form](topic-form.md)

[User Criteria form](ec-user-criteria-form.md)

[User Criteria output](user-criteria-output.md)

