---
title: Change Management - Predictive Intelligence Core
description: To activate Change Management predictive intelligent features, the Change Management - Predictive Intelligence Core plugin \(com.snc.change\_management.ml\) is required and is automatically installed along with other through Change Management Predictive Intelligence plugins that are requested using the Now Support Customer Service system.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Change Management - Predictive Intelligence Core

To activate Change Management predictive intelligent features, the Change Management - Predictive Intelligence Core plugin \(com.snc.change\_management.ml\) is required and is automatically installed along with other through Change Management Predictive Intelligence plugins that are requested using the Now Support Customer Service system.

## Before you begin

Role required: maint

## About this task

The Change Management - Predictive Intelligence Core plugin \(com.snc.change\_management.ml\) plugin activates these related plugins if they are not already active.

<table id="table_fvt_nq2_plb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Predictive Intelligence\[com.glide.platform\_ml\]

</td><td>

Using Predictive Intelligence you an create, train, and test solutions so that you can quickly understand the basic functionality of how a machine-learning solution works.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  On the All Applications page, select **Request Plugin** to open the **Activate Plugin** form on Now Support.

    ![Admin view of Activate Plugin form to capture details for activating the CSM Workspace plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/request-plugin.png)

3.  On Now Support, select the link to access the Now Support Service Portal Service Catalog.

    ![Message informing customers about new service portal with a link provided.](../../../reuse/images/hi-redirect.png)

4.  Select your instance.

5.  Select **Actions &gt; Activate Plugin**.

6.  On the **Activate Plugin** form, provide the following information.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="target-instance"><td>

What is your target instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Which plugin would you like to activate

</td><td>

Name of the plugin to activate.

 **Note:** If the system does not list the plugin you want or if you are activating the plugin on an OEM or on-premise instance, select the **Plugin I'm looking for is not listed** check box and then enter the name of the plugin.

</td></tr><tr id="date-time"><td>

Select Maintenance Date and Time

</td><td>

The date and time to activate the plugin.

 **Note:** Plugins are activated in two batches, once in the morning and once in the evening, on every business day in the US Pacific time zone. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr></tbody>
</table>    For example, see the following form to activate the CSM Workspace plugin on an instance named My Instance.

    ![Admin view of the form to capture details of the CSM Workspace plugin on a selected instance. For the text description, refer to the Activate Plugin form table.](../../../reuse/images/activate-plugin-form.png "Activate Plugin form")

7.  Select **Submit**.

    For additional details about requesting a plugin, see [Requesting a Plugin from the Service Catalog \[KB0751715\] article in the Now Support Knowledge Base.](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0751715)


-   **[Components installed with Change Management - Predictive Intelligence Core](../reference/installed-withpicore.md)**  
Several types of components are installed with activation of the Change Management - Predictive Intelligence Core plugin that includes tables. These tables can be utilized only after the other Change Management Predictive Intelligence plugins are activated.

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

[Activate Change Management - Core](t_ActivateChangeMgmtCore.md)

[Request Change Management - Risk Assessment](request-cm-risk-assessment.md)

[Request Change Management - Standard Change Template Intelligence](request-cm-std-chg-template-intelligence.md)

[Activate Change Management - Change Flows](activate-change-flows.md)

[Activate Change Management - Change Velocity dashboard](activate-change-velocity-dashboard.md)

[Activate Change Management - Change Models](activate-change-models.md)

[Activate Change Management Success Probability](install-chg-mgmt-success-probability.md)

[Activate Change Management - Data Archiving](activate-data-retention-archive-rule.md)

[List of plugins \(Xanadu\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

