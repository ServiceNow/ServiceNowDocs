---
title: Service Operations Workspace for ITSM release notes
description: The ServiceNow Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. See the following sections for release notes by version.The September 2026 release adds features to help in automatic application installation. Agents can find attached knowledge quickly because it is now a default related list in the Related records tab. This release also deprecates Migration Utility for Service Operations Workspace application. Agent Client Collector for Investigation and Microsoft Endpoint Configuration Manager for Investigation are prepared for future deprecation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/service-operations-workspace-itsm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [sow]
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Service Operations Workspace for ITSM release notes

The ServiceNow® Service Operations Workspace \(SOW\) application is a configurable workspace that provides a unified agent experience for multiple IT Service Management and IT Operations Management capabilities. See the following sections for release notes by version.

## About Service Operations Workspace for ITSM

-   Service Operations Workspace provides a unified interface for IT service agents to manage incidents, changes, requests and approvals. It supports configurable dashboards, list views, and record pages for ITSM and ITOM workflows.
-   You can effectively manage the lifecycle of incidents, requests in Service Operations Workspace. All of these workflows leverage the power of capabilities such collaborations and AI based recommendations.

See [Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/sow-landing-page.md) for more information.

## Activation and other requirements

**Note:** Service Operations Workspace is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Service Operations Workspace for ITSM is active by default and its default version is 9.5 in Brazil. When you upgrade from any previous release to Brazil from the ServiceNow Store, Service Operations Workspace for ITSM 9.5 is automatically installed.


## Accessibility and localization

-   **Accessibility information**
    -   Accessibility improvements were made to the Major Incident Management in Service Operations Workspace for ITSM in UI List component, record pages and Major Incident workbench tabs, including keyboard navigation and screen reader support. These updates benefit users who rely on screen readers or other Assistive Technology \(AT\), keyboard-only users, and users with low vision.
    -   Reflow support for Major Incident Management in Service Operations Workspace for ITSM: Content can be zoomed up to 400% through your browser settings, with page layouts automatically transforming into a vertical, stacked view without loss of content or functionality. This enhancement helps users with low vision or who have trouble seeing web content due to monitor size, device type, poor lighting, or other situations.

**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Version 9.5

The September 2026 release adds features to help in automatic application installation. Agents can find attached knowledge quickly because it is now a default related list in the Related records tab. This release also deprecates Migration Utility for Service Operations Workspace application. Agent Client Collector for Investigation and Microsoft Endpoint Configuration Manager for Investigation are prepared for future deprecation.

### What's new

-   **[Auto install SOW](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/getting-started-sow.md)**

    A scheduled job is now available that executes a batch installation on a new instance to automatically install applications such as Service Operations Workspace for ITSM Advanced Applications only if the you have the necessary entitlements for the application. This is applicable only on newly provisioned zboot instance.


### What's changed

-   **[Default Attached knowledge related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-sow.md)**

    The attached knowledge related list now appears in the Related records tab by default, if any Knowledge article attached to the incident record.


### Plugin information

-   **Deprecated plugins**

    Migration Utility for Service Operations Workspace \(sn\_sow\_migration\) is deprecated: There is no replacement for this plugin.

-   **Plugins planned for deprecation**
    -   Agent Client Collector for Investigation \(com.snc.acc\_adapter\): Planned for deprecation in Brazil. There is no replacement for this plugin.
    -   Microsoft Endpoint Configuration Manager for Investigation \(com.snc.mecm\_adapter\): Planned for deprecation in Brazil. There is no replacement for this plugin.

