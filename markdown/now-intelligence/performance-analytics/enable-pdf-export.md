---
title: Enable PDF export of dashboards
description: To export dashboards to PDF, a plugin and property are needed.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Enable PDF export of dashboards

To export dashboards to PDF, a plugin and property are needed.

## Before you begin

Role required: admin.

Activate the WebKit HTML To PDF plugin and configure the plugin to export homepages, dashboards, and some reports as PDF documents.

**Important:**

The functionality found in homepages, arranging information from your instance to tell a story about your data, is found in dashboards on new instances. On upgraded instances with Next Experience enabled, users can view existing homepages if they have a direct URL, but they can't create or edit them. Responsive dashboards and Analytics Overview dashboards take over homepage functionality.

Use the [Homepage deprecation help tool](../concept/homepage-deprecation-help-tool.md) to convert the homepages on your instance to responsive dashboards.

For more information, see:

-   [Dashboards in the Analytics Center](../../par-for-workspace/concept/analytics-center-dashboards.md).
-   [Working with responsive dashboards](../concept/c_ResponsiveDashboards.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for **WebKit HTML to PDF**.

    Select the plugin to open its form.

3.  Click **Activate/Repair**.

    If the OAuth 2.0 plugin is not already active, the WebKit HTML To PDF plugin activates it as well. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


## Result

Users can export dashboards to PDF to archive, print, or distribute.

