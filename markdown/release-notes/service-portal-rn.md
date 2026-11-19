---
title: Service Portal release notes
description: The ServiceNow Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. See the following sections for release notes by version.The ServiceNow Otto message no longer appears in Service Portal by default.The September release provides an enhancement to enable identifier-first login authentication method.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-portal-rn.html
release: brazil
topic_type: topic
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [Service Portal release notes Brazil, Service Portal, Service Portal release notes Brazil Patch 2, Brazil Patch 2, Service Portal release notes Brazil Early Availability, Brazil Early Availability in Service Portal]
breadcrumb: [ServiceNow AI Platform user interface release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Portal release notes

The ServiceNow® Service Portal application enables you to build mobile-friendly self-service experiences for your customers and employees with a modular portal framework. See the following sections for release notes by version.

## About Service Portal

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow® products, including ServiceNow®. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Quickly create a self-service portal with an engaging, mobile-friendly user experience using an easy-to-use, modular UI.
-   Empower users with self-service, deflect issues, and drive user productivity and satisfaction by providing simple and immediate access to resources.
-   Connect users to what they’re looking for in a powerful, consumer-grade search experience.

See [Exploring Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/exploring-service-portal.md) for more information.

## Activation and other requirements

-   **Activation information**

    Service Portal is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[ServiceNow AI Platform user interface release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-ui-rn-landing.md)

## Brazil Patch 2

The ServiceNow Otto® message no longer appears in Service Portal by default.

### What's new

-   **ServiceNow Otto**

    The new `glide.sp.otto_onboarding.enabled` system property controls whether the ServiceNow Otto onboarding message is shown to users in all portals. The system property is set to `false` by default, so the ServiceNow Otto message does not appear in portals. Set the system property to `true` to have the ServiceNow Otto message appear on all portals except those listed in the `glide.sp.otto_onboarding.suppressed_portals` property.


## Brazil Early Availability

The September release provides an enhancement to enable identifier-first login authentication method.

### What's new

-   **[Enable identifier-first login in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/identifier-first-login-service-portal.md)**

    Use an identifier-first login authentication method in Service Portal where the authentication path is determined by the username or email entered, and evaluated against configured identifier-first login policies.


