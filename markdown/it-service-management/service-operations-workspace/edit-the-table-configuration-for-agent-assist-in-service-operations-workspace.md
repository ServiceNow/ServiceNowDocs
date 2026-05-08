---
title: Edit the table configuration for Agent Assist in Service Operations Workspace
description: Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Agent Assist tab in Service Operations Workspace, Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Edit the table configuration for Agent Assist in Service Operations Workspace

Edit the table configuration for Agent Assist to see the required search results in the Agent Assist tab.

## Before you begin

Role required: admin

**Note:** Admin should always be in Global Domain to edit the table configurations of Agent Assist in Service Operations Workspace.

## About this task

Update the table configuration to get the required search results.

To create a table configuration, see Configure table for a contextual search.

**Important:** Use this process if you're using a SOW version prior to 4.0. If you're using the version after 4.0, you can use **SOW Sidebar tabs top** Page collection to enable or disable the Agent Assist tab. For more information, see [Edit the table configuration for Agent Assist in Service Operations Workspace using the Standard Record Page](edit-the-table-configuration-for-agent-assist-in-service-operations-workspace-using-standard-record-page.md).

## Procedure

1.  Navigate to **All**.

2.  In the search box, enter `sys_ux_screen_type.list` and press Enter.

3.  Select the filter icon \(![Filter icon](../../configurable-workforce-optimization-itsm/image/show-filter-icon.png)\), enter **\[Name\] \[contains\] \[Agent Assist\]** and **\[Application\] \[is\] \[Service Operations Workspace\]**, and select **Run**.

4.  Search for name containing: **Agent Assist** and Application is the workspace name: **Service Operations Workspace**.

5.  Select the **Agent Assist** link.

6.  From the **UX Screens** tab, select **Agent assist SNC**.

7.  To add the property and relevant sys ID of the table configuration in the **Macroponent Configuration**, do the following:

    1.  Enter the new table name and the sys\_id of the required table configuration.![UX Screen form with callouts the additions to the Macroponent Configuration field](../image/screen_variant_srp.png)

        **Note:** To copy the sys\_id, navigate to **Table Configuration** &gt; **Copy\_sysid**.

    2.  Select **Update**.

        To enable or disable Agent Assist tab, see [Configure the Agent Assist tab in Service Operations Workspace](configure-the-agent-assist-tab-in-service-operations-workspace.md).


**Parent Topic:**[Configure the Agent Assist tab in Service Operations Workspace](configure-the-agent-assist-tab-in-service-operations-workspace.md)

