---
title: Combined Notify release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Notify from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-notify-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Notify release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Notify from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Notify release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Notify to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Zurich

</td><td>

Starting with the Zurich release, Notify uses subflows instead of workflows. For existing users in Zurich, your current workflows are still supported. For new users, your Notify plugin installations use subflows.

 As part of this transition, the following workflow activities are available as flow actions and can be used when creating subflows:

-   Join conference call
-   Call
-   Send SMS
-   Forward call
-   Input
-   Hangup
-   Play
-   Record
-   Reject
-   Say
-   Forward to notify client
-   Queue

 Maintain, build, and modify your own custom subflows in Workflow Studio with subflows for new instances. The following base system workflows have been migrated to subflows:

-   \(Re\)join Conference Call
-   Join Conference Call with muting
-   Join Conference Call with SMS

Your existing workflows continue to function after the upgrade.

**Note:** All workflow-related artifacts have been moved to a new plugin, which is maintained in a support-only mode and isn't available for new installations.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Notify.

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

-   **[Deny-Unless ACL](https://servicenow-staging.fluidtopics.net/access?context=acl-denial-behavior&family=yokohama&ft:locale=en-US)**

Enhance the security of Notify tables by restricting access for non-authenticated users through Deny ACLs.

-   **[Enhanced security for client-callable script includes](https://servicenow-staging.fluidtopics.net/access?context=r_NotifyRoles&family=yokohama&ft:locale=en-US)**

Enhanced security for all client-callable script includes by introducing the ability to switch off the sandbox mode, providing greater control and protection against unauthorized script execution for Notify tables.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Notify workflow activities](https://servicenow-staging.fluidtopics.net/access?context=c_NotifyActivities&family=zurich&ft:locale=en-US)**

Manage the subflows for Notify use cases with the following actions.

    -   Input - Advanced: This action is intended for advanced scenarios where the **Say and Play** activity must be repeated multiple times.
    -   Get Notify Number: This action generates a Notify number by accepting the required type as input—**Voice**, **SMS**, or **both**.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Notify features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Enhanced security to access Notify](https://servicenow-staging.fluidtopics.net/access?context=manage-conf-call&family=washingtondc&ft:locale=en-US)**

Control who can view and select the **Start conference call** and **Send SMS** UI actions for a **Task** record through assigning the notify\_view role. The notify\_view is the minimum required role for accessing Notify.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Notify Twilio Direct driver](https://servicenow-staging.fluidtopics.net/access?context=Notify-TwilioDirectDriver&family=xanadu&ft:locale=en-US)**

When the Twilio messaging service is disconnected from a ServiceNow instance, you can choose to delete the messaging records according to your data management and security retention policies or retain the records for future reference. For more details, see the [Behaviour of Default Messaging Service when connecting to Twilio from ServiceNow instance \[KB1644265\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1644265) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Notify features or functionality were removed.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Notify features or functionality were deprecated.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Notify.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Notify is a ServiceNow AI Platform feature that is available with activation of the Notify \(com.snc.notify\) plugin. For details, see [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Notify is a ServiceNow AI Platform feature that is available with activation of the Notify \(com.snc.notify\) plugin. For details, see [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Notify is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Notify is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Notify we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Notify we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Notify, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Notify we have noted them here.

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Notify we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Control who can start a conference call or send an SMS on a task record using Notify.

 See [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

Provides the flexibility to delete or retain Twilio messaging records when Twilio is disconnected from a ServiceNow instance.

 See [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enhanced security for all client-callable script includes by enabling switching off the sandbox mode.
-   Enhanced security access for Notify tables.

 See [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Build Notify subflows according to your requirements by using the default subflows provided in new instances.
-   Coral is the new default theme for Next Experience and Core UI, offering a user-friendly experience.

 See [Notify](https://servicenow-staging.fluidtopics.net/access?context=notify-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

