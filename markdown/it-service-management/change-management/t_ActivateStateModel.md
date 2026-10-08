---
title: Activate Change Management - State Model
description: You can activate the Change Management - State Model plugin \(com.snc.change\_management.state\_model\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_ActivateStateModel.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Activate Change Management - State Model

You can activate the Change Management - State Model plugin \(com.snc.change\_management.state\_model\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

The Change Management - State Model plugin builds on the Change Management - Core plugin. Activate State Model on an instance where Core is not yet active. During activation, State Model activates Core **Type** field on the change request. For the Core plugin, see [Activate Change Management - Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_ActivateChangeMgmtCore.md). For the state model concept, see [State model and transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/c_ChangeStateModel.md)

<table id="table_ub5_s43_w5"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change Management - Core\[com.snc.change\_management\]

</td><td>

Change management is used to create and manage change requests. Once this is activated, the values for the **Type** field on the change request are updated.

</td></tr></tbody>
</table>**Warning:** Activate the Change Management - StateModel plugin `(com.snc.change-management.state_model)` only on an instance where the Change Management - Core plugin `(com.snc.change_management)` is not yet active. State Model activates Core automatically. If you activate Core independently before activating State Model, State Model does not function as expected.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


## What to do next

If you upgraded from a release prior to Geneva, you must [update old state labels to new state labels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-model-activate-tasks.md).

-   **[Update change request states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/state-model-activate-tasks.md)**  
If you upgraded from a release prior to Geneva, you must update old state labels to new state labels after you activate the Change Management state model.
-   **[Installed with Change Management - State Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/r_InstalledWithStateModel.md)**  
Several types of components are installed with the Change Management - State Model.

**Parent Topic:**[Change Management plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management]()

[Activate Business Stakeholder]()

[Activate Change Management - Collision Detector]()

[Activate Change Management - Risk Calculator]()

[Activate Change Management - Change Schedule]()

[Activate Change Management - Risk Assessment]()

[Activate Change Management - Standard Change Catalog]()

[Activate Change Management - Change Success Score]()

[Activate Change Management - Mass Update CI]()

[Activate Change Management -Approval policy]()

[Activate Change Management - CAB Workbench]()

[Activate Change Management ATF Tests]()

[Activate Change Management - Core]()

[Request Change Management - Risk Assessment]()

[Request Change Management - Standard Change Template Intelligence]()

[Change Management - Predictive Intelligence Core]()

[Activate Change Management - Change Flows]()

[Activate Change Management - Change Velocity dashboard]()

[Activate Change Management - Change Models]()

[Activate Change Management Success Probability]()

[Activate Change Management - Data Archiving]()

[List of plugins \(Brazil\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/list-of-plugins.md)

