---
title: Service Portal release notes
description: The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Service Portal release notes

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.

## About Service Portal

-   Starting with Zurich Patch 12, Now Assist is now ServiceNow Otto®. ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Service Portal. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Use the `glide.sp.otto_onboarding.suppressed_portals` property to suppress the ServiceNow Otto onboarding message for specific Service Portal portals. Set the property value to a single portal sys\_id, or use a comma-separated list of sys\_ids for multiple portals. Users visiting any portal listed in this property will not see the onboarding message.
-   Use the support for Service Portal in the iOS Google App.
-   As an admin, configure the widget load order on Service Portal pages.
-   As an admin, defer the loading of AI Search assets to enhance page performance.

See [Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/c_ServicePortal.md) for more information.

## Activation and other requirements

-   **Activation information**

    Service Portal is a ServiceNow AI Platform feature that is active by default.


## Accessibility and localization

-   **Accessibility information**
    -   **Dark theme**

        The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-platform-ui-rn-landing.md)

## December 2025

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.

### What's new

-   **[Approval Info Record widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/approval-info-record-widget.md)**

    The Service Portal Approval Info Record widget shows details about the approval request and a full record for an approval including the activity stream.

    The Approval Info Record widget and the new Now Assist Approval Assistance AI agent maintain parity. To use the new Approval Info Record widget, activate the Approval Details Page Route Map, and uptake the Approval Info Record widget in your custom page.

    The new Now Assist Approval Assistance AI agent allows you to see your pending approvals, as well as the details about your pending approvals. For more information, see [Platform Approval assistance AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-approval-aia.md).


## Zurich

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a simple-to-use modular portal framework. Service Portal was enhanced and updated in the Zurich release.

### What's new

-   **[Configure Service Portal Approval Configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-approval-assistance-ai-agent.md)**

    Configure the Service Portal Approval Configuration record to make the Approval Assistance AI agent and Approval Info Record widget work better for your specific use case.

-   **[Configure widget loading order in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-widget-loading-order.md)**

    As an admin, configure the widget loading order to defer their loading. This feature enables faster loading of the page and makes the widgets available for interaction as they load, thus improving the user experience.


-   **[Deferred loading of AI Search assets in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/defer-loading-ais-sp.md)**

    Enable deferred loading of AI Search assets on the Service Portal page until the main content is loaded. This feature helps the page load faster and improves user experience.


### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


