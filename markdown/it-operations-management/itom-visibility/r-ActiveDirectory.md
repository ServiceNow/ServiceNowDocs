---
title: Active Directory Domain Controller discovery
description: The Discovery and Service Mapping Patterns application uses the Active Directory Domain Controller On Windows pattern to find active directory domain controllers running on a Windows server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Active Directory Domain Controller discovery

The Discovery and Service Mapping Patterns application uses the Active Directory Domain Controller On Windows pattern to find active directory domain controllers running on a Windows server. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Active Directory Domain Controller On Windows pattern.

|Label|Field Name|
|-----|----------|
|Name|name|
|Domain name|domain\_name|
|Domain Controller name|domain\_controller\_name|
|Forest name|forest\_name|
|Class|sys\_class\_name|
|TCP port\(s\)|tcp\_port|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

