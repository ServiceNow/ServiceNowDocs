---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow AI Platform core features provide configurations for global ServiceNow AI Platform behavior and behavior in some ServiceNow AI Platform applications. See the following sections for release notes by version.Enhancements to AI indicators, HTML editor upgrade to TinyMCE 8.3.0, improved JavaScript engine features, and new configuration options for choice fields and exports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/core-platform-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ServiceNow AI Platform core feature release notes

The ServiceNow AI Platform® core features provide configurations for global ServiceNow AI Platform behavior and behavior in some ServiceNow AI Platform applications. See the following sections for release notes by version.

## About ServiceNow AI Platform

-   Access platform capabilities, discover new applications, and get intelligent, actionable insights.
-   Install and manage licensed applications and plugins for your instance and understand your subscriptions and entitlements.
-   Configure core features, such as tables and data, users, search, notifications, and localization.
-   Maintain and monitor the ServiceNow AI Platform to identify issues or enhance performance.
-   Plan and manage ServiceNow AI Platform upgrades to patches and new releases.

See [Administer the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/intro-now-platform-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    The ServiceNow AI Platform core features are active by default.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-admin-rn-landing.md)

## Brazil Early Availability

Enhancements to AI indicators, HTML editor upgrade to TinyMCE 8.3.0, improved JavaScript engine features, and new configuration options for choice fields and exports.

### What's new

-   **AI indicators now visible in Core UI lists**

    Rows in Core UI lists that are created or modified by an AI agent now display an AI indicator. The indicator clears automatically when a user makes an inline edit to the row, keeping the indicator accurate as data changes.

-   **Caching for repeated metadata queries**

    The platform caches repeated metadata queries to optimize processing of metadata requests.

-   **[Monitor daily slow-pattern trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/daily_slow_patterns.md)**

    Track day-over-day trends in slow-pattern data with daily snapshots that automatically identify new or worsening patterns. High-significance changes are highlighted in list views, helping you quickly spot meaningful changes and prioritize investigation efforts. Built-in data retention and filtering keep historical comparisons accurate and relevant for up to 33 days.


### What's changed

-   **[AI indicators updated for form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-ai-indicator-form-fields.md)**

    AI indicators for form fields in Core UI and configurable workspaces now support AI color gradients and have been updated to reflect the latest ServiceNow Otto name and iconography.

-   **[TinyMCE version 8.3.0 upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_UseHTMLFields.md)**

    The HTML editor in Core UI and configurable workspaces is upgraded from TinyMCE version 6.8.2 to version 8.3.0.

-   **[Text pattern configuration in the HTML editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configuring-the.md-system-properties-in-tinymce.md)**

    Text patterns in the HTML editor can now be turned on or off using the **glide.ui.html.editor.textpatterns** system property.

-   **[Configurable choice field empty option labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_AvailableSystemProperties.md)**

    Configure choice fields to display either None or --None-- for empty options using the **glide.ui.choice.display\_none** system property.

-   **[Base cross-scope access on the latest source code updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/r_AvailableSystemProperties.md)**

    Control how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set with the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property. By default, a database listener monitors update set commits on source code tables and invalidates RCA records at the time of the commits so that cross-scope access is based on the latest source code updates.

-   **[ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/javascript-engine-feature-support.md)**

    Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **[JavaScript engine updated with changes from the Rhino engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/updates-javascript-engine.md)**

    The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **[Configure row threshold for exports to Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/c_ExportLimits.md)**

    Configure the row limit for exports to Excel using the properties **glide.export.xls.max.rows.per.sheet** and **glide.export.xlsx.max.rows.per.sheet**.


