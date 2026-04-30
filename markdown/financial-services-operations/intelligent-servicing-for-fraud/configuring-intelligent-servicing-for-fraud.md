---
title: Setting up Intelligent Servicing for Fraud
description: You can set up your implementation for the Intelligent Servicing for Fraud application by installing the application, importing financial services data, and reviewing and configuring the components that are installed with the application.
locale: en-US
release: xanadu
product: Intelligent Servicing for Fraud
classification: intelligent-servicing-for-fraud
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Intelligent Servicing for Fraud, Banking applications, Financial Services Operations \(FSO\)]
---

# Setting up Intelligent Servicing for Fraud

You can set up your implementation for the Intelligent Servicing for Fraud application by installing the application, importing financial services data, and reviewing and configuring the components that are installed with the application.

The following table provides an overview of the configuration tasks that are required for Intelligent Servicing for Fraud.

<table id="table_ksw_gpr_4nb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Install Intelligent Servicing for Fraud.

</td><td>

Install the Intelligent Servicing for Fraud application to work on fraud cases.

 For detailed instructions on how to install the application, see [Install Intelligent Servicing for Fraud](../task/install-intelligent-servicing-for-fraud.md).

</td></tr><tr><td>

Assign roles for Intelligent Servicing for Fraud users.

</td><td>

Assign roles to control the actions that are available for each user.

 For detailed instructions on how to assign roles, see [Assign roles for Intelligent Servicing for Fraud users](../task/assign-roles-for-intelligent-servicing-for-fraud-users.md).

</td></tr><tr><td>

Configure service definitions.

</td><td>

Configure service definitions by navigating to **Fraud Operations** &gt; **Administration** &gt; **Service Definitions.**.

 For detailed instructions on how to configure service definitions, see [Configure service definitions](../../fso-common/task/configure-service-definitions.md).

</td></tr><tr><td>

Configure a playbook.

</td><td>

Configure the playbook by navigating to **All** &gt; **Process Automation** &gt; **Process Automation Designer.**.

 For detailed instructions on how to edit or create flows, see [Edit or create a new playbook](../../fso-common/task/configure-playbooks-fso-apps.md).

</td></tr><tr><td>

Configure CSM Configurable Workspace.

</td><td>

Configure CSM Configurable Workspace to enable agents to interact with customers and to create and work on cases.

 For detailed instructions on how to configure CSM Configurable Workspace, see[Configure CSM Configurable Workspace.](../../fso-common/task/configure-csm-workspace-fso-apps.md)

</td></tr><tr><td>

Edit or create flows.

</td><td>

Edit or create flows by navigating to **All** &gt; **Process Automation** &gt; **Flow Designer.**.

 For detailed instructions on how to edit or create flows, see [Configure flows](../../fso-common/task/configure-flow-designer-flows-fso-apps.md)

</td></tr><tr><td>

Configure service level agreements \(SLAs\).

</td><td>

Configure an SLA by navigating to **All** &gt; **Service Level Management** &gt; **SLA** &gt; **SLA Definitions**.

 For detailed instructions on how to configure an SLA, see [Configure the Service Level Agreements \(SLAs\)](../../fso-common/task/configure-sla-definitions-fso-cases.md).

</td></tr><tr><td>

Configure user groups.

</td><td>

Configure the following user groups for case and task assignments. You can also assign roles to groups and users.

 |Name|Roles|
|----|-----|
|Fraud operations analyst|sn\_bom\_fraud.agent|
|Fraud operations investigator|sn\_bom\_fraud.agent|
|Fraud operations manager|sn\_bom\_fraud.manager and sn\_process\_optimization\_analyst|

 For detailed instructions on how to configure user groups, see [Configure user groups](../../fso-common/task/configure-groups-fso.md).

</td></tr><tr><td>

Configure assignment rules to route tasks to agents, based on their skill sets.

</td><td>

Configure the following assignment rule to identify cases that meet certain conditions and then route those cases to agents.

 |Name|Table|
|----|-----|
|Fraud case|sn\_bom\_fraud\_case|

 For detailed instructions on how to configure assignment rules, see [Configure assignment rules](../../fso-common/task/configure-assignment-rules-fso-applications.md)

</td></tr></tbody>
</table>