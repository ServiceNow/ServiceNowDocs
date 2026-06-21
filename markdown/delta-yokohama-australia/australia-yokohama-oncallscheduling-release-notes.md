---
title: Combined On-Call Scheduling release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for On-Call Scheduling from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-oncallscheduling-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined On-Call Scheduling release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for On-Call Scheduling from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family On-Call Scheduling release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading On-Call Scheduling to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Starting from the Zurich release, On-Call Scheduling uses subflows, not workflows. You must transition from workflows to subflows, because the workflows are considered as legacy workflows. For existing users in Zurich, your current workflows continue to be supported. However, for new users, the On-Call Scheduling plugin installations on Zurich and later instances only use subflows.

 Maintain, build, and modify your own custom on-call scheduling flows in Workflow Studio with subflows for new instances. The following subflows are available for configuration:

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for On-Call Scheduling.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Add custom on-call notification channels](https://www.servicenow.com/docs/access?context=custom-on-call-channel-integration&family=zurich&ft:locale=en-US)**

Increase the flexibility in communication by adding and configuring service providers as on-call notification channels. You must configure the communication channel by using the On-call communication channel configuration \[on\_call\_comunication\_channel\_config\] table. After you configure the channel, you can select the new channel. This feature is applicable only after the subflows are configured and used.

-   **[Customize the on-call notification message and keywords](https://www.servicenow.com/docs/access?context=config-oncall-communication-channel&family=zurich&ft:locale=en-US)**

Customize an on-call notification message and response keywords that are sent to the user and user groups as per your preferences. You can customize the message and keywords by using the On-call communication channel configuration \[on\_call\_communication\_channel\_config\] tables.

-   **[Send the on-call escalation notifications when the configured record fields are modified](https://www.servicenow.com/docs/access?context=create-trigger-rule-oncall&family=zurich&ft:locale=en-US)**

Send the on-call escalation notifications when the configured record fields are modified. On-call trigger rules have the following enhancements:

    -   Configure the changes to fields as a triggering condition to run trigger rules. For example, changes to the **Priority** field for an incident can be configured as a trigger condition.
    -   Configure the group or team level trigger rules, or you can configure the global trigger rules that aren’t associated with a user group.
    -   If the assignment group is auto-populated when an incident is created, you can still configure the on-call trigger rules to run and send the escalation notifications.

</td></tr><tr><td>

Australia

</td><td>

-   **[Monthly roster rotation for an on-call schedule](https://www.servicenow.com/docs/access?context=create-update-schedule-oncall&family=australia&ft:locale=en-US)**

Simplify shift management by configuring a monthly roster rotation for an on-call schedule. This option is available only for the 2024 schedule engine.

-   **[Granular role for on-call schedule configurations](https://www.servicenow.com/docs/access?context=roles-assigning-oncall&family=australia&ft:locale=en-US)**

Configure on-call schedule features using the granular and specific role, sn\_on\_call\_admin. It contains sn\_trigger\_table\_cfg\_read and sn\_trigger\_table\_cfg\_write roles.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing On-Call Scheduling features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Email redirection behavior for links in major on-call schedule email notification](https://www.servicenow.com/docs/access?context=create-update-schedule-oncall&family=yokohama&ft:locale=en-US)**

In all major on-call schedule or shift email notifications, you can now decide where the links to an on-call schedule or shift record are redirected. Instead of an on-call schedule or shift record automatically opening in the classic UI16 interface in On-Call Scheduling, the record can be opened in SOW. The on-call schedule or shift record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`.
    -   The **Redirect SOW Email notification for On-call scheduling** \(**sow\_email\_notification\_redirect.on\_call**\) property is set to `true`.
    -   You have the sn\_sow\_user role.
The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Performance improvements in subflows for on-call notifications](https://www.servicenow.com/docs/access?context=on-call-new-trigger-engine&family=zurich&ft:locale=en-US)**

The following performance enhancements are available for on-call notifications when subflows are used:

    -   On-call notifications are sent to multiple channels such as SMS or email simultaneously instead of sending it sequentially.
    -   When the **com.snc.on\_call\_rotation.new\_trigger\_engine** property is set to true, the on-call subflows are processed via the Flow runner queue. The on-call subflows that are marked as High priority are processed faster via a Flow runner queue especially when multiple events are triggered at the same time and are in the process queue.
    -   Reminder notifications are also sent to users when the instance is upgrading.
-   **[Enhanced on-call trigger rules to support subflows](https://www.servicenow.com/docs/access?context=on-call-scheduling-subflows-overview&family=zurich&ft:locale=en-US)**

The on-call trigger rules form is enhanced to trigger a subflow when the trigger rule is executed. You can enable and select a specific subflow for a trigger rule.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some On-Call Scheduling features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some On-Call Scheduling features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=yokohama&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr><tr><td>

Zurich

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=zurich&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

-   FullCalendar library
-   DHTMLX scheduler

**Note:** The On-Call Scheduling \(com.snc.on\_call\_rotation\) plugin is active by default for zBoot customers.

</td></tr><tr><td>

Australia

</td><td>

On-Call Scheduling is available with activation of the ServiceNow AI Platform On-Call Scheduling plugin \(com.snc.on\_call\_rotation\). For details, see [Activate On-Call Scheduling](https://www.servicenow.com/docs/access?context=t_ActivateOnCallScheduling&family=australia&ft:locale=en-US). Activating this plugin activates the following third-party libraries:

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

Control whether an on-call schedule or shift record link in all major on-call email notifications redirects you to Service Operations Workspace \(SOW\) or to the classic UI16 interface in On-Call Scheduling.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Build on-call escalation notification configurable flows by using subflows that are available by default in new instances.
-   Add new custom providers as channels for on-call escalation notifications.
-   Configure the on-call notification message and response keywords to send the escalation notifications to the stakeholders.
-   Send the on-call escalations notifications to all the stakeholders when any of the configured record fields are modified.
-   Use Coral, which is the new default theme for Next Experience and Core UI.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Configure on-call schedule features using granular roles.
-   Configure a monthly roster rotation for an on-call schedule to simplify shift management.

 See [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

