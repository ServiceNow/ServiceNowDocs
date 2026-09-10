---
title: Service Portal release notes
description: The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. Service Portal was enhanced and updated in the Australia release.The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. Service Portal was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Service Portal release notes

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. Service Portal was enhanced and updated in the Australia release.

## About Service Portal

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Service Portal. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Use the `glide.sp.otto_onboarding.suppressed_portals` property to suppress the ServiceNow Otto® onboarding message for specific Service Portal portals. Set the property value to a single portal sys\_id, or use a comma-separated list of sys\_ids for multiple portals. Users visiting any portal listed in this property will not see the onboarding message.
-   View the updated user interface for the Service Portal New Organization Chart widget. It includes additional display configurations, such as default and secondary field names.
-   Use portal-specific authentication methods to allow users access to different portals without having to customize Service Portal authentication.
-   Enhance Service Portal accessibility navigation for screen readers by using semantic tags.
-   Use a Coral dark theme on a portal to improve focus, readability, and accessibility.
-   Create theme variants for the Service Portal themes to tailor the visual experience for your users.

See [Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ServicePortal.md) for more information.

## Activation and other requirements

**Important:** Service Portal is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Service Portal is a ServiceNow AI Platform feature that is active by default.


## Accessibility and localization

-   **Accessibility information**
    -   **[Enable dark theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/enable-dark-theme.md)**

        Use the Dark theme in Service Portal to improve focus and provide better accessibility support. This option is commonly used to alleviate eye strain and improve readability.

    -   ****

        Add and edit more semantic tags within the Service Portal Designer to define key areas of a portal to support clearer navigation and descriptions for screen readers. This update helps users who are blind or have low vision by making it easier for assistive technology to identify and understand different sections of each page.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-ui-rn-landing.md)

## Australia

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. Service Portal was enhanced and updated in the Australia release.

### What's new

-   **[Configure Service Portal Approval Configuration record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-approval-assistance-ai-agent.md)**

    The Approval assistance AI agent allows checklist generation from documents that are stored in integrated third-party cloud providers such as Microsoft SharePoint, Google Drive, or a custom internal table.

-   **[New Organization Chart widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/new-organization-chart-widget.md)**

    Use the Service Portal New Organization Chart widget to show additional display configurations, such as default and secondary field names, location, department, and so on, to gain visibility into employees within their organization.

-   **[Create a portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/create-a-portal.md)**

    Configure and apply different authentication configurations for each portal to enable different login experiences for each portal. For example, you can set an authentication method like Okta for an internal employee portal or use Microsoft Azure for an external portal.


### What's changed

-   **[Create a portal theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_CustomCSS.md)**

    Create theme variants for Service Portal themes to tailor the visual experience for your users, which can help you match your brand.


