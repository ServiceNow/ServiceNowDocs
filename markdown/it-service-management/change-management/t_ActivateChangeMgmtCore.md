---
title: Activate Change Management - Core
description: You can activate the Change Management - Core plugin \(com.snc.change\_management\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_ActivateChangeMgmtCore.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Activate Change Management - Core

You can activate the Change Management - Core plugin \(com.snc.change\_management\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

This plugin will update the Type field on the Change Request to have the values as Normal, Standard, or Emergency.

The Type value on existing the Change Requests will be updated as following:

|Before installing the plugin|After installing the plugin|
|----------------------------|---------------------------|
|Routine|Standard|
|Comprehensive|Normal|
|Emergency|Emergency|

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).


## What to do next

You can activate one or more of the following [plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-plugins.md):

-   State model \(com.snc.change\_management.state\_model\)
-   Change Management - Collision Detector \(com.snc.change.collision\)
-   Best practice - change risk calculator \(com.snc.bestpractice.change\_risk\)
-   Change risk assessment \(com.snc.change\_management.risk\_assessment\)
-   Standard change catalog \(com.snc.change\_management.standard\_change\_catalog\)
-   Best practice - bulk CI changes \(com.snc.bestpractice.bulkchange\)
-   Mass update CI \(com.snc.change\_management.mass\_update\_ci\)
-   CAB workbench \(com.snc.change\_management.cab\)

You can now [configure Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-change-management.md).

-   **[Installed with Change Management - Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/r_InstlldWthChngMgmtCore.md)**  
Several types of components are installed with the Change Management - Core.

**Parent Topic:**[Change Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management]()

[Activate Business Stakeholder]()

[Activate Change Management - State Model]()

[Activate Change Management - Collision Detector]()

[Activate Best Practice - Change Risk Calculator]()

[Activate Change Management - Change Schedule]()

[Activate Change Management - Risk Assessment]()

[Activate Change Management - Standard Change Catalog]()

[Activate Change Management - Change Success Score]()

[Activate Change Management - Mass Update CI]()

[Activate Change Management -Approval policy]()

[Activate Change Management - CAB Workbench]()

[Activate Change Management ATF Tests]()

[Request Change Management - Risk Assessment]()

[Request Change Management - Standard Change Template Intelligence]()

[Change Management - Predictive Intelligence Core]()

[Activate Change Management - Change Flows]()

[Activate Change Management - Change Velocity dashboard]()

[Activate Change Management - Change Models]()

[Activate Change Management Success Probability]()

[Activate Change Management - Data Archiving]()

[List of plugins \(Australia\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)

