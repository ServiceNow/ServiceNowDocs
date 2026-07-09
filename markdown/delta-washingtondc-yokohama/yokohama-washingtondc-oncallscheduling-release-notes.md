---
title: Combined On-Call Scheduling release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for On-Call Scheduling from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-oncallscheduling-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined On-Call Scheduling release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for On-Call Scheduling from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family On-Call Scheduling release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading On-Call Scheduling to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for On-Call Scheduling.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Configure preferences for a user group](https://www.servicenow.com/docs/access?context=config-group-prefs-oncall&family=washingtondc&ft:locale=en-US)**

Select a preferred start day of the week for a group, using the **First day of the week** field. Previously, this setting was available only system-wide.

-   **[Enable users to subscribe to the On-Call calendar](https://www.servicenow.com/docs/access?context=enable-subscribe-calendar-oncall&family=washingtondc&ft:locale=en-US)**

Use SSO credentials to log in and subscribe to an on-call calendar and get notified about the upcoming on-call rotation.

-   **[Track the progress of an escalation](https://www.servicenow.com/docs/access?context=track-escalation-progress-oncall&family=washingtondc&ft:locale=en-US)**

Use the info icon \(\[Omitted image "image.icon-view-event-rpa"\] Alt text: Info icon.\) on the Live escalation tracking page to view who has delegated the escalation.


</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing On-Call Scheduling features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[On-Call Scheduling new schedule engine](https://www.servicenow.com/docs/access?context=oncall-schedule-engine&family=xanadu&ft:locale=en-US)**

The new 2024 schedule engine offers a more efficient and improved experience for managing your schedules and shifts. On-Call Scheduling supports an automatic upgrade to the new schedule engine.

-   **[On-Call Scheduling new schedule engine](https://www.servicenow.com/docs/access?context=oncall-schedule-engine&family=xanadu&ft:locale=en-US)**

The new schedule engine introduces the following enhancement:

    -   Shift support to resolve gaps resulting from member placement.
    -   Resolve daily rotation gaps, caused by adding or removing members, holiday schedules, or extra time.
    -   Verifies user continuity based of the last on-call member from the previous schedule.
    -   Improved performance by reducing the time required to add, remove, or move members.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Email redirection behavior for links in major on-call schedule email notification](https://www.servicenow.com/docs/access?context=create-update-schedule-oncall&family=yokohama&ft:locale=en-US)**

In all major on-call schedule or shift email notifications, you can now decide where the links to an on-call schedule or shift record are redirected. Instead of an on-call schedule or shift record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call schedule or shift record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
    -   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some On-Call Scheduling features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some On-Call Scheduling features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate On-Call Scheduling.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=washingtondc&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr><tr><td>

Xanadu

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=xanadu&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr><tr><td>

Yokohama

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=yokohama&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for On-Call Scheduling we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for On-Call Scheduling we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for On-Call Scheduling, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for On-Call Scheduling we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for On-Call Scheduling we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Delegate On-call escalation notifications as configured in the escalation policy by assigning a delegate record to another user.
-   Select a preferred first day of the week for a group to accommodate global users.
-   Receive notifications about the upcoming on-call rotation by downloading or subscribing to a calendar with your SSO authentication.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Reduce and resolve gaps in on-call shifts more efficiently with the new 2024 schedule engine.
-   Reduce the time required to add, remove, or move members from a shift more efficiently.
-   Confirm member continuity with the new schedule engine.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

Control whether an on-call schedule or shift record link in all major on-call email notifications redirects you to Service Operations Workspace \(SOW\) or to the classic UI16 interface in On-Call Scheduling.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)

