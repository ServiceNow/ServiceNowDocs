---
title: Enable playbooks for analyst selection
description: Add new playbooks to the playbook selection list.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Additional Security Analyst Workspace configuration, Configure the Security Analyst Workspace, Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Enable playbooks for analyst selection

Add new playbooks to the playbook selection list.

You can select an appropriate playbook to investigate security incidents in the Security Analyst Workspace \([Manage security threats using the Security Analyst Workspace](sir-new-ui.md)\). The playbook selection option supports only the playbooks which are designed using Flow Designer.

![Security Incident New UI: Select playbook](../image/add-task-button-callout-1.png)

After you have created a playbook using Flow Designer, follow these steps to include it in the Selected Playbook choice list:

1.  Navigate to `sys_hub_flow` table.
2.  Search for the new playbook you have created using Flow Designer.
3.  Add the **sir\_playbook** tag to the playbooks that you want to include in the Selected Playbook choice list.

**Note:** If you have old playbooks that have not been migrated from workflows to Flow Designer, they will not appear in the list. But, if a playbook created using workflows is assigned to a security incident either by a trigger condition or by manual selection \(using **Run Orchestration** option in the classic environment\), this playbook is launched when you open the security incident in the Security Analyst Workspace.

