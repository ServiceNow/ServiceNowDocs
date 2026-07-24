---
title: Create or modify Dependency Views menu actions
description: To modify an existing menu option, first you create a copy of the original menu action record, and then you modify the copy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/dependency-views/t\_CreateModifyNGBSMMenuActions.html
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or modify Dependency Views menu actions

To modify an existing menu option, first you create a copy of the original menu action record, and then you modify the copy.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## About this task

This ensures that your instance can update the record normally during the upgrade process and allows you to quickly restore the original menu option, if necessary.

## Procedure

1.  To create a new menu option, navigate to **Dependency Views** &gt; **Map Menu Actions** and click **New**.

    Fill in the fields on the form, as appropriate. See the Menu Action form table.

2.  To modify an existing menu option, navigate to **Dependency Views** &gt; **Map Menu Actions**.

3.  Open the menu action you want to edit.

4.  Right-click in the header and click **Insert and Stay**.

    This step creates a duplicate copy of the menu action and leaves it open for editing.

5.  Change the name of the copied record to avoid confusion.

6.  Modify the form fields as necessary and save the record.

7.  Open the original record and disable it by clearing the **Active** check box.

<table id="table_bvs_5tw_dr"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name that appears as the menu option.

</td></tr><tr><td>

Active

</td><td>

Check box that allows you to enable or disable this record.

</td></tr><tr><td>

Condition

</td><td>

Condition that triggers the display of this menu option. If the condition evaluates to **false** the menu option does not display. Script is evaluated in JavaScript in the user's browser and does not have access to all the APIs that Business Rules do. For details on available parameters, see Condition Parameters. .

</td></tr><tr><td>

Item

</td><td>

Map element for which the menu option displays. Valid values are: -   **Canvas** for the menu on the map background.
-   **Node** for the menu on a CI.
-   **Relationship** for the menu on a relationship link.


</td></tr><tr><td>

Order

</td><td>

Physical location of the option in the menu. The option with the lowest order number appears first in the menu. All editable and custom options appear below the permanent menu options.

</td></tr><tr><td>

Script

</td><td>

Script that is executed in the browser when the menu option is selected. Script is evaluated in JavaScript in the user's browser and does not have access to all the APIs that Business Rules do.

</td></tr><tr><td>

Type

</td><td>

Menu action type being created, either a menu option or a menu separator. The menu separator is a single line. When the type is a separator, the **Script** field is ignored.

</td></tr></tbody>
</table>
**Parent Topic:**[Administer Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators]()

[Create or modify map icons]()

[Create a predefined filter]()

[Set a predefined filter as default]()

[Create or modify Map Related Items]()

[Condition and script parameters for menu actions]()

[Create or edit a dependency type]()

