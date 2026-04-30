---
title: Configure the list layout
description: You can configure a list to choose which columns appear in a list, create list views, and create fields on the table.Administrators can configure a property that determines whether fields on extended tables can be added to a parent table list. For example, when this feature is enabled, you can view and filter on the Caller field, from the Incident table, on a Task table list.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# Configure the list layout

You can configure a list to choose which columns appear in a list, create list views, and create fields on the table.

## Before you begin

Role required: personalize\_list

## About this task

Configure the list layout

## Procedure

1.  Navigate to the list you want to configure.

2.  Open the **List controls** menu \(![](../image/list-control-icon.png)\) and select **View** &gt; **\(view name\)**to select the view you want to configure.

3.  Right-click any column heading and select **Configure** &gt; **List Layout**.

4.  Add, remove, or reorder fields to configure the columns displayed and their order of appearance.

    The first non-reference field automatically links to the form view of the record. For this reason, consider using the record number as the first column in the list layout.

5.  Select **Save**.

    **Note:**

    -   If you use [Personal lists](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) and then configure the list view differently, the changes do not appear until you reset your personal list to column defaults.
    -   Inactive fields display in admin-configured lists until an admin updates the list layout to remove them.

If a reference field in a list displays as \(empty\) instead of the expected value, it is due to another field in the list containing an incorrect reference to either an orphaned record or a sys\_id that does not exist in the referenced table. The solution is to remove the incorrect reference data from any reference fields in that table.

**Parent Topic:**[Configuring lists on the ServiceNow AI Platform](../concept/c_ListConfiguration.md)

## Add an extended field to a base table list

Administrators can configure a property that determines whether fields on extended tables can be added to a parent table list. For example, when this feature is enabled, you can view and filter on the **Caller** field, from the Incident table, on a Task table list.

### Before you begin

Role required: admin

**Note:** Enabling this property does not show the extended table fields in the personalize list.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **UI Properties**.

2.  Locate the property **Allow base table lists \(task, cmdb\_ci, etc.\) to include extended table fields \(incident\_state, os\_version, etc.\), and allow filtering on extended table fields** \(**glide.ui.list.allow\_extended\_fields**\).

3.  Select the check box to enable extended fields on parent table lists, or clear the check box to disable the feature.

4.  Select **Save**.


