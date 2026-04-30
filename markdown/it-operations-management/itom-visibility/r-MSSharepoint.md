---
title: Microsoft SharePoint discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of Microsoft SharePoint.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft SharePoint discovery

Discovery creates or updates a CMDB record when it detects a running instance of Microsoft SharePoint.

By default, Discovery uses the **SharePoint** pattern to discover Microsoft SharePoint. For information on supported Microsoft SharePoint versions, see [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md).

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery for Microsoft SharePoint

The following data is collected in the SharePoints`[cmdb_ci_appl_sharepoint]` table:

|Label|Field Name|
|-----|----------|
|Name|name|
|Class|sys\_class\_name|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Version|version|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

