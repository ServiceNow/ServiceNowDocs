---
title: Properties installed with Content Publishing
description: The Content Publishing \[com.sn\_content\_delivery\] plugin adds the following properties that are designed to control how scheduled jobs work in relation to notifications, to-dos, and communities.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-09-04"
reading_time_minutes: 9
breadcrumb: [Reference, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Properties installed with Content Publishing

The Content Publishing \[com.sn\_content\_delivery\] plugin adds the following properties that are designed to control how scheduled jobs work in relation to notifications, to-dos, and communities.

To modify Content Publishing properties as a Content Admin \[sn\_cd.content\_admin\], navigate to **Content Publishing** &gt; **Advanced** &gt; **Properties**.

Content Publishing properties determine how the scheduled jobs run and help to ensure that there is limited impact on the performance of your instance.

|Properties|Description|Default Value|
|----------|-----------|-------------|
|sn\_cd.all\_must\_approve|Indicates that all approvers must approve any scheduled content prior to publishing it. If you check No, only one approver is required to publish it.|Yes|

<table id="table_y22_1ky_lnb"><thead><tr><th>

Properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

Allow Ownership for Audiences \(sn\_cd.activate\_audience\_delegation\_controls\)

</td><td>

Indicates you want to be able to enable audience ownership within Content Publishing.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td><td>

No

</td></tr><tr><td>

Allow Ownership for Content Items \(sn\_cd.activate\_content\_authoring\_controls\)

</td><td>

Indicates you want to be able to enable content item ownership within Content Publishing.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td><td>

No

</td></tr><tr><td>

Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\)

</td><td>

Indicates you want to enable topic ownership within Content Publishing.Ownership of a topic includes:

-   Ability to restrict what groups or users can schedule content for publication.
-   Ability to edit content assigned to the topic.
-   Ability to preview content for the topic.

**Note:** Other users that have access to the content can view the content scheduled to the restricted topic, but cannot remove the topic from the schedule.

For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td><td>

No

</td></tr><tr><td>

Allow Ownership for Portal pages \(sn\_cd.activate\_page\_ownership\)

</td><td>

Indicates you want to exclude groups or non-applicable content managers \(specific users\) from assigning content to a specific portal page.

</td><td>

No

</td></tr></tbody>
</table>|Properties|Description|Default Value|
|----------|-----------|-------------|
|sn-cd.activate\_content\_snapshots|Select the checkbox to enable Content Versioning for the Content Library. See [Content versioning](../concept/ec-content-versioning.md)|Yes|

<table id="table_uxj_qz3_jdb"><thead><tr><th>

Properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

sn\_cd.notification.max\_run\_time

</td><td>

The maximum amount of time \(in seconds\) the Content Publishing: Send notifications scheduled job runs. Limits the length of the scheduled job, but completes any work in progress and does not pick up any new work.

</td><td>

-   Max run time in seconds \(notifications\) is 600
-   Number of seconds to stagger events \(notifications\) is 60
-   Max number of events to queue \(notifications\) is 50
-   Max number of users processsed per email event \(notifications\) is 1000

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_recipients

</td><td>

The maximum number of people you can send an SMS notification to. **Note:** When the maximum is exceeded, the SMS is not sent. The **Notification status** on the Schedule Content form is **Max Exceeded**.

</td><td>

Max number of 50,000

</td></tr><tr><td>

sn\_cd.sms\_notification.max\_users\_per\_event

</td><td>

The maximum number of users to add per event for an SMS notification.

</td><td>

Max number of users processed per email is 1000

</td></tr><tr><td>

sn\_cd.notification.event\_stagger

</td><td>

The amount of time between events when a scheduled job runs. Staggering provides time for the events to be processed during the staggered time.Default value: 60 seconds.

</td><td>

60 seconds

</td></tr><tr><td>

sn\_cd.notification.max\_events

</td><td>

The maximum number of events from campaigns to process during the scheduled job.

</td><td>

Max number 50

</td></tr><tr><td>

sn\_cd.notification.max\_users\_per\_event

</td><td>

The maximum number of users to add per event for an email notification.

</td><td>

Max number of users processed per email is 1000

</td></tr><tr><td>

sn\_cd.notification.max\_recipients

</td><td>

The maximum number of recipients allowed per email notification.

</td><td>

Max number of 50,000

</td></tr></tbody>
</table>|Properties|Description|Default Value|
|----------|-----------|-------------|
|sn\_cd.todo.max\_run\_time|The maximum run time in seconds for the Content Publishing: Create To-dos scheduled job. When the job finishes running, any current items are still processed after the elapsed time.|Max run time is 600 seconds|
|sn\_cd.todo.event\_stagger|The number of seconds between events.|60 seconds|
|sn\_cd.todo.max\_events|The maximum number of events that are queued per scheduled job run.|Max number of events is 50|
|sn\_cd.todo.max\_users\_per\_event|The maximum number of users that can be added per event.|Max number of users is 1000|
|sn\_cd.todo.max\_assignees|The maximum number of people you can assign to a task.|Max number of assignees is 50,000|

|Properties|Description|Default Value|
|----------|-----------|-------------|
|sn\_cd.content\_community.max\_posts|The maximum number of posts to a forum allowed per Content Publishing: Post to Forums scheduled job.|Max post is 100|
|sn\_cd.audience.autocount\_timeout|Maximum number of seconds to wait for the automatic audience count while configuring an audience record.|Max is 2 seconds|

<table id="table_oyq_ln3_wtb"><thead><tr><th>

Properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

sn\_cd.enable\_language\_switching

</td><td>

Allows you to change your system setting language in the Content Library.When you turn this system property on, the **Switch language** button appears after creating content from the Content Library.

 Selecting the **Switch language** button allows you to view the fields on the form to appear in the language you select. You can select the button after reviewing to switch back to your original language.

 For more information, see [Portal content](../concept/ec-streamline-content.md).

</td><td>

No

</td></tr><tr><td>

sn\_cd.enable\_localization\_framework\_integration

</td><td>

Enables integration with Localization Framework. For more information, see [Configure Localization Framework for Content Publishing](../concept/ec-int-localization-framework.md).

</td><td>

No

</td></tr></tbody>
</table><table id="table_vlv_zz3_wtb"><thead><tr><th>

Properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

Service Portal URL suffix you want to use for portal previews \(sn\_cd.preview.portal\_url\_suffix\)

</td><td>

The URL suffix of the service portal or Employee Center \(EC\) your company uses for portal previews.You can change this system property when you want to preview your content on a different portal.

</td><td>

esc

</td></tr></tbody>
</table>|Properties|Description|Default Value|
|----------|-----------|-------------|
|Limits how many news articles are shown in the News widgets \(sn\_cd.content\_page\_limit\)|Sets a maximum of news articles that can appear in any of the news widgets, with a system maximum of 500 articles.|Max articles in widgets is 200|
|Page ID you want to use for News Center \(sn\_cd.news\_center\_page\_id\)|Defines the landing page for news content. The **News Center** button in the main navigation redirects to this page, as well as breadcrumbs and the Call to action button in the widgets.|cd\_news\_center|
|Page ID you want to display News articles in \(sn\_cd.news\_article\_page\_id\)|Defines the page where a full news article is viewed. When a user clicks a news article in a News widget, the widget redirects to this page.|cd\_news\_article|
|Sys ID \(sys\_id\) from the Record Section \(sys\_sg\_item\_section\) table for where news articles will be displayed in the mobile app \(sn\_cd.mobile\_record\_section\)|Defines the section in the mobile app where the news article is viewed.|10a5286777403110cd1b756f1b5a99e2|

|Properties|Description|Default Value|
|----------|-----------|-------------|
|Enables the ability to edit the HTML and CSS within a Rich Content design \(sn\_cd.activate\_rce\_edit\_code\)|Select **Yes** to allow content managers to edit rich content source code.|No|

|Properties|Description|Default Value|
|----------|-----------|-------------|
|The number of seconds to wait before timing out a video content provider subflow \(sn\_cd.provider\_timeout\)|Sets the period of time that the Employee Center attempts to connect to the video content provider. See [Video hosting integrations framework](../concept/content-providers.md)|20 seconds|

<table id="table_mxg_gxv_sbc"><thead><tr><th>

Properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

Allow comments \(sn\_cd.allow\_comments\)

</td><td>

Displays a checkbox in the new content and content template forms for content managers to allow employees to comment on news articles

</td><td>

Yes

</td></tr><tr><td>

Allow replies to comments \(sn\_cd.allow\_replies\_to\_comments\)**Important:** This property is not currently connected to any functionality and might be removed in future releases.

</td><td>

Displays a checkbox in the new content and content template forms for content managers to allow employees to reply to comments on news articles

</td><td>

Yes, but currently unused

</td></tr><tr><td>

Allow reactions \(sn\_cd.allow\_reactions\)

</td><td>

Displays a checkbox in the new content and content template forms for content managers to allow employees to select a reaction icon

</td><td>

Yes

</td></tr><tr><td>

Show view count \(sn\_cd.show\_views\)

</td><td>

Displays the number of unique views for a news article at the top of the article

</td><td>

Yes

</td></tr></tbody>
</table>|Properties|Description|Default Value|
|----------|-----------|-------------|
|sn\_cd.enable\_precomputed\_audiences|Enables precomputed audiences for Company Events.|Yes|
|sn\_cd.audience\_count\_threshold|Sets the threshold for the number of users that will automatically put the portal into performance mode.|5000|
|sn\_cd.performance\_portal\_navigation|Sets an Advanced portal navigation sys\_id to use when a Company event is a surge event and is live.|92de6ac87f8a1210a3a9fac8fc86651e|
|sn\_cd.high\_performance\_event\_buffer|Specify the number of minutes in advance for triggering the high-traffic event.|30|
|sn\_cd.company\_event\_article\_page\_id|Page ID to display Company Event articles.|cd\_company\_event|
|sn\_cd.high\_traffic\_event\_modal|Display the event modal on the home page when a high-traffic event is in progress.|No|
|sn\_cd.high\_traffic\_event\_degraded\_experience|The view displayed for widgets when a high-traffic event is in progress.|Default view|

**Parent Topic:**[Employee Center Pro reference](emp-center-pro-reference.md)

**Related topics**  


[Approvals experience reference](approval-hub-ootb.md)

[Block content form](block-content-form.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Experiences](installed-with-content-auto.md)

[Components installed with Content Publishing](installed-with-content-delivery.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Employee Center Pro widgets](employee-center-pro-widgets-list.md)

[Feedback Analytics dashboard](../concept/ex-fdback-board.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Link content form](link-content-form.md)

[Location Consent form](location-consent-form.md)

[Notification content form](notification-content-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Schedule appointment form](schedule-appointment-form.md)

