---
title: Modify important actions on the Home view of CMDB Workspace
description: Modify the appearance order and other properties of the important action cards that appear on the Home view of the CMDB Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Modify important actions on the Home view of CMDB Workspace

Modify the appearance order and other properties of the important action cards that appear on the Home view of the CMDB Workspace.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

The task cards that appear in the Important tasks tile on the landing page of the CMDB Workspace, are stored in the CMDB WS Imp Action Card Config \[sn\_cmdb\_ws\_imp\_action\_card\_config\] table. You can edit some attributes of these cards, including the setting that controls whether a specific card appears at all. Cards in the Important actions tile are available only for the CMDB Admin \[sn\_cmdb\_admin\] and the CMDB Editor \[sn\_cmdb\_editor\] user roles and each is configured per one of those roles.

There is some overlap in the task cards that appear for a CMDB Admin and for a CMDB Editor, however, the filters in those task cards are different. Typically, for CMDB Admins, the card filter also includes unassigned tasks that a CMDB Admin needs to assign.

Only editing is possible, you can't add or delete action records in this table.

## Procedure

1.  Navigate to **All**.

2.  In the navigation filter, enter `sn_cmdb_ws_imp_action_card_config.list`.

3.  In the list view of the table, edit the table row that you want to modify or click the row to open the record form.

<table id="table_gzr_rty_w5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Persona

</td><td>

The logged on user \(such as CMDB Admin\) for which this card appears.

 You can't edit this field.

</td></tr><tr><td>

Type

</td><td>

Tasks group that this task belongs to, such as Duplicate CIs.

 You can't edit this field.

</td></tr><tr><td>

Table

</td><td>

The table used in the card filter.You can't edit this field.

</td></tr><tr><td>

Active

</td><td>

Determines whether the card for this action appears in CMDB Workspace.

</td></tr><tr><td>

Order

</td><td>

Numeric value that determines the order of each card within the rest of the cards in the Important actions tile. Cards with lower order numbers appear before cards with higher order numbers.

</td></tr><tr><td>

Filter condition

</td><td>

Filters for the tasks that are included for the card.

</td></tr><tr><td>

List columns

</td><td>

Columns that appear in the list view when you click a card to show its associated tasks.

</td></tr><tr><td>

List groupby

</td><td>

Attribute to group by the card's associated tasks in the card's list view. The card's list view appears when you click a card to show its associated tasks.

</td></tr></tbody>
</table>4.  Click **Update**.


**Parent Topic:**[Configuring CMDB Workspace](../concept/configuring-cmdb-workspace.md)

