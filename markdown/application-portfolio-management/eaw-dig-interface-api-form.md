---
title: Digital interface to API form
description: The relationship between a digital interface and an application service API helps analysts to view which digital interface is using which API.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Digital interface to API form

The relationship between a digital interface and an application service API helps analysts to view which digital interface is using which API.

## Digital interface to API form fields

|Field|Description|
|-----|-----------|
|Number|Number of the digital interface API. This field is automatically generated and can’t be edited. The number starts with the prefix DINTFAPI. For example: DINTFAPI0001234.|
|Digital Interface|Name of the digital interface. This field is auto-populated with the name of the interface that you’re editing. If you want to create the relationship to a different digital interface, use the Lookup icon to select a digital interface.|
|API|Name of the CMDB API. Select an API that you want to associate with the digital interface. You can also select the child class of the API \(cmdb\_ci\_api\). For example, Managed API \(cmdb\_ci\_managed\_api\).|
|Description|Description about the connection between the digital interface and the API.|

**Parent Topic:**[Enterprise Architecture Workspace reference](eaw-reference.md)

**Related topics**  


[Connect a digital interface with the CMDB API in the EA Workspace](../../task/eaw-task/eaw-relate-dig-interface-api.md)

