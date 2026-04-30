---
title: Enable a hierarchical list
description: You can enable hierarchical lists to make data from related lists directly accessible from within a v2 list.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable a hierarchical list

You can enable hierarchical lists to make data from related lists directly accessible from within a v2 list.

## Before you begin

Role required: personalize\_control

## About this task

Hierarchical lists enable a user to view the contents of the related lists of a record without leaving the record list form.

**Note:** You cannot enable a hierarchical list view for an embedded list. Hierarchical lists are not supported in List v3, even if they are enabled.

## Procedure

1.  Right-click any column header, and select **Configure** &gt; **List Control** from the context menu.

2.  Select the **Hierarchical lists** check box in the List Control dialog box and then click **Submit** or **Update**.

3.  Click the arrow for a record number to display the related lists for the record.

    ![Hierarchical list](../image/HierarchicalList.png)


-   **[Use list controls in hierarchical lists](t_SelectARelatedList.md)**  
By default, no related list tabs are visible in a hierarchical list and only a single related list is displayed at a time. The column headers are hidden by default.

**Parent Topic:**[List administration](../../core-configuration/concept/p_ListAdministration.md)

