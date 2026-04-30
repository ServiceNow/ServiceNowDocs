---
title: Activate Change Management - State Model
description: You can activate the Change Management - State Model plugin \(com.snc.change\_management.state\_model\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Activate Change Management - State Model

You can activate the Change Management - State Model plugin \(com.snc.change\_management.state\_model\) if you have the admin role. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

State Model activates the following related plugin if it is not already active.

<table id="table_ub5_s43_w5"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change Management - Core\[com.snc.change\_management\]

</td><td>

Change management is used to create and manage change requests. Once this is activated, the values for the **Type** field on the change request are updated.

</td></tr></tbody>
</table>**Note:** If you install the Change Management - Core plugin \(com.snc.change\_management\), the Change Management - State Model plugin \(com.snc.change\_management.state\_model\) doesn't function as expected. You must not install Change Management - State Model plugin \(com.snc.change\_management.state\_model\) plugin if you install Change Management - Core plugin \(com.snc.change\_management\).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

If you upgraded from a release prior to Geneva, you must [update old state labels to new state labels](state-model-activate-tasks.md).

-   **[Update change request states](state-model-activate-tasks.md)**  
If you upgraded from a release prior to Geneva, you must update old state labels to new state labels after you activate the Change Management state model.
-   **[Installed with Change Management - State Model](../reference/r_InstalledWithStateModel.md#)**  
Several types of components are installed with the Change Management - State Model.

**Parent Topic:**[Change Management plugins](../concept/change-plugins.md)

**Related topics**  


[Request ITSM Roles- Change Management](request-itsm-roles-cm.md)

[Activate Business Stakeholder](../../../reuse/itsm/task/activate-business-stakeholders.md)

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

[Activate Change Management - Core](t_ActivateChangeMgmtCore.md)

[Request Change Management - Risk Assessment](request-cm-risk-assessment.md)

[Request Change Management - Standard Change Template Intelligence](request-cm-std-chg-template-intelligence.md)

[Change Management - Predictive Intelligence Core](request-cm-picore.md)

[Activate Change Management - Change Flows](activate-change-flows.md)

[Activate Change Management - Change Velocity dashboard](activate-change-velocity-dashboard.md)

[Activate Change Management - Change Models](activate-change-models.md)

[Activate Change Management Success Probability](install-chg-mgmt-success-probability.md)

[Activate Change Management - Data Archiving](activate-data-retention-archive-rule.md)

[List of plugins \(Xanadu\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

