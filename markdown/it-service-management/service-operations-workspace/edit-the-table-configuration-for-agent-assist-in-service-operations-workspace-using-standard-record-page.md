---
title: Edit the table configuration for Agent Assist in Service Operations Workspace using the Standard Record Page
description: Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab using Standard Record Page \(SRP\) in Service Operations Workspace.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Agent Assist tab, Configuring Standard Record Page in Service Operations Workspace, Configuring record pages in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Edit the table configuration for Agent Assist in Service Operations Workspace using the Standard Record Page

Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab using Standard Record Page \(SRP\) in Service Operations Workspace.

## Before you begin

Role required: admin

## About this task

Update the table configuration using to get the required search results.

To create a table configuration, see Configure table for a contextual search.

**Important:** If you are on version which is prior to 4.0, [Edit the table configuration for Agent Assist in Service Operations Workspace](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  From the Page Collections list, select **SOW Sidebar tabs top**.

    **Note:** The **SOW Sidebar tabs top** Page collection is used in Service Operations Workspace SRP record page.

3.  From the Pages and variants list in the Record section, select **Agent Assist SNC**.

4.  Select **Settings** to switch to the Settings mode.

    ![Settings page button indicated by a box](../image/settings_SRP.jpg)

5.  From the Open records drop-down list, select **Variant record**.

6.  In the UX screen form, add the property and sys ID in the **Macroponent Configuration** tab.

    1.  Enter the new table name and the sys\_id of the required table configuration.![UX Screen form with callouts the additions to the Macroponent Configuration field](../image/screen_variant_srp.png)

        **Note:** To copy the sys\_id, navigate to **Table Configuration** &gt; **Copy\_sysid**.

    2.  Select **Update**.

        **Note:** To enable or disable Agent Assist tab, see [Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page](configure-agent-assist-tab-sow-srp.md).


**Parent Topic:**[Configure the Agent Assist tab in Service Operations Workspace using the Standard Record Page](configure-agent-assist-tab-sow-srp.md)

