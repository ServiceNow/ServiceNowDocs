---
title: Assign a playbook to Major Incident Management
description: Configure and assign playbooks to manage the major incidents process.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Assign a playbook to Major Incident Management

Configure and assign playbooks to manage the major incidents process.

## Before you begin

The Major Incident Management \(MIM\) plugin must be activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: sn\_mim\_sow\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management. In the Playbook section, you can view the number of assigned playbooks.

3.  Select **Configure**.

    The Playbook page displays the following tabs:

    -   **Assigned playbooks**: List of playbooks that are assigned to Major Incident Management.

        In the case that no playbook is assigned, the **Assign playbook** option is available so you can assign a playbook to Major Incident Management.

    -   **Available Playbooks**: List of playbooks that are available to be assigned to Major Incident Management.
4.  On the configuration page, you can use the following options to assign a playbook to Major Incident Management.

<table id="choicetable_ttg_gsk_gbc"><tbody><tr><td id="d349469e188">

**Recommended playbooks**

</td><td>

The recommended playbooks section displays the following two base system playbooks that are shipped with Major Incident Management: -   **MI playbook**: Provides a simple and concise interface for communication and collaboration, as well as for unplanned communication or collaboration features in separate sections in a task-oriented view. This playbook is suggested for and can be used by upgrade customers.
-   **Advanced MI playbook**: Provides a similar interface to the MI Playbook but has advanced, configurable capabilities for communication and collaboration, as well as unplanned communication or collaboration placed under a single section. You can configure the unplanned communication or collaboration section of the playbook to create, add, and configure the communication plans, tasks, collaboration channels, and channel types as required using the Playbooks.
For more information, see [Designing a major incident playbook](../concept/design-playbooks-mim-sow.md). Playbooks enables you to make the Advanced MI Playbook more flexible to use. This playbook is suggested for and can be used by new or zBoot customers. For more information, see [Managing major incidents using playbooks](../concept/managing-mi-playbook-sow.md).

You can assign and use any or both playbooks with Major Incident Management based on your requirements and usage. Use the **sn\_sow.mim\_playbook\_ids** property to add the sys\_id of the playbook that you want to display under the playbook section and use for Major Incident Management.

Select **View details** to view the playbook information and then select **Assign to MIM** to assign the playbook to Major Incident Management.

</td></tr><tr><td id="d349469e262">

**Available playbooks**

</td><td>

Select the **Available playbooks** tab, then select **Playbook** and then select **Assign**. The selected playbook is assigned to Major Incident Management and is added to the list of assigned playbooks.

</td></tr><tr><td id="d349469e283">

**Create new playbook**

</td><td>

Select the **Process Automation Designer** link in the Create new playbook section on the side panel to create a playbook or configure an existing playbook. For more information, see [Designing a major incident playbook](../concept/design-playbooks-mim-sow.md).

</td></tr></tbody>
</table>
