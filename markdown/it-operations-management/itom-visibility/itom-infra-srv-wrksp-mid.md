---
title: MID Server Workspace
description: See a concise overview of MID Server activity. The workspace provides real-time monitoring and enables corrective actions across multiple MID Servers.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use ITOM Infra Services Workspace, ITOM Infra Services Workspace, ITOM Visibility, IT Operations Management]
---

# MID Server Workspace

See a concise overview of MID Server activity. The workspace provides real-time monitoring and enables corrective actions across multiple MID Servers.

## ITOM Infrastructure Services dashboard

The MID Server panel is displayed on the ITOM Infrastructure Services dashboard to provide an overview of MID Server issues.

Selecting any of the cards in the MID Server panel, such as **Servers down** or **Servers with issues**, takes you to that detailed table.

This page also provides a set-up link to Download a MID Server.

## MID Servers tables

Navigate to the MID Servers workspace either by selecting its icon from the application list or by selecting a card from the dashboard. Each of the cards on the dashboard corresponds to the cards in this workspace view.

Selecting a card shows a table of MID Servers filtered by category. You can customize the filter by selecting the filter icon, and save the filters with the **Saved filters** drop-down menu. Group and sort the results by selecting the **Show column filter row** icon in the category row.

On the **Total MID Servers** table, a banner enables you to quickly filter for MID Servers that have been created in the past week. Use this filter to monitor new MID Servers and diagnose any issues from their deployment.

## Server Actions

MID Servers can be selected by the check box on the table, then the **Server Actions** drop-down menu enables you to perform any available action. These actions include Validating or Rekeying the MID Servers. This **Server Actions** menu enables you to perform corrective actions to multiple MID Servers at once from the overview.

## Detailed view

Selecting a MID Server's name navigates to a detailed view of that MID Server. On the Status, Validated, and Unresolved Issues cards, relevant correction actions are shown such as upgrading or validating the MID Server. If the MID Server has any alerts, they are shown in a banner.

If the user has the SOAP ECC queue role, then the View ECC Queue button becomes visible, which navigates to the ECC Queue table.

In the **MID Server details** view, selected from the context menu, you can edit the **Purpose** field to save any notes about the MID Server's purpose. This field is only a text note and does not change anything about the MID Server.

The **Purpose** field can be viewed from the dashboard tables by adding it to the **Personalize fields** menu, accessed through the three-dot menu beside the **Server Actions** menu.

The **MID Server configuration** and **Troobleshooting** sections of the context menu show the records assigned to this MID Server. You can access the MID Server properties or logs. Use the **Create** button to create new records, or the **Manage** button to manage existing ones. You can filter the list of records by selecting the filter icon.

**Parent Topic:**[Use ITOM Infra Services Workspace](itom-infra-srv-wrksp-use.md)

**Related topics**  


[Use the Agent Client Collector \(ACC\) admin workspace](../../agent-client-collector/task/use-acc-admin-workspace.md)

