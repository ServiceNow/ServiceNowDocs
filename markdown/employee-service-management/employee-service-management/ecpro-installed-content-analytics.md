---
title: Components installed with Content Analytics
description: Several types of components install with the activation of the Content Analytics \[sn\_cda\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Components installed with Content Analytics

Several types of components install with the activation of the Content Analytics \[sn\_cda\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

**Note:** The Content Analytics \[sn\_cda\] plugin activates the sn\_cda.min\_admin\_count system property \[sys\_properties.list\]. This property prevents you from deleting your only Content Analytics admin user by requiring a minimum number \(default is two\) of active users with this role.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|Analytics admin \[sn\_cda.analytics\_admin\]|Creates tracking profiles, assigns the sn\_cda.analytics\_admin and sn\_cda.analytics\_reader roles, and can view the dashboards.|None|
|Analytics reader \[sn\_cda.analytics\_reader\]|Can view tracking profiles and dashboards.|None|

## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content Experiences: Calculate Campaign Engagements

</td><td>

Calculates the engagement score for every published campaign with tracking turned on.By default, runs every five minutes.

</td></tr><tr><td>

Content Experiences: Process SNC analytics

</td><td>

Converts analytics from the Tracked Event \[sn\_cda\_tracked\_evt\_agg\] table into the Analytics Statistic \[sn\_ca\_analytics\_stat\] table. This fills in campaign, action, and content references.By default, runs daily.

</td></tr></tbody>
</table>**Note:** You can trigger or run a tracking profile scheduled job from the Tracking Profile list. You may have to add the **Trigger** field by using the Update Personalized List feature. See [Personal lists](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Analytics Import \[sn\_cda\_import\]

</td><td>

Stores information regarding profile imports.

</td></tr><tr><td>

Analytics Log \[sn\_cda\_analytics\_log\]

</td><td>

Stores logs created when profile validation or import fails.

</td></tr><tr><td>

Analytics Visit Statistic \[sn\_cda\_analytics\_visit\_stat\]

</td><td>

An accumulation of visit statistics on a per day and per profile basis.For example, the number of visitors and page views per session.

</td></tr><tr><td>

Browser \[sn\_cda\_visit\_browser\]

</td><td>

Stores unique list of browsers.

</td></tr><tr><td>

Browser Statistic \[sn\_cda\_browser\_stat\]

</td><td>

Stores analytics related to visits based on browsers and devices.

</td></tr><tr><td>

Device Statistic \[sn\_cda\_device\_stat\]

</td><td>

Stores analytics related to device types \(for example, desktop, mobile\).

</td></tr><tr><td>

Event Statistic \[sn\_cda\_event\_stat\]

</td><td>

Stores browser event analytics \(for example, video plays, button clicks\) from all profiles.

</td></tr><tr><td>

External Tracking Profile \[sn\_cda\_external\_tracking\_profile\]

</td><td>

Generic table that holds external tracking profiles.

</td></tr><tr><td>

Page Statistic \[sn\_cda\_page\_stat\]

</td><td>

Stores page view analytics from all profiles.

</td></tr><tr><td>

Profile Trigger \[sn\_cda\_profile\_trigger\]

</td><td>

Stores schedule jobs, one per profile, which imports data for the tracking profile.

</td></tr><tr><td>

Restricted Country \[sn\_cda\_m2m\_prof\_country\]

</td><td>

Defines what countries you do not want to track. Do not track users that reside in the defined country.

</td></tr><tr><td>

ServiceNow Tracking Profile \[sn\_cda\_snc\_tracking\_profile\]

</td><td>

Stores profiles when tracking with ServiceNow. Extends Tracking Profile \[sn\_cda\_tracking\_profile\]

</td></tr><tr><td>

Tracked Event \[sn\_cda\_tracked\_evt\_agg\]

</td><td>

Stores raw tracked events for ServiceNow profiles. When imported, transforms to the sn\_cda\_event\_stat table.

</td></tr><tr><td>

Tracked Field Value \[sn\_cda\_tracked\_fld\_value\]

</td><td>

Helper table to use during tracking for storing references to unique field/value combinations. Enables analytics breakdowns.

</td></tr><tr><td>

Tracked Page \[sn\_cda\_tracked\_page\_agg\]

</td><td>

Stores raw page view events for ServiceNow profiles. When imported, transforms to the sn\_cda\_page\_stat table.

</td></tr><tr><td>

Tracking Profile \[sn\_cda\_tracking\_profile\]

</td><td>

Generic table that holds analytics profiles.

</td></tr><tr><td>

Tracked Visit \[sn\_cda\_tracked\_visit\_agg\]

</td><td>

Stores raw visit events for ServiceNow profiles. When imported, transforms to the sn\_cda\_visit\_analytics\_stat table.

</td></tr><tr><td>

Visit Referral \[sn\_cda\_visit\_referral\]

</td><td>

Stores analytics related to page referrals.

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|Analytics Statistic \[sn\_ca\_analytics\_stat\]|Stores aggregate analytics for a campaign, including interactions with campaign, action, and content.|
|Archived Campaign Statistic \[sn\_ca\_campaign\_arch\]|Stores archived campaign statistics.|
|Tracked Action \[sn\_ca\_tracked\_action\]|What unique actions you want to track with a campaign.|
|Campaign Tracked Action \[sn\_ca\_m2m\_campaign\_action\]|Track the many-to-many relationships between actions and a campaign. Track only actions that are part of a campaign.|
|Convertive Action \[sn\_ca\_m2m\_action\_content\_type\]|Many-to-many relationship between actions and content types. Defines what types of actions contribute to the engagement score of a campaign. For example, a banner impression action should not change the engagement score, but a banner click-through should.|

## Widgets installed

|Widget|ID|Description|
|------|---|-----------|
|Content Analytics Site Tracker|cda-site-analytics|Helps analyze user behavior, usage metrics, and more from the user experience dashboard.|

**Note:** A new **Enable Tracking** field has been introduced to content notifications, designed specifically for email content. Existing notification records will have this field disabled by default, in line with prior system settings and by default, existing email content will have tracking turned off. However, for new email notification contents, the **Enable Tracking**option will be available for your selection and will be automatically enabled on new record creation. This feature provides greater flexibility, allowing you to determine whether tracking should be applied to specific email content record.

