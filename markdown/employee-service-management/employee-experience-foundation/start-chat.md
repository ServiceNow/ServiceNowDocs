---
title: Customize Start Microsoft Teams chat UI action
description: Enables you to extend the Start Microsoft Teams chat UI actions to the tables you require.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize UI actions for IT Service Management with Microsoft Teams, IT Service Management integration, Customize Integrations for Employee Experience, Manage, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Customize Start Microsoft Teams chat UI action

Enables you to extend the Start Microsoft Teams chat UI actions to the tables you require.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **UI Actions**.

2.  Open the existing **Start Microsoft Teams chat** UI action in a new window.

3.  Click **New**.

4.  On the **UI action** form, fill the fields:

<table id="table_mjd_tth_pnb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the UI action. Ex: Start Microsoft Teams chat

</td></tr><tr><td>

Table

</td><td>

Table to which the Start Microsoft Teams chat UI action is to be available

</td></tr><tr><td>

Form button

</td><td>

Check this box

</td></tr><tr><td>

Show insert

</td><td>

Clear this box

</td></tr><tr><td>

Client

</td><td>

Check this box

</td></tr><tr><td>

List v3 Compatible

</td><td>

Check this box

</td></tr><tr><td>

Onclick

</td><td>

Type `initChatWithGroup()`

</td></tr><tr><td>

Condition

</td><td>

Copy and paste the condition of the existing Start Microsoft Teams chat. Modify the column name as required.

</td></tr><tr><td>

Script

</td><td>

Copy and paste the script of the existing Start Microsoft Teams chat. Modify the column name as required.

</td></tr><tr><td>

Workspace Form Button

</td><td>

Check this box.Copy and paste the **Workspace Client Script**of the existing Start Microsoft Teams chat. Modify the column name as required.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Customize UI actions for IT Service Management with Microsoft Teams](../concept/ui-actions-ms-teams.md)

