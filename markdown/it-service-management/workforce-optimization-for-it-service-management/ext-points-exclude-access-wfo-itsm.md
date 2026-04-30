---
title: Using extension points to include access for specific groups in Workforce Optimization for ITSM manager workspace
description: Use scripted extension points to add access for managers to view assignment groups data other than the default groups that they manage in Workforce Optimization for ITSM manager workspace.
locale: en-US
release: yokohama
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Add or remove access to assignment groups in Workforce Optimization for ITSM manager workspace, Advanced configurations for Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Using extension points to include access for specific groups in Workforce Optimization for ITSM manager workspace

Use scripted extension points to add access for managers to view assignment groups data other than the default groups that they manage in Workforce Optimization for ITSM manager workspace.

To see a list of extension points that you can use for Workforce Optimization for ITSM, navigate to **System Extension Points** &gt; **Scripted Extension Points**. In the Extension Points list, open the sn\_wfo\_common.ApplicableGroupsDefinitionManager extension point.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

|Extension point name|Description|
|--------------------|-----------|
|sn\_wfo\_common.ApplicableGroupsDefinitionManager|Implement this extension point to customize the logic to include access for managers to see assignment groups other than the default groups that they manage in the Workforce Optimization for ITSM manager workspace.|

**Parent Topic:**[Add or remove access to assignment groups in Workforce Optimization for ITSM manager workspace](../concept/specify-access-assignment-group-wfo-itsm.md)

**Related topics**  


[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

