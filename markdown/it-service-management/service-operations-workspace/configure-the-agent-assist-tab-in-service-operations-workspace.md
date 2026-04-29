---
title: Configure the Agent Assist tab in Service Operations Workspace
description: Enable or disable the Agent Assist tab in the contextual side panel for the required record type.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the Agent Assist tab in Service Operations Workspace

Enable or disable the Agent Assist tab in the contextual side panel for the required record type.

## Before you begin

Role required: admin

**Note:** Admin should be in Global Domain to edit the table configurations of Agent Assist in Service Operations Workspace.

## About this task

Add or remove a record table from the screen condition and update the sys\_id for the record to enable or disable the Agent Assist tab for that table.

**Important:** Use this process if you're using a SOW version prior to 4.0. If you're using the version after 4.0, you can use **SOW Sidebar tabs top** Page collection to enable or disable the Agent Assist tab. For more information, see [Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page](configure-agent-assist-tab-sow-srp.md).

## Procedure

1.  Navigate to **All**.

2.  In the search box, enter `sys_ux_screen_type.list` and press Enter.

3.  Select the filter icon \(![Filter icon](../../configurable-workforce-optimization-itsm/image/show-filter-icon.png)\), enter **\[Name\] \[contains\] \[Agent Assist\]** and **\[Application\] \[is\] \[Service Operations Workspace\]**, and select **Run**.

4.  Select the **Agent Assist** link.

5.  From the **UX Screens** tab, select **Agent assist SNC**.

6.  To update the Screen Condition and sys\_id, do the following:

    1.  On the UX Screen form, edit the **Screen Condition** field and add the record tables where you want the tab to appear.

        For example, you could add the following code for the interaction record.

        ```
        controller.sowrecordctrl.table=incident^ORcontroller.sowrecordctrl.table=problem^ORcontroller.sowrecordctrl.table=problem_task^ORcontroller.sowrecordctrl.table=change_request^ORcontroller.sowrecordctrl.table=change_task^ORcontroller.sowrecordctrl.table=kb_knowledge^ORcontroller.sowrecordctrl.table=interaction
        ```

    2.  If you want to enable the Agent Assist tab, add the sys\_id of the relevant table configuration in **Macroponent Configuration**.![UX Screen form with callouts the additions to the Screen Condition and Macroponent Configuration fields](../image/screen_variant_srp.png)

        For more information, see [Edit the table configuration for Agent Assist in Service Operations Workspace](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace.md).

    3.  Select **Update**.

7.  To disable the Agent Assist tab for a record table, remove the record table from the **Screen Condition** field and sys\_id of the relevant table configuration from the **Macroponent Configuration** field, and then select **Update**.


-   **[Edit the table configuration for Agent Assist in Service Operations Workspace](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace.md)**  
Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab.

**Parent Topic:**[Contextual side panel configurations in Service Operations Workspace for ITSM](../concept/contextual-side-panel-configurations-sow-itsm.md)

