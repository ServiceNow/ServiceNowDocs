---
title: Mobile Platform release notes
description: The ServiceNow Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Mobile Platform release notes

The ServiceNow® Mobile Platform application enables you to access your ServiceNow instance from anywhere. Mobile Platform was enhanced and updated in the Australia release.

## Mobile Platform highlights for the Australia release

-   Speak with an AI-powered voice assistant directly from your mobile device.
-   Use the enhanced mobile offline capabilities, including seamless online-to-offline continuity.
-   Assign the new mobile\_admin role to administrators who specifically configure mobile applications.
-   Enable multiple users to securely access a single ServiceNow account from shared mobile devices.

See [Mobile Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-config-navigation.md) for more information.

## New in the Australia release

-   **[Mobile offline enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-offline-mode.md)**

    Use the following enhancements added to the mobile offline capability:

    -   Use the seamless online-to-offline continuity, by enabling users to start a form online, save it, and then proceed offline. While offline, users can continue viewing and editing the same data, including attachments, comments, and navigation, for uninterrupted productivity in low or no-connectivity environments. All changes automatically sync after your connection is restored.
    -   Save or submit forms offline, and reopen them later while still offline with all data fully restored.
    -   Support of offline capabilities for descriptive elements in input forms.
    -   Support of offline capabilities for input actions in input forms.
    -   Improved outbox efficiency for input forms by continually combining saved and submitted data.
-   **[Dedicated mobile\_admin role for mobile configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-admin-role.md)**

    Assign the new mobile\_admin role to administrators who configure mobile applications, granting them precisely the permissions needed to complete their tasks. This new role helps reduce reliance on the broader admin role for controlled, secure access of your ServiceNow® account.

-   **[Enable multiple users to work on a shared device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/multi-user-single-instance.md)**

    Enable multiple users to securely log into a ServiceNow single account from shared mobile devices. This feature is beneficial in environments where devices are not personal, as it offers secure and personalized access through user-configured PINs, eliminating the need for repetitive full authentications.

    **Note:** From the Australia version and above, the terms instance and instances have been renamed as account and accounts on mobile devices. Accounts are a reflection of platform instances on a mobile device and work in the same way, only the terminology has changed.

-   **[Configurable timing for PIN application timeout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/pin-timeout.md)**

    Configure a new property to define the PIN timeout for different ServiceNow mobile apps. This configuration helps reinforce security by controlling how long users are can remain inactive before being required to reenter their PIN.

-   **[Dynamic variable support in record screens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/record-screen-script-type.md)**

    Use the script screen field in record screens to display dynamic field values. For example, you can display translated content for dynamic variables within an email.

-   **[Mobile AI Voice Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-voice-agent.md)**

    Speak with an AI-powered voice assistant on your mobile device for real-time support. Follow along with live conversation transcripts that can also be saved or shared after the call.

-   **[Push notifications for logged-out users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/sg-mobile-push-notifications.md)**

    Configure push notifications to be sent to users even when they’re logged out so critical updates aren't missed.


## UI changes

-   **[Mobile App Builder live component previews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-record-example-panel.md)**

    Support was added for live component previews to the following:

    -   Input form screens
    -   Navigation tabs
    -   Mobile app configurations
    -   UI rules
-   **[Mobile App Builder auto-loading](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mab-workspace.md)**

    Auto-load records and its downstream components when opening a record for the first time.

-   **[Product branding in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-publishing.md)**

    Add custom in-product branding to Virtual Agent.

-   **[Chat button in standard search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/now-assist-mobile-search.md)**

    Launch Virtual Agent directly from your standard search results to chat with the Virtual Agent about the selected search result.


## Changed in this release

-   **[Enhanced prelogin page customization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/branded-landing-page.md)**

    Configure the placement of the branded landing page login button to be either in the top menu header or as a part of the web page. Integrating the button into a web page helps you to implement a secure flow that addresses issues like short authentication session lifetimes.

-   **[Tone in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/now-assist-mobile-va.md)**

    Adjust the Virtual Agent tone and response lengths in Assistant Designer.

-   **[Suggested actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/using-enhanced-chat-mobile.md)**

    Configure suggested actions across all agentic workflows.

-   **[Input form screen buttons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/servicenow-lens-mobile.md)**

    Enable up to two top action buttons on mobile device input forms that have the **Screen presentation** attribute.

-   **[Markdown support for tables in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/now-assist-mobile-va.md)**

    Render tables in Virtual Agent with markdown support to keep table sizing consistent.

-   **[Turn off mobile impersonation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-impersonate-2.md)**

    Configure the **impersonationEnabled** property to turn off mobile impersonation functionality. With this property, administrators can hide the impersonation option from the mobile app, regardless of assigned user roles.


## Activation information

Mobile Platform is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

Improved readability on tablet devices.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

