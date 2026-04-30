---
title: GlassFish Server discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of GlassFish Server.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GlassFish Server discovery

Discovery creates or updates a CMDB record when it detects a running instance of GlassFish Server.

By default, Discovery uses the following patterns to perform the discovery: **GlassFish Server** and **GlassFish WAR**.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery for GlassFish

The following data is collected in the GlassFish \[cmdb\_ci\_appl\_glassfish\] and GlassFish Wars \[cmdb\_ci\_appl\_glassfish\_war\] tables:

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Class|sys\_class\_name|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Installation directory|install\_directory|
|TCP port\(s\)|tcp\_port|
|Configuration directory|config\_directory|
|Configuration file|config\_file|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

