---
title: Components installed with Content Experiences
description: Several types of components install with the activation of the Content Experiences \[sn\_cd\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Employee Center Pro reference, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Components installed with Content Experiences

Several types of components install with the activation of the Content Experiences \[sn\_cd\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

For more information about tables, see [Table administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-administration-and-data-management/c_TableAdministration.md).

Demo data is available for this feature.

**Note:** The Content Experiences \[sn\_cd\] plugin activates the sn\_ca.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Content Experiences admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles

The following roles are included when you install the Employee Center application \(sn\_ex\_sp\):

<table id="table_qyy_dv2_sqb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Campaign Approver \[sn\_ca.campaign\_approver\]

</td><td>

When configured, can approve content for a campaign. Requires approval before a campaign publishes.

</td><td>

Content Approver \[sn\_cd.content\_approver\]

</td></tr><tr><td>

Content Admin \[sn\_ca.campaign\_admin\]

</td><td>

Grants access to all Content Experiences information and privileges.Can create, configure, administer, and schedule campaigns.

 Can access read and write records to the Content Experiences tables.

 Can use an analytics tracking profile with a campaign.

**Note:** Does not inherit Content Delivery Analytics Admin \[sn\_cda.analytics\_admin\] role to set up tracking profiles.

</td><td>

Content Experiences Manager \[sn\_ca.campaign\_manager\]

</td></tr><tr><td>

Content Manager \[sn\_ca.campaign\_manager\]

</td><td>

Provides access to all Content Experiences content. This includes:Creating and scheduling content for the Employee Center and campaigns.

</td><td>

-   Campaign Approver \[sn\_ca.campaign\_approver\]
-   sn\_esign.config\_manager
-   sn\_cda.analytics\_reader
-   sn\_cd.content\_approver

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content Experiences: Add Non-Portal Campaign Content

</td><td>

Creates sn\_ca\_campaign\_item\_user\_records for sent emails. It does not send the email.Runs every four hours by default.

</td></tr><tr><td>

Content Experiences: Calculate Campaign Engagements

</td><td>

Calculates the total number of actionable engagements \(videos viewed, links clicked\) recorded divided by the total number possible with an engagement percentage.Runs on a designated repeating interval.

</td></tr><tr><td>

Content Experiences: Campaign Success Criteria

</td><td>

Populates the base count and evaluation period count. Runs the evaluation criteria set up for a campaign.Takes the success goals from published or finished \(end date has passed\) campaigns and evaluates them to calculate the:

-   Baseline count
-   Target count
-   Evaluation count

Evaluation count analyzed against the Target count to determine success.

 Runs daily.

</td></tr><tr><td>

Content Experiences: Create To-dos

</td><td>

Creates to-do tasks for assigned audience for a campaign.Runs every hour by default.

</td></tr><tr><td>

Content Experiences: Deactivate Campaign Users

</td><td>

Deactivates users assigned to a campaign that has ended.Runs every six hours by default.

</td></tr><tr><td>

Content Experiences: Manage Content States

</td><td>

Updates the state of targeted content and marks content as available or expired. For example:-   A Targeted Content record is available starting on 12-01-2019.
-   Today is 11-27-2019.
-   When 12-01-2019 arrives, the state of the targeted content changes from Pending to Ready or Available.
-   If the same content is only available until 12-05-2019 and the date is 12-06-2019, the state of the targeted content changes to Complete or Incomplete.

 Runs every hour and five minutes by default.

</td></tr><tr><td>

Content Experiences: Process SNC analytics

</td><td>

Processes analytics captured using a ServiceNow tracker to update campaign statistics.Runs daily.

**Note:** Available to use if the SNC tracking profile fails to upgrade and work with flow designer.

</td></tr><tr><td>

Content Experiences: Purge Campaign Data

</td><td>

Purges campaigns and users based on the Content Experiences Configurations Properties settings.See the Purging section in [Properties installed with Content Experiences](properties-installed-with-content-auto.md).

 Runs every hour by default.

</td></tr><tr><td>

Content Experiences Profile

</td><td>

Works with the trigger associated with Content Experiences Profile. Processes analytics collected by the Content Experiences Profile tracker to update campaign statistics.Runs daily.

</td></tr><tr><td>

Content Experiences: Send Email Notifications

</td><td>

Sends the emails for a campaign.Runs every hour by default.

</td></tr><tr><td>

Content Experiences: Send Push Notifications

</td><td>

Sends SMS notifications for a campaign.Runs on a designated repeating interval.

</td></tr><tr><td>

Content Experiences: Send MS Teams Notifications

</td><td>

Sends an MS Teams notification for a campaign.Runs every 90 minutes by default.

</td></tr><tr><td>

Content Experiences: Update Campaign Audience

</td><td>

Reevaluates the audience for a campaign and removes employees that no longer satisfy the criteria. Adds users that match your defined criteria to the campaign. Users show up in the Campaign Targets related list for a campaign.

 You can view the updated audience from the Campaign Targets tab of a campaign. See [View campaign targets](../task/manage-campaign-targets.md).

 Runs daily by default.

</td></tr></tbody>
</table>## Tables installed

|Table|Description|
|-----|-----------|
|Campaign \[sn\_ca\_campaign\]|Defines high-level information about a campaign, including the to and from date range a campaign runs and the audience that can view it.|
|Campaign Bundle \[sn\_ca\_campaign\_bundle\]|Grouping mechanism for items that have the same triggering mechanism and availability.|
|Campaign Content \[sn\_ca\_campaign\_item\]|Campaign content associated with a bundle.|
|Targeted Content \[sn\_ca\_campaign\_item\_user\]|Campaign content available to the audience. After a campaign publishes and content is available, users appear under the Campaign Target tab of the campaign,|
|Campaign Target \[sn\_ca\_campaign\_user\]|Who in your company is part of a campaign.|
|Creation Status \[sn\_ca\_creation\_status\]|Tracks whether a campaign target has visited a particular widget instance that is part of the campaign.|

**Parent Topic:**[Employee Center Pro reference](emp-center-pro-reference.md)

**Related topics**  


[Block content form](block-content-form.md)

[Campaign overview and Campaign analytics dashboards](../concept/ecpro-content-automation-content-pack.md)

[Components installed with Employee Center Pro](components-installed-with-employee-center-pro-1.md)

[Components installed with Content engagement](installed-content-engagement.md)

[Components installed with Content Publishing](installed-with-content-delivery.md)

[Components installed with Content Governance](ec-installed-content-governance.md)

[Components installed with Content Analytics](ecpro-installed-content-analytics-1.md)

[Content Analytics dashboards](../concept/content-analytics-dashboards.md)

[Content engagement dashboard](../concept/ec-pro-content-engagement-dashboard.md)

[Content Library Overview dashboard](../concept/content-library-overview-dashboard.md)

[Employee Center Pro widgets](employee-center-pro-widgets-list.md)

[Feedback configuration form](ex-feedback-new-record.md)

[Feedback definition form](fdbck-dfnition-record.md)

[Link content form](link-content-form.md)

[Notification content form](notification-content-form.md)

[Properties installed with Content Experiences](properties-installed-with-content-auto.md)

[Properties installed with Content Governance](properties-installed-content-governance.md)

[Properties installed with Content Publishing](properties-with-content-delivery.md)

[Standard banner and icon sizes](ec-portal-images-size.md)

[To-do content form](to-do-content-form.md)

