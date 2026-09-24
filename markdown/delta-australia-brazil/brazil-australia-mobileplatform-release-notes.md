---
title: Combined Mobile Platform release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Mobile Platform from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-mobileplatform-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Mobile Platform release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Mobile Platform from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Mobile Platform release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Mobile Platform to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Mobile Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Mobile offline enhancements](https://www.servicenow.com/docs/access?context=mobile-offline-mode&family=australia&ft:locale=en-US)**

Use the following enhancements added to the mobile offline capability:

    -   Use the seamless online-to-offline continuity, by enabling users to start a form online, save it, and then proceed offline. While offline, users can continue viewing and editing the same data, including attachments, comments, and navigation, for uninterrupted productivity in low or no-connectivity environments. All changes automatically sync after your connection is restored.
    -   Save or submit forms offline, and reopen them later while still offline with all data fully restored.
    -   Support of offline capabilities for descriptive elements in input forms.
    -   Support of offline capabilities for input actions in input forms.
    -   Improved outbox efficiency for input forms by continually combining saved and submitted data.
-   **[Dedicated mobile\_admin role for mobile configuration](https://www.servicenow.com/docs/access?context=mobile-admin-role&family=australia&ft:locale=en-US)**

Assign the new mobile\_admin role to administrators who configure mobile applications, granting them precisely the permissions needed to complete their tasks. This new role helps reduce reliance on the broader admin role for controlled, secure access of your ServiceNow® account.

-   **[Multiple users on a shared device](https://www.servicenow.com/docs/access?context=multi-user-single-instance&family=australia&ft:locale=en-US)**

Enable multiple users to securely log into a ServiceNow single account from shared mobile devices. This feature is beneficial in environments where devices are not personal, as it offers secure and personalized access through user-configured PINs, eliminating the need for repetitive full authentications.

**Note:** From the Australia version and above, the terms instance and instances have been renamed as account and accounts on mobile devices. Accounts are a reflection of platform instances on a mobile device and work in the same way, only the terminology has changed.

-   **[Configurable timing for PIN application timeout](https://www.servicenow.com/docs/access?context=pin-timeout&family=australia&ft:locale=en-US)**

Configure a new property to define the PIN timeout for different ServiceNow mobile apps. This configuration helps reinforce security by controlling how long users can remain inactive before being required to reenter their PIN.

-   **[Dynamic variable support in record screens](https://www.servicenow.com/docs/access?context=record-screen-script-type&family=australia&ft:locale=en-US)**

Use the script screen field in record screens to display dynamic field values. For example, you can display translated content for dynamic variables within an email.

-   **[Mobile AI Voice Agent](https://www.servicenow.com/docs/access?context=mobile-voice-agent&family=australia&ft:locale=en-US)**

Speak with an AI-powered voice assistant on your mobile device for real-time support. Follow along with live conversation transcripts that can also be saved or shared after the call.

-   **[Push notifications for logged-out users](https://www.servicenow.com/docs/access?context=sg-mobile-push-notifications&family=australia&ft:locale=en-US)**

Configure push notifications to be sent to users even when they’re logged out so critical updates aren't missed.

-   **[Mobile Voice Agent SDK support](https://www.servicenow.com/docs/access?context=na-mobile-sdk&family=australia&ft:locale=en-US)**

Enable Voice Agent in SDK-based mobile applications by configuring the External Applications section within the Voice Assistant configuration. Admins with an SDK app configured on the instance can select and save a custom app to activate Voice Agent for that SDK application.

-   **Premium chat for mobile Virtual Agent [\[Placeholder link text to key using-premium-chat\]](https://www.servicenow.com/docs/access?context=using-premium-chat&family=australia&ft:locale=en-US)**

Premium Chat opens a web-based chat experience within your mobile app, ensuring that every feature configured for the web is accessible on your mobile device.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Voice to form](https://www.servicenow.com/docs/access?context=voice-to-form&family=brazil&ft:locale=en-US)**

Fill an entire mobile form by speaking aloud using voice to form. On-device AI maps what you say to the correct fields, and you can review and edit the results before submitting the form.

-   **[Support for Microsoft Entra Shared Device Mode](https://www.servicenow.com/docs/access?context=shared-device-device-level&family=brazil&ft:locale=en-US)**

Enable secure multi-user device sharing with Microsoft Entra Shared Device Mode. Users authenticate once at the device level, and Microsoft Entra-enabled apps use this authentication as part of their own sign-in process. When users sign out, data is cleared across all apps, preparing the device for the next user. This setup is applicable for areas like kiosk and shift-based deployments managed through Microsoft Intune.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Mobile Platform features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Mobile App Builder live component previews](https://www.servicenow.com/docs/access?context=mab-record-example-panel&family=australia&ft:locale=en-US)**

Support was added for live component previews to the following:

    -   Input form screens
    -   Navigation tabs
    -   Mobile app configurations
    -   UI rules
-   **[Mobile App Builder auto-loading](https://www.servicenow.com/docs/access?context=mab-workspace&family=australia&ft:locale=en-US)**

Auto-load records and its downstream components when opening a record for the first time.

-   **[Product branding in Virtual Agent](https://www.servicenow.com/docs/access?context=mobile-publishing&family=australia&ft:locale=en-US)**

Add custom in-product branding to Virtual Agent.

-   **[Chat button in standard search results](https://www.servicenow.com/docs/access?context=now-assist-mobile-search&family=australia&ft:locale=en-US)**

Launch Virtual Agent directly from your standard search results to chat with the Virtual Agent about the selected search result.

-   **[\[Placeholder link text to key mobile-voice-agent\]](https://www.servicenow.com/docs/access?context=mobile-voice-agent&family=australia&ft:locale=en-US)Mobile Voice Agent background calling**

Continue a Voice Agent call after backgrounding the mobile app on iOS and Android. Mute, unmute, or end the call from the home screen or lock screen without returning to the app.


 -   **[Enhanced prelogin page customization](https://www.servicenow.com/docs/access?context=branded-landing-page&family=australia&ft:locale=en-US)**

Configure the placement of the branded landing page login button to be either in the top menu header or as a part of the web page. Integrating the button into a web page helps you to implement a secure flow that addresses issues like short authentication session lifetimes.

-   **[Tone in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&family=australia&ft:locale=en-US)**

Adjust the Virtual Agent tone and response lengths in Assistant Designer.

-   **[Suggested actions](https://www.servicenow.com/docs/access?context=using-enhanced-chat-mobile&family=australia&ft:locale=en-US)**

Configure suggested actions across all agentic workflows.

-   **[Input form screen buttons](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&family=australia&ft:locale=en-US)**

Enable up to two top action buttons on mobile device input forms that have the **Screen presentation** attribute.

-   **[Markdown support for tables in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-mobile-va&family=australia&ft:locale=en-US)**

Render tables in Virtual Agent with markdown support to keep table sizing consistent.

-   **[Turn off mobile impersonation](https://www.servicenow.com/docs/access?context=mobile-impersonate-2&family=australia&ft:locale=en-US)**

Configure the **impersonationEnabled** property to turn off mobile impersonation functionality. With this property, administrators can hide the impersonation option from the mobile app, regardless of assigned user roles.

-   **[\[Placeholder link text to key servicenow-lens-mobile\]](https://www.servicenow.com/docs/access?context=servicenow-lens-mobile&family=australia&ft:locale=en-US)**

The following changes have been made:

    -   Expanded the supported file types to include all of the following: PDF, DOC, DOCX, XLS, XLSX, PPT, PPTX, JPG, JPEG, PNG
    -   Field service agents can now upload attachments in the background after submitting a work order task form, eliminating wait time caused by slow or unreliable network connections. Failed uploads retry automatically, so agents can move to their next task without interruption.
-   **[Redesigned Settings screen](https://www.servicenow.com/docs/access?context=manager-user-settings&family=australia&ft:locale=en-US)**

Navigate the redesigned Settings screen in the Now Mobile and Mobile Agent apps to manage entries like preferences, profile, and account switching in one place. Tap the arrow next to a heading to expand or collapse its related options.


</td></tr><tr><td>

Brazil

</td><td>

-   **Android app build request form**

Meet Google's new Android security requirements for developer verification and app registration using the updated build request form and pipeline. The form now includes a developer verification section where you provide your snippet, and the pipeline automatically embeds it in your APK or generates a verification APK for manual registration.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Mobile Platform features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Mobile Platform features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Mobile Platform.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Mobile Platform is a ServiceNow AI Platform feature that is active by default.


</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Mobile Platform is a ServiceNow AI Platform feature that is active by default.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Mobile Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Mobile Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Mobile Platform, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Accessibility information**

Improved readability on tablet devices.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Mobile Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Mobile Platform we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   Speak with an AI-powered voice assistant directly from your mobile device.
-   Use the enhanced mobile offline capabilities, including seamless online-to-offline continuity.
-   Assign the new mobile\_admin role to administrators who specifically configure mobile applications.
-   Enable multiple users to securely access a single ServiceNow account from shared mobile devices.

 See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Empower your workforce to manage work from anywhere by delivering custom mobile experiences through the Now Mobile and Mobile Agent apps.
-   Support field service technicians and engineers on the go by giving them off-site access to incidents, tasks, and workflows through the Mobile Agent app.
-   Streamline everyday employee tasks by letting your entire organization view schedules, browse knowledge articles, and reserve resources through the Now Mobile app.

 See [Mobile Platform](https://www.servicenow.com/docs/access?context=mobile-config-navigation&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

