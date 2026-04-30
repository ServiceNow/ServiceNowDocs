---
title: Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page
description: Enable or disable the Agent Assist tab in the contextual side panel for the required record type using the Standard Record Page \(SRP\) in Service Operations Workspace.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Standard Record Page in Service Operations Workspace, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page

Enable or disable the Agent Assist tab in the contextual side panel for the required record type using the Standard Record Page \(SRP\) in Service Operations Workspace.

## Before you begin

Role required: admin

**Note:** Admin should be in Global Domain to edit the table configurations of Agent Assist in Service Operations Workspace.

## About this task

Add or remove a record table from the screen condition, update the sys\_id for the record, and update the script conditions to enable or disable the Agent Assist tab for that table.

**Important:** If you are on a version prior to 4.0, see [Configure the Agent Assist tab in Service Operations Workspace](configure-the-agent-assist-tab-in-service-operations-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Page Collections list, select **SOW Sidebar tabs top**.

    **Note:** The **SOW Sidebar tabs top** Page collection is used in the Service Operations Workspace SRP record page.

3.  From the Pages and variants list in the Record section, select **Agent Assist SNC**.

4.  Select **Settings** to switch to the Settings mode.

    ![Settings page button indicated by a box](../image/settings_SRP.jpg)

5.  To update the Script Conditions, do the following:

    1.  Select the **Scripted Screen Conditions** icon \(![Scripted Screen Conditions icon](../image/scripting_icon.png)\) to open the script conditions.

    2.  Under **Active** column, select **True**.

    3.  If you want to enable the Agent Assist tab for a record table, add the required script to the **Script** field and select **Update**.

    4.  If you want to disable the Agent Assist tab for a record table, remove the script from the **Script** field and select **Update**.

6.  To update the Screen Conditions and sys\_id, do the following:

    1.  From the **Open records** drop-down list, select **Variant record**.

    2.  On the UX Screen form, edit the **Screen Condition** field and add the record tables where you want the tab to appear.

        For example, you could add the following code for the interaction record.

        ```
        controller.sowrecordctrl.table=incident^ORcontroller.sowrecordctrl.table=problem^ORcontroller.sowrecordctrl.table=problem_task^ORcontroller.sowrecordctrl.table=change_request^ORcontroller.sowrecordctrl.table=change_task^ORcontroller.sowrecordctrl.table=kb_knowledge^ORcontroller.sowrecordctrl.table=interaction
        ```

    3.  If you want to enable the Agent Assist tab, add the relevant sys\_id of the table configuration in **Macroponent Configuration**.

        For more information, see [Edit the table configuration for Agent Assist in Service Operations Workspace using the Standard Record Page](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace-using-standard-record-page.md).

    4.  If you want to disable the Agent Assist tab, remove the sys\_id of the relevant table configuration in **Macroponent Configuration**.

        ![UX Screen form with callouts the additions to the Screen Condition and Macroponent Configuration fields](../image/screen_variant_srp.png)

    5.  Select **Update**.


-   **[Edit the table configuration for Agent Assist in Service Operations Workspace using the Standard Record Page](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace-using-standard-record-page.md)**  
Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab using Standard Record Page \(SRP\) in Service Operations Workspace.

**Parent Topic:**[Configure Standard Record Page in Service Operations Workspace](../concept/srp-service-operations-workspace.md)

