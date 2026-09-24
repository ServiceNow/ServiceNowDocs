---
title: Self-service and omnichannel engagement for CSM release notes
description: The ServiceNow Customer Service Management \(CSM\) application enables customers to connect with your organization through chat on self-service portals, consumer messaging apps, email, phone calls, and WebRTC voice widgets. See the following sections for release notes by version.The ServiceNow Customer Self-Service and Omnichannel Engagement application helps customers resolve issues through self-service portals and omnichannel interactions. This release adds work order visibility in the Consumer Portal and WebRTC voice calling from portal pages and the Engagement Messenger. It also includes AI Voice Agent integration with Amazon Connect for inbound call routing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/customer-self-service-omnichannel-engagement-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [consumer portal, work orders, portal analytics, communities deprecation, customer self-service]
breadcrumb: [Customer Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Self-service and omnichannel engagement for CSM release notes

The ServiceNow® Customer Service Management \(CSM\) application enables customers to connect with your organization through chat on self-service portals, consumer messaging apps, email, phone calls, and WebRTC voice widgets. See the following sections for release notes by version.

## About Self-service and omnichannel engagement for CSM

-   Handle inbound calls intelligently by configuring AI Voice Agents with ServiceNow Voice and Amazon Connect.
-   Initiate WebRTC voice calls from portal pages or engagement messenger with a widget that maintains call state and context across page navigation.

See [Self-service for Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/self-service-options-csm-customers.md), and [Omnichannel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/omnichannel.md) for more information.

**Note:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Activation and other requirements

-   **Activation information**

    Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    Introduced dynamic resizing to the Active Call Interaction Control toolbar. Buttons adapt to container width at runtime while keyboard navigation and focus order remain consistent.

-   **Browser requirements**

    The WebRTC voice call widget is not supported on mobile browsers.

-   **Additional requirements**

    Microphone permission is required for WebRTC calls on mobile devices.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/customer-service-mgmt-rn-landing.md)

## Version 1.0

The ServiceNow® Customer Self-Service and Omnichannel Engagement application helps customers resolve issues through self-service portals and omnichannel interactions. This release adds work order visibility in the Consumer Portal and WebRTC voice calling from portal pages and the Engagement Messenger. It also includes AI Voice Agent integration with Amazon Connect for inbound call routing.

### What's new

-   **[View work orders on the Consumer Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/workorders-consumerportal.md)**

    View and track work orders directly in the Consumer Portal \(B2C\) using the new Work Orders page.

-   **[Use Voice call widget for portal communication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/portal-phone-widget.md)**

    Customers can now make voice calls directly from portal pages or the Engagement Messenger. Call context stays intact as customers navigate between pages. These calls connect to AI Voice Agents to deliver conversational voice experiences without relying on contact center platforms.

-   **[Integrate ServiceNow Voice with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integrate-ccc-amazonconnect.md)**

    Use ServiceNow AI Voice Agents to build conversational voice experiences by routing calls from Amazon Connect, Five9, or NICE contact center channels to deliver natural, conversational customer interactions.


### What's changed

-   **[Usage calculation of self-service experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-portal-user-sessions-timeouts_2.md)**

    Get more accurate portal usage data with an updated analytics definition that eliminates double-counting of guest user sessions.


### What's deprecated or removed

-   **Communities**

    Communities is no longer deployed, enhanced, or supported. The Communities plugins are set to planned deprecation status, which prevents new customer installations. Existing customers who have Communities installed can continue to use it, but new activations are no longer available. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


### Plugin information

-   **New plugins**

    WebRTC Voice \(sn-webrtc\): The WebRTC voice feature for self-service enables users to make voice calls directly from the portal interface or Engagement Messenger.

-   **Deprecated plugins**

    Communities \(com.sn\_communities\): There is no replacement for this plugin.

    Customer Communities \(com.sn\_customer\_communities\): There is no replacement for this plugin.

    Communities Contextual Search \(com.sn\_communities\_contextual\_search\): There is no replacement for this plugin.

    Communities Demo Data \(com.sn\_communities\_demo\): There is no replacement for this plugin.

    Communities Global Entities \(com.sn\_communities\_global\): There is no replacement for this plugin.

    Performance Analytics - Content Pack - Communities \(com.snc.pa.communities\): There is no replacement for this plugin.

    Gamification Core Framework \(com.snc.gamification\): There is no replacement for this plugin.

-   **Plugins planned for deprecation**

    No plugins are planned for deprecation beyond those listed above.

-   **Renamed or changed plugins**

    No plugins were renamed or changed in this release.


