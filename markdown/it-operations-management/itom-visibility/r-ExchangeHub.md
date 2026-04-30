---
title: Exchange Hub Transport Servers discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of Exchange Hub.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Exchange Hub Transport Servers discovery

Discovery creates or updates a CMDB record when it detects a running instance of Exchange Hub.

By default, Discovery uses the Hub Transport Server On Windows pattern to discover Exchange Hub Transport Servers.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Hub Transport Server On Windows pattern.

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Class|sys\_class\_name|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Installation directory|install\_directory|
|Type|type|

## CI relationships

The Hub Transport Server On Windows pattern doesn't discover any relationships.

**Parent Topic:**[Software discovery](../concept/c_Software.md)

