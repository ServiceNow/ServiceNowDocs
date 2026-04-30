---
title: Properties installed with Content Experiences
description: The Content Experiences \[sn\_ca\] plugin adds properties that determine how a campaign runs related to scheduled jobs and performance.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [Reference, Employee Center, Employee Service Management]
---

# Properties installed with Content Experiences

The Content Experiences \[sn\_ca\] plugin adds properties that determine how a campaign runs related to scheduled jobs and performance.

To access Content Experiences properties, navigate to **Content Experiences** &gt; **Configurations** &gt; **Properties**.

Content Experiences properties determine how the scheduled jobs run and help to ensure that there is limited impact on the performance of your instance.

**Note:** Properties with an asterisk \(\*\) in front of the name indicates that the default values are recommendations when the number of users targeted is 100,000 or less. If your audience is over 100,000 and the scheduled jobs run longer than expected, you can try increasing the values.

|Property|Usage|
|--------|-----|
|All approvers must approve any schedule content record to publish it \(sn\_ca.all\_must\_approve\)|Indicates that all approvers must approve any scheduled content prior to publishing it. If you check **No**, only one approver is required to publish a campaign.|

<table id="table_btz_j1r_gnb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Allow Ownership for Audiences \(sn\_cd.activate\_audience\_delegation\_controls\)

</td><td>

Indicates you want to be able to enable audience ownership within Content Experiences.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Content Items \(sn\_cd.activate\_content\_authoring\_controls\)

</td><td>

Indicates you want to be able to enable content item ownership within Content Experiences.For more information, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Topics \(sn\_cd.activate\_topic\_ownership\)

</td><td>

Indicates you want to enable topic ownership within Content Experiences.Ownership of a topic includes:

-   Ability to restrict what groups or users can schedule content to a topic for a campaign.
-   Ability to edit content assigned to the topic.
-   Ability to preview content for the topic.

**Note:** Other users that have access to the content can view the content scheduled to the restricted topic, but cannot remove the topic from the schedule.

 For more information on this and what roles are required, see [Content Ownership](../concept/ecpro-content-restriction.md).

</td></tr><tr><td>

Allow Ownership for Portal pages \(sn\_cd.activate\_page\_ownership\)

</td><td>

Indicates you want to exclude groups or non-applicable content managers \(specific users\) from assigning content to a specific portal page.

</td></tr></tbody>
</table><table id="table_j5x_mgg_hsb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

\*Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.add\_users.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Update Campaign Audience scheduled job runs. Limits the length of the scheduled job, but completes any work in progress and does not pick up any new work.Default value: 1,800 seconds

</td></tr><tr><td>

The number of seconds to stagger events to process campaigns by \(sn\_ca.add\_users.event\_stagger.campaign\)

</td><td>

The amount of time between campaign events when a scheduled job runs. Staggering provides time for the events to be processed during the staggered time.Default value: 300 seconds

</td></tr><tr><td>

The number in seconds to stager events to add user by \(sn\_ca.add\_users.event\_stagger.users\)

</td><td>

The amount of time between campaign events to add users when the Content Experiences: Update Campaign Audience scheduled job runs. Staggering provides time for the events to be processed during the staggered time.Default value: 3 seconds

</td></tr><tr><td>

Max number of events to add users per campaign \(sn\_ca.add\_users.max\_events\)

</td><td>

The maximum number of events that users can be added for a campaign when the Content Experiences: Update Campaign Audience scheduled job runs. Default value: 1,000

</td></tr><tr><td>

Max number of users to add per event \(sn\_ca.add\_users.max\_users\_per\_event\)

</td><td>

The maximum number of users you can add in a single event.Default value: 1000

</td></tr></tbody>
</table><table id="table_u3z_ssh_jdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

\*Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.campaign.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Add Non-Portal Campaign Content scheduled job runs. Limits the length of the Content Experiences: Send Email Notifications scheduled job, but completes any work in progress and does not pick up any new work.

 Default value: 2,700 seconds

</td></tr><tr><td>

\*Max number of campaign targets to process per job run \(sn\_ca.campaign.max\_records\_process\)

</td><td>

The maximum number of people a campaign can target per scheduled job run.Default value: 100,000

</td></tr><tr><td>

\*Max number of records to create per job run \(sn\_ca.campaign.max\_records\_create\)

</td><td>

The maximum number of records to create per job run.Default value: 100,000

</td></tr><tr><td>

The number of seconds to stagger events to process pending content by \(sn\_ca.campaign.pending.event\_stagger\)

</td><td>

The number of seconds between each time the Content Experiences: Add Non-Portal Campaign Content scheduled job runs to try to send non-portal content.Default value: 3 seconds

</td></tr></tbody>
</table>|Note|
|----|
|These properties determine limits on non-portal content \(emails and SMS\). The Content Experiences: Send Email Notifications scheduled job runs every hour by default and attempts to send non-portal content not sent in the first pass. Customers with a large database should consider increasing this property after testing the impact it could have on performance.|

<table id="table_pfm_zhv_gfb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Max run time in seconds of scheduled job \(Job will finish processing current item after time as has elapsed\) \(sn\_ca.task.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Create To-dos scheduled job runs. Limits the length of the scheduled job, but completes any work in progress and does not pick up any new work.Default value: 300 seconds

</td></tr><tr><td>

Max number of records to create per job run \(sn\_ca.task.max\_records\_create\)

</td><td>

The maximum number of records to create per scheduled job run.Default value: 25,000

</td></tr></tbody>
</table><table id="table_rty_qph_jdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

The maximum number of users to add per event for SMS \(sn\_ca.sms\_notification.max\_users\_per\_event\)

</td><td>

The maximum number of users to add per event for an SMS notification.Default value: 1,000

</td></tr><tr><td>

\*Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.notification.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Send Email Notifications, Content Experiences: Send Push Notifications, Content Experiences: Send SMS Notifications scheduled jobs run.Default value: 1,800 seconds

</td></tr><tr><td>

\*The maximum number of events to queue per job run for SMS \(sn\_ca.sms\_notification.max\_events\)

</td><td>

The maximum number of events to queue for SMS messages when the Content Experiences: Send Email Notifications, Content Experiences: Send Push Notifications, Content Experiences: Send SMS Notifications scheduled jobs run.Default value: 100

 **Note:** The Notify \(com.snc.notify \) plugin must be activated for this sys property and Content Experiences: Send SMS Notifications scheduled job to appear.

</td></tr><tr><td>

The number of seconds to stagger events by \(sn\_ca.notification.event\_stagger\)

</td><td>

The amount of time between events when the Content Experiences: Send Email Notifications, Content Experiences: Send Push Notifications, Content Experiences: Send SMS Notifications scheduled jobs run. Staggering provides time for the events to be processed during the staggered time.Default value: 3 seconds

</td></tr><tr><td>

\*The maximum number of events to queue per job run for Email \(sn\_ca.notification.max\_events\)

</td><td>

The maximum number of events to queue for the Content Experiences: Send Email Notifications, Content Experiences: Send Push Notifications, Content Experiences: Send SMS Notifications scheduled jobs run.Default value: 100

</td></tr><tr><td>

The maximum number of events to queue per job run for Email \(sn\_ca.notification.max\_events\)

</td><td>

The maximum number of events to queue per job run for email notifications.Default value: 100

</td></tr><tr><td>

The maximum number of users to add per event for Email \(sn\_ca.notification.max\_users\_per\_event\)

</td><td>

The maximum number of users to add per event for email notifications.Default value: 1,000

</td></tr></tbody>
</table><table id="table_fb5_5ph_jdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

The number of seconds to stagger the sn\_ca.campaign.published event after kicking off the Create To-Dos and Send Notifications Flow Designer Actions. Default is 2700 seconds or 45 minutes. \(sn\_ca.campaign.published.event\_stagger\)

</td><td>

Determines the time to delay the publication of a campaign after the Create To-Dos and Send Notifications Flow Designer Actions are started.This sys property determines when the state of a campaign is set back to Published after going through the other states. The Published state is required for the scheduled jobs to pick up for future processing.

 Default value: 2700 seconds or 45 minutes.

</td></tr><tr><td>

Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.state\_management.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Manage Content States scheduled job runs.Default value: 300 seconds

</td></tr><tr><td>

Used to manage whether we want to trigger the campaign publishing process immediately after publishing the campaign. \(sn\_ca.publish.campaign.immediately\)

</td><td>

Check **Yes** to indicate you want a campaign to trigger immediately after selecting the Publish button.Checking **Yes** is recommended for campaigns targeting less than 100,000 users.

 **Note:** Selecting **Yes** bypasses the scheduled jobs and is dependent on the start date and time.

</td></tr><tr><td>

Max number of records to update per job run \(sn\_ca.state\_management.max\_records\_update\)

</td><td>

The maximum number of records to update per job run.Default value: 25,000

</td></tr></tbody>
</table><table id="table_uq4_bqh_jdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.user\_deactivation.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Deactivate Campaign Users scheduled job runs.The scheduled job deactivates flagged users.

 Default value: 300 seconds

</td></tr><tr><td>

Max number of users to deactivate per job run \(sn\_ca.user\_deactivation.max\_users\_per\_job\)

</td><td>

The maximum number of users to deactivate per job run.The Content Experiences: Deactivate Campaign Users scheduled job runs every six hours by default.

 Default value: 25,000 users

</td></tr></tbody>
</table>|Note|
|----|
|These properties determine limits on the Content Experiences: Deactivate Campaign Users scheduled job for optimal performance. Customers with a large database should consider increasing this property after testing the impact it could have on performance.|

<table id="table_e2s_tqh_jdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Max run time in seconds of scheduled job \(Job will finish processing current item after time has elapsed\) \(sn\_ca.purging.max\_run\_time\)

</td><td>

The maximum amount of time \(in seconds\) the Content Experiences: Purge Campaign Data scheduled job runs.Default value: 300 seconds

</td></tr><tr><td>

Max number of users to purge per job run \(sn\_ca.purging.max\_users\_per\_job\)

</td><td>

The maximum number of users to purge per job run.Default value: 25,000

</td></tr><tr><td>

Purge campaign data after the campaign ends \(sn\_ca.purging.purge\_after\_campaign\_end\)

</td><td>

Purge all campaigns when the end date is reached.Default value: Yes

</td></tr><tr><td>

Number of days after the campaign ends to start purging campaign data \(sn\_ca.purging.days\_after\_campaign\_end\)

</td><td>

The number of days after the campaign end date when campaigns are purged.Default value: 180 days

</td></tr><tr><td>

Purge campaign data for a user after user exits campaign \(sn\_ca.purging.purge\_on\_user\_removed\)

</td><td>

Indicates if campaign information for a user should be purged after the user is removed from the campaign.Default value: Yes

</td></tr><tr><td>

Number of days after user exits campaign to start purging campaign data \(sn\_ca.purging.days\_after\_user\_removed\)

</td><td>

The number of days after a user is removed from a campaign to remove the campaign information.Default value: 180 days

</td></tr></tbody>
</table>## Campaign Re-evaluation

<table id="table_ppw_ztq_zjb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

The number of days after which the campaign audience to be re-evaluated \(sn\_ca.campaign.reevaluation\_frequency\)

</td><td>

The default number of days to re-evaluate a campaign audience.You can override this default from the **Re-evaluate campaign** and **Re-evaluate frequency** fields on the Campaign form. For more information, see [View campaign targets](../task/manage-campaign-targets.md).

 Default value: 7 days

</td></tr></tbody>
</table>## Portal Preview

<table id="table_wgq_rtw_n4b"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

Service Portal URL suffix you want to use for portal previews \(sn\_cd.preview.portal\_url\_suffix\)

</td><td>

The URL suffix of the service portal or Employee Center \(EC\) your company uses for portal previews.You can change this system property when you want to preview your content over different portals.

 Default value: esc

</td></tr></tbody>
</table>**Parent Topic:**[Employee Center reference](emp-center-reference.md)

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

