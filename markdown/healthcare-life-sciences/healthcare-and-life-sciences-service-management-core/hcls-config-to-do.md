---
title: Configure the service portal to add a to-dos menu item for completing healthcare-related tasks
description: Enable the to-dos menu item that uses the HCLS to dos \(hcls-todo-list\) widget for displaying to-do items on a service portal.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configure the service portal to add a to-dos menu item for completing healthcare-related tasks

Enable the to-dos menu item that uses the HCLS to dos \(hcls-todo-list\) widget for displaying to-do items on a service portal.

## Before you begin

Set the application scope to Global using the application picker. For more information, see Application picker.

Role required: admin

## About this task

The HCLS to dos \(hcls-todo-list\) service portal widget is pre-configured to display to-do items for patients. By default, the widget is included in the hcls\_todos page provided with the Healthcare and Life Sciences Service Management Core application. In this procedure, you add a menu item to a patient portal to access the hcls\_todos page.

## Procedure

1.  Navigate to **All** &gt; **Service portal** &gt; **Menus**.

2.  Select the header menu for the patient portal.

3.  In the Menu Items related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_qmn_yth_5qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name that appears for the item in the menu.

</td></tr><tr><td>

Parent Menu

</td><td>

This field is automatically set to the name of the menu you are adding items to. You can change the value as required to other menus.

</td></tr><tr><td>

Type

</td><td>

Page the item links to. For example, you can link to another page in the portal, or an external URL. Form fields vary depending on the option you select from this list.

</td></tr><tr><td>

Order

</td><td>

Value that determines where the item appears in the menu in relation to other menu items.

</td></tr><tr><td>

Page

</td><td>

Name of the portal page the item links to.

 To use the hcls\_todos page provided with the application, set the value to the `hcls_todos`.

</td></tr><tr><td>

Condition

</td><td>

Conditions required for menu items to show in the header.

</td></tr><tr><td>

Glyph

</td><td>

Icon that appears beside the menu item.

</td></tr></tbody>
</table>5.  Click **Save**.


