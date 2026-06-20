---
title: Combined Notifications release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Notifications from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-notifications-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Notifications release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Notifications from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Notifications release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Notifications to Zurich

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

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Notifications.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Support for client credential flow in SMTP account](https://servicenow-staging.fluidtopics.net/access?context=send-email-client-credential-flow&family=washingtondc&ft:locale=en-US)**

Configure SMTP account for outbound email in ServiceNow instance using client credential flow.

-   **[Email bounce management](https://servicenow-staging.fluidtopics.net/access?context=email-bounce&family=washingtondc&ft:locale=en-US)**

Link actions to content dynamically in provider notifications actionable content creation by using event params with the existing static actions.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[Sensitive data redaction](https://servicenow-staging.fluidtopics.net/access?context=sensitive-data-redaction&family=xanadu&ft:locale=en-US)**

Redact sensitive data for inbound emails.

-   **[International characters support](https://servicenow-staging.fluidtopics.net/access?context=int-characters-email&family=xanadu&ft:locale=en-US)**

Support added for International characters in the email addresses.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Email notifications dashboard](https://servicenow-staging.fluidtopics.net/access?context=email-notifications-dashboard&family=yokohama&ft:locale=en-US)**

Use the new notifications dashboard with key metrics. This dashboard is available to administrators by default. You can configure this dashboard to enable access to other users.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Email diagnostics dashboard](https://servicenow-staging.fluidtopics.net/access?context=email-diagnostics-dashboard&family=zurich&ft:locale=en-US)**

With email diagnostics you can track bounce management, email delivery metrics, email sender, and reader jobs health.

-   **[Email agentic workflow](https://servicenow-staging.fluidtopics.net/access?context=use-agentic-ai-notifications&family=zurich&ft:locale=en-US)**

With email agentic workflow you can intelligently handle new email agentic workflows by identifying intent, executing actions, &amp; drafting appropriate email responses.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Notifications features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Dynamic actions linking for provider notifications](https://servicenow-staging.fluidtopics.net/access?context=noti-select-provider-actions-order&family=washingtondc&ft:locale=en-US)**

Link actions to content dynamically by using event params and the existing static actions in provider notifications actionable content creation.

-   **[Mandatory __Category__ field in provider notifications](https://servicenow-staging.fluidtopics.net/access?context=noti-new-update-notification&family=washingtondc&ft:locale=en-US)**

The category field for provider notifications is a required field.


</td></tr><tr><td>

Xanadu

</td><td>

-   **[New search and category filter in notification preferences](https://servicenow-staging.fluidtopics.net/access?context=advanced-notification-prefrences&family=xanadu&ft:locale=en-US)**

Notification preferences now include the ability to search within custom notifications and filter by category in system notifications.

-   **[Email unsubscribe](https://servicenow-staging.fluidtopics.net/access?context=email-unsubscribe&family=xanadu&ft:locale=en-US)**

Unsubscribe from emails using the unsubscribe capability in the email header.

-   **[Language preferences](https://servicenow-staging.fluidtopics.net/access?context=multilingual-email-notifications&family=xanadu&ft:locale=en-US)**

Honor sys\_user language preferences set by users for email translations.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Advanced filters in notification preferences](https://servicenow-staging.fluidtopics.net/access?context=advanced-notification-prefrences&family=yokohama&ft:locale=en-US)**

Use notifications filters for categories, delivery channels, active or inactive notifications, subscriptions, and digest enabled notifications.

-   **[Support for assignment group](https://servicenow-staging.fluidtopics.net/access?context=create-add-assignment-group&family=yokohama&ft:locale=en-US)**

Send provider notifications for assignment groups and to users that are part of groups stored in sys\_user\_group table.

-   **[Advanced condition for provider framework](https://servicenow-staging.fluidtopics.net/access?context=noti-new-update-notification&family=yokohama&ft:locale=en-US)**

Use an advanced condition to send a notification that is based on the current email record, changing field values, or system properties.

-   **[Mandatory notifications for provider framework](https://servicenow-staging.fluidtopics.net/access?context=make-notification-mandatory-provider&family=yokohama&ft:locale=en-US)**

Make critical notifications mandatory for the provider framework.

-   **[Email bounce](https://servicenow-staging.fluidtopics.net/access?context=email-bounce&family=yokohama&ft:locale=en-US)**

Prevent resending bounced emails to the addresses that are known to generate bounces.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Email digest for multiple target records](https://servicenow-staging.fluidtopics.net/access?context=configure-email-digest&family=zurich&ft:locale=en-US)**

The email digest now supports both single or multiple target records within a set time interval.

-   **[Notification preferences](https://servicenow-staging.fluidtopics.net/access?context=create-notification-filter-configuration&family=zurich&ft:locale=en-US)**

Enables admins to control the list of notifications displayed for users under the advanced notification preferences.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Notifications features or functionality were removed.

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

Between your current release family and Zurich, some Notifications features or functionality were deprecated.

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

Review information on how to activate Notifications.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

 Install Email agentic workflow by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Notifications we have noted them here.

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

If any specific browser requirements were introduced or changed for Notifications we have noted them here.

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

Review details on accessibility information for Notifications, such as specific requirements or compliance levels.

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

Screen reader support has been extended to the aria labels in the notification preferences and the advanced preferences. The support provides an explanation for button actions, such as the toggle button.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Notifications we have noted them here.

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

If there are specific highlight considerations for Notifications we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Limit sending emails to IDs that are known to generate bounces according to RFC3463 and enable the admins to control blocked ids.
-   Configure SMTP \(Simple Mail Transfer Protocol\) email account for outbound emails using client credential flow.
-   Limit sending emails to IDs that are known to generate bounces according to RFC3463.

 See [Notifications](https://servicenow-staging.fluidtopics.net/access?context=notifications&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

-   Redact sensitive data from customer-initiated inbound emails.
-   Support for international characters in the email addresses.
-   Filter by category in system notifications and search for custom notifications.
-   Optimize SMTP sender job to enhance outbound email delivery.
-   Modify email retry logic for a better delivery experience according to RFC 5321.

 See [Notifications](https://servicenow-staging.fluidtopics.net/access?context=notifications&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Use the new email notifications dashboard with key metrics.
-   Use filter notifications that are based on categories, delivery channels, subscriptions, and digests for notification preferences.
-   Use the enhanced assignment group, advanced condition, and mandatory notifications for a provider framework.
-   Use the standard forms for custom notification preferences and delivery channels.

 See [Notifications](https://servicenow-staging.fluidtopics.net/access?context=notifications&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use email diagnostics dashboard to monitor email delivery metrics, track bounce management, and overall health associated with email sender and reader jobs.
-   Control the preferences page to display relevant notifications.
-   Support multiple target records for email digest.
-   Use the standard forms for system notification preference.
-   Handle incoming email requests intelligently with the new email agentic workflow by identifying intent, executing actions, and drafting appropriate email responses.

 See [Notifications](https://servicenow-staging.fluidtopics.net/access?context=notifications&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

