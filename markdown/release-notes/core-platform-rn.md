---
title: ServiceNow AI Platform core feature release notes
description: The ServiceNow AI Platform core features provide configurations for global ServiceNow AI Platform behavior and behavior in some ServiceNow AI Platform applications. See the following sections for release notes by version.Cross-scope access security enforcement for the getRefRecord\(\) JavaScript API is improved and the default behavior of the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property changed in this patch.Troubleshoot MCP server connections and tool calls from the system logs.Enhancements to AI indicators, HTML editor upgrade to TinyMCE 8.3.0, improved JavaScript engine features, and new configuration options for choice fields and exports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/core-platform-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
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

See  for more information.

## Activation and other requirements

-   **Activation information**

    The ServiceNow AI Platform core features are active by default.

    To use Multi-Instance Setup, you must install it from the ServiceNow Store and activate the AMF Core plugin. For more information, see .


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-admin-rn-landing.md)

## Brazil Patch 2

Cross-scope access security enforcement for the getRefRecord\(\) JavaScript API is improved and the default behavior of the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property changed in this patch.

### What's changed

-   **Improved cross-scope access security enforcement for getRefRecord\(\) JavaScript API**

    The cross-scope security mechanism has been strengthened, supporting consistent application of authorization rules. For more information, see [KB3142985: Cross-Scope Access Security Enhancement \(Glide Element API: getRefRecord\(\)\)](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3142985).

-   **Default value of glide.sys.fencing.restricted\_caller\_access.invalidation\_mode is SCRIPT\_ENGINE**

    The default value of the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property changed from DB\_LISTENER to SCRIPT\_ENGINE. When the property is set to SCRIPT\_ENGINE, and an update set contains a script with changes, the script engine doesn't invalidate associated RCA records. To enable a database listener that monitors update set commits on source code tables and invalidates RCA records at the time of the commits, set the value to DB\_LISTENER.


## Brazil Patch 1

Troubleshoot MCP server connections and tool calls from the system logs.

### What's new

-   **MCP server logging**

    Troubleshoot MCP server connections and tool calls by enabling logging for MCP servers and reviewing the system logs.


## Brazil Early Availability

Enhancements to AI indicators, HTML editor upgrade to TinyMCE 8.3.0, improved JavaScript engine features, and new configuration options for choice fields and exports.

### What's new

-   **Set up cross-instance communication**

    Run a scan to discover non-production instances related to a production instance and connect instances using the Multi-Instance Setup application \(sn-app-amf\). Multi-Instance Setup supports cross-instance communication with other ServiceNow applications and provides a single interface to view and monitor connections.

-   **AI indicators now visible in Core UI lists**

    Rows in Core UI lists that are created or modified by an AI agent now display an AI indicator. The indicator clears automatically when a user makes an inline edit to the row, keeping the indicator accurate as data changes.

-   **Caching for repeated metadata queries**

    The platform caches repeated metadata queries to optimize processing of metadata requests.

-   **Monitor daily slow-pattern trends**

    Track day-over-day trends in slow-pattern data with daily snapshots that automatically identify new or worsening patterns. High-significance changes are highlighted in list views, helping you quickly spot meaningful changes and prioritize investigation efforts. Built-in data retention and filtering keep historical comparisons accurate and relevant for up to 33 days.


### What's changed

-   **AI indicators updated for form fields**

    AI indicators for form fields in Core UI and configurable workspaces now support AI color gradients and have been updated to reflect the latest ServiceNow Otto name and iconography.

-   **TinyMCE version 8.3.0 upgrade**

    The HTML editor in Core UI and configurable workspaces is upgraded from TinyMCE version 6.8.2 to version 8.3.0.

-   **Text pattern configuration in the HTML editor**

    Text patterns in the HTML editor can now be turned on or off using the **glide.ui.html.editor.textpatterns** system property.

-   **Configurable choice field empty option labels**

    Configure choice fields to display either None or --None-- for empty options using the **glide.ui.choice.display\_none** system property.

-   **Base cross-scope access on the latest source code updates**

    Control how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set with the glide.sys.fencing.restricted\_caller\_access.invalidation\_mode system property.

    **Note:** In the Brazil Early Availability and Brazil Patch 1 releases, the default value is DB\_LISTENER. Beginning with the Brazil Patch 2 release, the default value is SCRIPT\_ENGINE.

-   **ECMAScript 2021 \(ES12\) JavaScript mode supports additional scripting features**

    Use additional scripting features in applications or scripts that use the ECMAScript 2021 \(ES12\) JavaScript mode.

-   **JavaScript engine updated with changes from the Rhino engine**

    The JavaScript engine on the ServiceNow AI Platform was updated to incorporate changes from the open-source Rhino JavaScript engine.

-   **Configure row threshold for exports to Excel**

    Configure the row limit for exports to Excel using the properties **glide.export.xls.max.rows.per.sheet** and **glide.export.xlsx.max.rows.per.sheet**.


