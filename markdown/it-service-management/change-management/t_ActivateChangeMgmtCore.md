---
title: Activate Change Management - Core
description: You can activate the Change Management - Core plugin \(com.snc.change\_management\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Plugins, Configure, Change Management, IT Service Management]
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

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

You can activate one or more of the following [plugins](../concept/change-plugins.md):

-   State model \(com.snc.change\_management.state\_model\)
-   Change Management - Collision Detector \(com.snc.change.collision\)
-   Best practice - change risk calculator \(com.snc.bestpractice.change\_risk\)
-   Change risk assessment \(com.snc.change\_management.risk\_assessment\)
-   Standard change catalog \(com.snc.change\_management.standard\_change\_catalog\)
-   Best practice - bulk CI changes \(com.snc.bestpractice.bulkchange\)
-   Mass update CI \(com.snc.change\_management.mass\_update\_ci\)
-   CAB workbench \(com.snc.change\_management.cab\)

You can now [configure Change Management](../concept/configure-change-management.md).

-   **[Installed with Change Management - Core](../reference/r_InstlldWthChngMgmtCore.md#)**  
Several types of components are installed with the Change Management - Core.

**Parent Topic:**[Change Management plugins](../concept/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management](request-itsm-roles-cm.md)

[Activate Business Stakeholder](../../../reuse/itsm/task/activate-business-stakeholders.md)

[Activate Change Management - State Model](t_ActivateStateModel.md)

[Activate Change Management - Collision Detector](t_ActivateConflictDetection.md)

[Activate Best Practice - Change Risk Calculator](activate-change-risk-calculator.md)

[Activate Change Management - Change Schedule](activate-changemgmt-changeschedule.md)

[Activate Change Management - Risk Assessment](activate-change-risk-assessment.md)

[Activate Change Management - Standard Change Catalog](t_ActivateStandardChangeCatalog.md)

[Activate Change Management - Change Success Score](activate-change-success-score.md)

[Activate Change Management - Mass Update CI](t_ActivateChangeManagementBulkCI.md)

[Activate Change Management -Approval policy](activate-change-approval-policy.md)

[Activate Change Management - CAB Workbench](activate-cab-workbench.md)

[Activate Change Management ATF Tests](activate-changemgmt-atftests.md)

[Request Change Management - Risk Assessment](request-cm-risk-assessment.md)

[Request Change Management - Standard Change Template Intelligence](request-cm-std-chg-template-intelligence.md)

[Change Management - Predictive Intelligence Core](request-cm-picore.md)

[Activate Change Management - Change Flows](activate-change-flows.md)

[Activate Change Management - Change Velocity dashboard](activate-change-velocity-dashboard.md)

[Activate Change Management - Change Models](activate-change-models.md)

[Activate Change Management Success Probability](install-chg-mgmt-success-probability.md)

[Activate Change Management - Data Archiving](activate-data-retention-archive-rule.md)

[List of plugins \(Zurich\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

