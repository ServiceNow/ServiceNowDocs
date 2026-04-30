---
title: Request ITSM Roles- Change Management
description: Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\) to gain more control over the access that different change agents, technicians, and managers have within your Change Management process.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Change Management plugins, Configure, Change Management, IT Service Management]
---

# Request ITSM Roles- Change Management

Request the ITSM Roles plugin \(com.snc.itsm.roles\) to activate the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\) to gain more control over the access that different change agents, technicians, and managers have within your Change Management process.

## Before you begin

Role required: admin

## About this task

The ITSM Roles plugin activates several related plugins such as Business Stakeholder \(com.snc\_business\_stakeholder\), ITSM Roles — Incident Management \(com.snc.itsm.roles.incident\_management\), ITSM Roles — Problem Management \(com.snc.itsm.roles.problem\_management\), ITSM Roles — Change Management \(com.snc.itsm.roles.change\_management\), and ITSM Roles — Request Management \(com.snc.service\_management.roles.request\_management\). The related plugins updates the security model and introduces roles for respective products.

With the introduction of the new roles, ITSM provides more control over the access that users have within the process.

By default, this feature is activated only in new instances created in New York or the above releases. It is not automatically activated when upgrading to New York or newer releases from a version prior to New York.

## Procedure

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


-   **[Components installed with ITSM Roles - Change Management](../reference/installed-with-cm-itsm-roles.md)**  
Several user roles are installed with the activation of the ITSM Roles — Change Management plugin \(com.snc.itsm.roles.change\_management\). Security ACLs to support the security model for Change Management and related functionality are also installed.

**Parent Topic:**[Change Management plugins](../concept/change-plugins.md)

**Related topics**  


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

[Change Management - Predictive Intelligence Core](request-cm-picore.md)

[Activate Change Management - Change Flows](activate-change-flows.md)

[Activate Change Management - Change Velocity dashboard](activate-change-velocity-dashboard.md)

[Activate Change Management - Change Models](activate-change-models.md)

[Activate Change Management Success Probability](install-chg-mgmt-success-probability.md)

[Activate Change Management - Data Archiving](activate-data-retention-archive-rule.md)

