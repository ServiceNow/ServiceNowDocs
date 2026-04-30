---
title: Microsoft Exchange Client Access Server discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of Microsoft Exchange Client Access Server \(Microsoft Exchange CAS\).
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Exchange Client Access Server discovery

Discovery creates or updates a CMDB record when it detects a running instance of Microsoft Exchange Client Access Server \(Microsoft Exchange CAS\).

By default, Discovery uses the **CAS On Windows** pattern to discover the Exchange Client Access Server.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery on the Exchange Client Access Server

The following data is collected on the Exchange Client Access Server `[cmdb_ci_exchange_cas]` table:

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Class|sys\_class\_name|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Installation directory|install\_directory|
|Type|type|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

