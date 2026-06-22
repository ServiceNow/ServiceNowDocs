---
title: Components installed with Client Transaction Timings
description: The Client Transaction Timings plugin installs several components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/time-configuration/c\_InstalledComponents.html
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client transaction timings, Reference, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with Client Transaction Timings

The Client Transaction Timings plugin installs several components.

## Database Table Structure

The plugin adds the table syslog\_client\_transaction.

## Scripts

The plugin relies on the new script include AJAXClientTiming. This script gathers the information required and populates them on the syslog\_client\_transaction table.

## Dependencies

This plugin does not require any other plugins, but does not gather information unless the [Response Time Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_ResponseTimeIndicator.md) [Response Time Indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/c_ResponseTimeIndicator.md) is enabled.

## Activating the Plugin

To activate the plugin, navigate to **System Definition** &gt; **Plugins** and activate the plugin.

**Note:** New instances have the plugin activated by default.

**Parent Topic:**[Client transaction timings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/r_ClientTransactionTimings.md)

