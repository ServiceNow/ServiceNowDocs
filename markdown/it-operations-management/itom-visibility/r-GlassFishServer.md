---
title: GlassFish Server discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of GlassFish Server.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# GlassFish Server discovery

Discovery creates or updates a CMDB record when it detects a running instance of GlassFish Server.

By default, Discovery uses the following patterns to perform the discovery: **GlassFish Server** and **GlassFish WAR**.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery for GlassFish

The following data is collected in the GlassFish \[cmdb\_ci\_appl\_glassfish\] table:

|Label|Field name|
|-----|----------|
|Inst name|inst\_name|
|Port|port|
|Class|sys\_class\_name|
|Version|version|
|Configuration file|config\_file|
|Domain directory|domain\_directory|
|Install Status|install\_status|
|Installation directory|install\_directory|
|PID|pid|
|Running process|running\_process|
|Running process command|running\_process\_command|
|Running process key parameters|running\_process\_key\_parameters|
|TCP port\(s\)|tcp\_port|
|Operational status|operational\_status|

The following data is collected in the GlassFish War \[cmdb\_ci\_appl\_glassfish\_war\] table:

|Label|Field name|
|-----|----------|
|Name|name|
|Class|class|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

