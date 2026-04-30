---
title: Properties installed with Content Publishing
description: The Content Publishing \[com.sn\_content\_delivery\] plugin adds the following properties that are designed to control how scheduled jobs work in relation to notifications, to-dos, and communities.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Reference, Employee Center, Employee Service Management]
---

# Properties installed with Content Publishing

The Content Publishing \[com.sn\_content\_delivery\] plugin adds the following properties that are designed to control how scheduled jobs work in relation to notifications, to-dos, and communities.

To modify Content Publishing properties as a Content Admin \[sn\_cd.content\_admin\], navigate to **Content Publishing** &gt; **Advanced** &gt; **Properties**.

Content Publishing properties determine how the scheduled jobs run and help to ensure that there is limited impact on the performance of your instance.

|Properties|Description|
|----------|-----------|
|sn\_cd.all\_must\_approve|Indicates that all approvers must approve any scheduled content prior to publishing it. If you check No, only one approver is required to publish it.|

<table id="table_y22_1ky_lnb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow Ownership for Audiences \(sn\_cd.activate\_audience\_delegation\_controls\)

</td><td>

Indicates you want to be able to enable audience ownership within Content Publishing.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Content Items \(sn\_cd.activate\_content\_authoring\_controls\)

</td><td>

Indicates you want to be able to enable content item ownership within Content Publishing.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\)

</td><td>

Indicates you want to enable topic ownership within Content Publishing.Ownership of a topic includes:

-   Ability to restrict what groups or users can schedule content for publication.
-   Ability to edit content assigned to the topic.
-   Ability to preview content for the topic.

**Note:** Other users that have access to the content can view the content scheduled to the restricted topic, but cannot remove the topic from the schedule.

 For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Portal pages \(sn\_cd.activate\_page\_ownership\)

</td><td>

Indicates you want to exclude groups or non-applicable content managers \(specific users\) from assigning content to a specific portal page.

</td></tr></tbody>
</table>|Properties|Description|
|----------|-----------|
|sn-cd.activate\_content\_snapshots|Select the checkbox to enable Content Versioning for the Content Library. See [Content versioning](../concept/ec-content-versioning.md)|

<table id="table_uxj_qz3_jdb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cd.notification.max\_run\_time

</td><td>

The maximum amount of time \(in seconds\) the Content Publishing: Send notifications scheduled job runs. Limits the length of the scheduled job, but completes any work in progress and does not pick up any new work.Default value: 600

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_recipients

</td><td>

The maximum number of people you can send an SMS notification to. Default value: 50,000.

**Note:** When the maximum is exceeded, the SMS is not sent. The **Notification status** on the Schedule Content form is **Max Exceeded**.

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_users\_per\_event

</td><td>

The maximum number of users to add per event for an SMS notification. Default value: 1000.

</td></tr><tr><td>

sn\_cd.notification.event\_stagger

</td><td>

The amount of time between events when a scheduled job runs. Staggering provides time for the events to be processed during the staggered time.Default value: 60 seconds.

</td></tr><tr><td>

sn\_cd.notification.max\_events

</td><td>

The maximum number of events from campaigns to process during the scheduled job.Default value: 50.

</td></tr><tr><td>

sn\_cd.notification.max\_users\_per\_event

</td><td>

The maximum number of users to add per event for an email notification.

</td></tr><tr><td>

sn\_cd.notification.max\_recipients

</td><td>

The maximum number of recipients allowed per email notification.

</td></tr></tbody>
</table>|Properties|Description|
|----------|-----------|
|sn\_cd.todo.max\_run\_time|The maximum run time in seconds for the Content Publishing: Create To-dos scheduled job. When the job finishes running, any current items are still processed after the elapsed time.|
|sn\_cd.todo.event\_stagger|The number of seconds between events.|
|sn\_cd.todo.max\_events|The maximum number of events that are queued per scheduled job run.|
|sn\_cd.todo.max\_users\_per\_event|The maximum number of users that can be added per event.|
|sn\_cd.todo.max\_assignees|The maximum number of people you can assign to a task.|

|Properties|Description|
|----------|-----------|
|sn\_cd.content\_community.max\_posts|The maximum number of posts to a forum allowed per Content Publishing: Post to Forums scheduled job.|

<table id="table_oyq_ln3_wtb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cd.enable\_language\_switching

</td><td>

Allows you to change your system setting language in the Content Library.When you turn this system property on, the **Switch language** button appears after creating content from the Content Library.

 Selecting the **Switch language** button allows you to view the fields on the form to appear in the language you select. You can select the button after reviewing to switch back to your original language.

 For more information, see [Content Library](../concept/ec-streamline-content.md).

</td></tr><tr><td>

sn\_cd.enable\_localization\_framework\_integration

</td><td>

Enables integration with Localization Framework. For more information, see [Integration with Localization Framework](../concept/ec-int-localization-framework.md).

</td></tr></tbody>
</table><table id="table_vlv_zz3_wtb"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service Portal URL suffix you want to use for portal previews \(sn\_cd.preview.portal\_url\_suffix\)

</td><td>

The URL suffix of the service portal or Employee Center \(EC\) your company uses for portal previews.You can change this system property when you want to preview your content on a different portal.

 Default value: esc

</td></tr></tbody>
</table>|Properties|Description|
|----------|-----------|
|Limits how many news articles are shown in the News widgets \(sn\_cd.content\_page\_limit\)|Sets a maximum of news articles that can appear in any of the news widgets, with a system maximum of 500 articles.|
|Page ID you want to use for News Center \(sn\_cd.news\_center\_page\_id\)|Defines the landing page for news content. The **News Center** button in the main navigation redirects to this page, as well as breadcrumbs and the Call to action button in the widgets.|
|Page ID you want to display News articles in \(sn\_cd.news\_article\_page\_id\)|Defines the page where a full news article is viewed. When a user clicks a news article in a News widget, the widget redirects to this page.|
|Sys ID \(sys\_id\) from the Record Section \(sys\_sg\_item\_section\) table for where news articles will be displayed in the mobile app \(sn\_cd.mobile\_record\_section\)|Defines the section in the mobile app where the news article is viewed.|

|Properties|Description|
|----------|-----------|
|Enables the ability to edit the HTML and CSS within a Rich Content design \(sn\_cd.activate\_rce\_edit\_code\)|Select **Yes** to allow content managers to edit rich content source code.|

|Properties|Description|
|----------|-----------|
|The number of seconds to wait before timing out a video content provider subflow \(sn\_cd.provider\_timeout\)|Sets the period of time that the Employee Center attempts to connect to the video content provider. See [Video hosting integrations framework](../concept/content-providers.md)|

|Properties|Description|
|----------|-----------|
|Allow comments \(sn\_cd.allow\_comments\)|Displays a checkbox in the new content and content template forms for content managers to allow employees to comment on news articles|
|Allow replies to comments \(sn\_cd.allow\_replies\_to\_comments\)|Displays a checkbox in the new content and content template forms for content managers to allow employees to reply to comments on news articles|
|Allow reactions \(sn\_cd.allow\_reactions\)|Displays a checkbox in the new content and content template forms for content managers to allow employees to select a reaction icon|
|Show view count \(sn\_cd.show\_views\)|Displays the number of unique views for a news article at the top of the article|

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

[Components installed with Content Publishing](installed-with-content-delivery-1.md)

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

[Quick Link form](ec-quick-link-form.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[Tab widget mapping form](tab-widget-mapping-form.md)

[Taxonomy form](taxonomy-form.md)

[To-do content form](to-do-content-form.md)

[Topic form](topic-form.md)

[User Criteria form](ec-user-criteria-form.md)

[User Criteria output](user-criteria-output.md)

