---
title: Components installed with Client Transaction Timings
description: The Client Transaction Timings plugin installs several components.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client transaction timings, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with Client Transaction Timings

The Client Transaction Timings plugin installs several components.

## Database Table Structure

The plugin adds the table syslog\_client\_transaction.

## Scripts

The plugin relies on the new script include AJAXClientTiming. This script gathers the information required and populates them on the syslog\_client\_transaction table.

## Dependencies

This plugin does not require any other plugins, but does not gather information unless the [Response Time Indicator](https://www.servicenow.com/docs/access?context=c_ResponseTimeIndicator&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) [Response Time Indicator](https://www.servicenow.com/docs/access?context=c_ResponseTimeIndicator&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) is enabled.

## Activating the Plugin

To activate the plugin, navigate to **System Definition** &gt; **Plugins** and activate the plugin.

**Note:** New instances have the plugin activated by default.

**Parent Topic:**[Client transaction timings](../reference/r_ClientTransactionTimings.md)

