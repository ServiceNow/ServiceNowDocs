---
title: Combined Notifications release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Notifications from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-notifications-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Notifications release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Notifications from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Notifications release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Notifications to Australia

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

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Notifications.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Email notifications dashboard](https://www.servicenow.com/docs/access?context=email-notifications-dashboard&family=yokohama&ft:locale=en-US)**

Use the new notifications dashboard with key metrics. This dashboard is available to administrators by default. You can configure this dashboard to enable access to other users.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Email diagnostics dashboard](https://www.servicenow.com/docs/access?context=email-diagnostics-dashboard&family=zurich&ft:locale=en-US)**

With email diagnostics you can track bounce management, email delivery metrics, email sender, and reader jobs health.

-   **[Email agentic workflow](https://www.servicenow.com/docs/access?context=use-agentic-ai-notifications&family=zurich&ft:locale=en-US)**

With email agentic workflow you can intelligently handle new email agentic workflows by identifying intent, executing actions, &amp; drafting appropriate email responses.


</td></tr><tr><td>

Australia

</td><td>

-   **[User mailbox integration](https://www.servicenow.com/docs/access?context=personal-corporate-mailbox&family=australia&ft:locale=en-US)**

Enable agents to integrate their personal corporate mail boxes to send and receive emails.

-   **[Granular admin roles required to secure the instance](https://www.servicenow.com/docs/access?context=granular-admin-roles-notifications&family=australia&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for Notifications without requiring the full admin role.

-   **[Notification agent](https://www.servicenow.com/docs/access?context=notification-creation-agent&family=australia&ft:locale=en-US)**

The Notification agent enables platform administrators to create and modify email notifications and templates using natural language prompts, reducing the need of navigating complex forms &amp; scripts.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Notifications features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Advanced filters in notification preferences](https://www.servicenow.com/docs/access?context=advanced-notification-prefrences&family=yokohama&ft:locale=en-US)**

Use notifications filters for categories, delivery channels, active or inactive notifications, subscriptions, and digest enabled notifications.

-   **[Support for assignment group](https://www.servicenow.com/docs/access?context=create-add-assignment-group&family=yokohama&ft:locale=en-US)**

Send provider notifications for assignment groups and to users that are part of groups stored in sys\_user\_group table.

-   **[Advanced condition for provider framework](https://www.servicenow.com/docs/access?context=noti-new-update-notification&family=yokohama&ft:locale=en-US)**

Use an advanced condition to send a notification that is based on the current email record, changing field values, or system properties.

-   **[Mandatory notifications for provider framework](https://www.servicenow.com/docs/access?context=make-notification-mandatory-provider&family=yokohama&ft:locale=en-US)**

Make critical notifications mandatory for the provider framework.

-   **[Email bounce](https://www.servicenow.com/docs/access?context=email-bounce&family=yokohama&ft:locale=en-US)**

Prevent resending bounced emails to the addresses that are known to generate bounces.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Email digest for multiple target records](https://www.servicenow.com/docs/access?context=configure-email-digest&family=zurich&ft:locale=en-US)**

The email digest now supports both single or multiple target records within a set time interval.

-   **[Notification preferences](https://www.servicenow.com/docs/access?context=create-notification-filter-configuration&family=zurich&ft:locale=en-US)**

Enables admins to control the list of notifications displayed for users under the advanced notification preferences.


</td></tr><tr><td>

Australia

</td><td>

-   **[Send email using Microsoft Graph](https://www.servicenow.com/docs/access?context=send-email-using-ms-graph&family=australia&ft:locale=en-US)**

Connect Microsoft email accounts using Microsoft Graph within the ServiceNow instance for sending outbound emails.

-   **[Email threading for inbound reply email](https://www.servicenow.com/docs/access?context=c_InboundEmailActions&family=australia&ft:locale=en-US)**

Enable classification of inbound emails by using the thread-index header for emails originating from Microsoft or Microsoft Outlook ecosystem.

-   **[Column Level Encryption for email attachments](https://www.servicenow.com/docs/access?context=cle-for-email-attachments&family=australia&ft:locale=en-US)**

Attachments from inbound emails are now encrypted when stored in CLE-enabled tables and decrypted when sent in outbound emails, ensuring secure access without requiring scripting.

-   **[Enable push notifications for logged-out users](https://www.servicenow.com/docs/access?context=enable-notifications-logged-out-users&family=australia&ft:locale=en-US)**

Push notifications can now be configured to be sent to users even when they are logged out, ensuring critical updates are not missed.

-   **[Now LLM support and email template configuration in Notification Agent](https://www.servicenow.com/docs/access?context=notification-creation-agent&family=australia&ft:locale=en-US)**

Now LLM and third-party LLM models are now supported, and email templates can be configured for notifications created using the Notification Agent.

-   **[Email templates for the Email Generator Agent](https://www.servicenow.com/docs/access?context=create-actions-for-intent&family=australia&ft:locale=en-US)**

Use branded email templates in the Email Generator Agent, allowing AI-generated responses with customer-specific layouts, logos, and styling.

-   **[Multiple intent identification in inbound emails](https://www.servicenow.com/docs/access?context=email-agentic-workflow&family=australia&ft:locale=en-US)**

Multiple intents can now be identified in inbound emails, allowing multiple reply email actions for a single email.

-   **[Handle missing inputs for inbound email actions](https://www.servicenow.com/docs/access?context=email-agentic-workflow&family=australia&ft:locale=en-US)**

Missing inputs for inbound email actions are now handled through configurable execution modes, allowing missing inputs to be requested, intents to be skipped, or processing to continue.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Notifications features or functionality were removed.

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

Between your current release family and Australia, some Notifications features or functionality were deprecated.

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

Review information on how to activate Notifications.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

 Install Email agentic workflow by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Notifications is a ServiceNow AI Platform feature that is active by default.

 Install Notifications Email Agents by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

 The Notification Agent requires the Implementation Agent \(IA\) Orchestration framework and is not supported as a standalone feature.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Notifications we have noted them here.

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

If any specific browser requirements were introduced or changed for Notifications we have noted them here.

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

Review details on accessibility information for Notifications, such as specific requirements or compliance levels.

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
</table>## Localization information

If there are specific localization considerations for Notifications we have noted them here.

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

If there are specific highlight considerations for Notifications we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Use the new email notifications dashboard with key metrics.
-   Use filter notifications that are based on categories, delivery channels, subscriptions, and digests for notification preferences.
-   Use the enhanced assignment group, advanced condition, and mandatory notifications for a provider framework.
-   Use the standard forms for custom notification preferences and delivery channels.

 See [Notifications](https://www.servicenow.com/docs/access?context=notifications&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Use email diagnostics dashboard to monitor email delivery metrics, track bounce management, and overall health associated with email sender and reader jobs.
-   Control the preferences page to display relevant notifications.
-   Support multiple target records for email digest.
-   Use the standard forms for system notification preference.
-   Handle incoming email requests intelligently with the new email agentic workflow by identifying intent, executing actions, and drafting appropriate email responses.

 See [Notifications](https://www.servicenow.com/docs/access?context=notifications&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Integrate personal corporate mailboxes with in ServiceNow to send and receive emails.
-   Send outbound emails from the ServiceNow instance using Microsoft Graph.
-   Encrypt inbound email attachments in CLE-enabled tables and decrypt them for outbound emails.
-   Enhanced inbound email classification to support thread-index header for emails generated via Microsoft or Microsoft Outlook ecosystem.
-   Deliver critical push notifications even when users are logged out.
-   Create and modify email notifications and email templates using natural language prompts through the Notification Agent.
-   Enhance customer communications with branded email template support in the Email Generator Agent.
-   Identify and process multiple intents in inbound emails, enabling multiple reply email actions.
-   Handle missing inputs in inbound emails using configurable execution modes.

 See [Notifications](https://www.servicenow.com/docs/access?context=notifications&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

