---
title: Create or update a configuration in EAP
description: Define your own Agile configuration or update an existing configuration in Enterprise Agile Planning \(EAP\).
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create or update a configuration in EAP

Define your own Agile configuration or update an existing configuration in Enterprise Agile Planning \(EAP\).

## Before you begin

[Install Strategic Planning](../../alignment-planner-workspace/task/install-alignment-planner-workspace.md).

Set the Application Scope of your ServiceNow instance to Strategic Planning.

Role required: sn\_apw\_advanced.eap\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace**.

2.  From the **Settings** menu, select **Enterprise Agile Planning** &gt; **Configuration**.

3.  Choose to create a configuration or update an existing one.

    -   To create, select **New configuration**.
    -   To update, select **Edit** from one of the available configurations.
    ![Create an EAP configuration or edit an existing one.](../images/eap-create-edit-config.png)

4.  On the form, fill in or update the fields.

<table id="table_ihv_5bq_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

Name to identify the configuration.

</td></tr><tr><td>

State

</td><td>

State of the configuration. The default value for this field is **Inactive**.Change it to **Active** to make it available to use for your Agile teams in Enterprise Agile Planning.

</td></tr><tr><td>

Sync with Agile Development

</td><td>

Select this option to sync iterations such as Planning Intervals and Sprints with Agile Development 2.0. For more information, see [Integration between EAP and Agile Development 2.0](../reference/sync-eap-and-agile-2.md).If your team is of the Kanban type, you can leave this option unselected.

</td></tr></tbody>
</table>5.  Select the work item types to be available within this configuration.

    Only the work item types that you enable here are available for your Agile teams in the Backlog and Planning board.

    ![Select work item types for EAP configuration.](../images/eap-work-item-types-enable.png)

6.  Select the team levels that you want to have in your configuration.

    Based on the team levels that you enable here, you can add only those entities to your Agile structure. For example, if you didn’t enable **Solution Train** team level in the configuration, you can’t add any solution trains to your Agile structure and you can’t plan work for any solution trains from the Backlog or Planning board.

7.  Select the default work item type to be available at each team level and its planning calendar.

    -   **Scrum teams with a regular cadence**

        Planning calendars can be set only for Agile Release Trains \(ARTs\) and Agile Teams and the planning calendar types available by default are **Planning Interval** and **Sprint**. If you want a different calendar, create one. See [Create a planning calendar in EAP](create-planning-calendar-type-in-eap.md).

        ![Mapping work item type and planning calendars to the team levels.](../images/eap-work-item-team-level-mapping.png)

    -   **Kanban teams**

        If your team operates in a Kanban style, which is a continuous workflow structure without any regular planning interval schedule, you can set the **Planning calendar** fields to **None**.

        ![Mapping work item type and planning calendars for a Kanban team configuration.](../images/eap-kanban-config-calendar.png)

8.  Select **Save**.


## What to do next

-   If you have updated the planning calendar selection for any active configuration that has teams associated with it, update the relevant dashboard configuration too. This action ensures that the metrics displayed for those teams are accurate. See [Updating dashboards for planning calendar changes in EAP](../concept/updating-dashboards-for-planning-calendar-changes-in-eap.md).
-   [Activate an EAP configuration](activate-eap-configuration.md)

