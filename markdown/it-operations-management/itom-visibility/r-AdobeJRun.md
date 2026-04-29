---
title: Adobe JRun discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of Adobe JRun.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Adobe JRun discovery

Discovery creates or updates a CMDB record when it detects a running instance of Adobe JRun.

By default, Discovery uses the **Jrun** pattern to perform the Discovery.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Privileged commands

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Data collected for Adobe JRun

The following data is collected in the Jrun `[cmdb_ci_app_server_jrun]` table:

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Installation directory|install\_directory|
|Configuration directory|config\_directory|
|Configuration file|config\_file|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

