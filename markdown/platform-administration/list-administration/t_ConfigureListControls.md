---
title: Configure list controls
description: You can configure list controls, such as buttons and filters.The following example shows how to configure a list of related incidents in a problem record to suit specific business needs.
locale: en-US
release: australia
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure list controls

You can configure list controls, such as buttons and filters.

## Before you begin

Role required: personalize\_control

## Procedure

1.  Open a list.

2.  Right-click any column heading and select **Configure** &gt; **List Control**.

3.  Complete the form.

    **Note:** The list control fields that are available for embedded lists are more limited. Unless otherwise noted, the list control fields in the following table are available for both standard and embedded lists.

<table id="table_cpn_n1p_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table for the list or related list. For example, **Change Request \[change\_request\]**. The system automatically sets this value.

</td></tr><tr><td>

Related list

</td><td>

Name of the table and field that define the related list. For example,**sysapproval\_approver.sysapproval**. The system automatically sets this value.

</td></tr><tr><td>

Label

</td><td>

Label to display for this list. Allows an admin to customize the label for a related list or list. If not supplied, the default plural label for the file is used. For example, the label for the Incident table would be **Incidents**.

</td></tr><tr><td>

Omit new button

</td><td>

Option to prevent the **New** button from displaying on this list. Clear the check box to display the **New** button or to control the **New** button with roles \(**New roles** field\). This field is available for standard lists only.

</td></tr><tr><td>

Omit edit button

</td><td>

Option to prevent the **Edit** button from displaying on this list. Clear this check box to display the **Edit** button or to control the **Edit** button with roles \(**New roles** field\). The **Edit** button does not apply to all lists.This field is available for standard lists only.

</td></tr><tr><td>

Omit if empty

</td><td>

Option to omit the **Related List** from the form entirely \(no header\) if there are no entries for the **Related List**.

</td></tr><tr><td>

Omit columns if empty

</td><td>

Option for a top-level list to omit the column headers AND filters/breadcrumbs for an empty column.

</td></tr><tr><td>

Omit filters

</td><td>

Option to hide filters or breadcrumbs for this list. Clear this check box if you always want filters or breadcrumbs or to control filters/breadcrumbs with roles \(**Filter roles** field\). This field is available for standard lists only.

</td></tr><tr><td>

Omit links

</td><td>

Option to hide links for fields that reference other files in this list. Leave this button unchecked to generate links or to control the use of links with roles \(**Link roles** field\).

</td></tr><tr><td>

Omit drill-down link

</td><td>

Option to disable the link to the record from the first column in list view. Users can still select the reference icon to access the record. This field is available for standard lists only.

</td></tr><tr><td>

Hierarchical lists

</td><td>

See [Enable a hierarchical list](t_EnableAHierarchicalList.md). Hierarchical list inserted into a record list. Hierarchical lists enable a user to view the contents of a record's related lists without leaving the record list form. This field is available for standard lists only.

</td></tr><tr><td>

List edit type

</td><td id="entry_ListEditTypeDesc">

Ability for the user to edit values directly in individual cells in a list. The options are: -   **Save immediately \(cell edit mode\):** enables cell editing. The entire row is saved when the user enters a new value.
-   **Save data by rows:** enables cell editing. The row is saved only when the user navigates away from the row or selects the **Save** icon \(![Save icon](../image/IconSave.png)\). This mode allows the user to modify multiple values before saving a record.
-   **Disable list editing:** prevents users from editing cells in the list.
 This field is available for standard lists only.

</td></tr><tr><td>

List edit tag

</td><td>

Unique tag that is sent to a [reference qualifier](../../../script/server-scripting/concept/c_ReferenceQualifiers.md) as the script variable *listEditRefQualTag*. Enter an arbitrary string of letters or numbers.

</td></tr><tr><td>

List edit insert row

</td><td id="entry_ListEditInsRowDesc">

Ability for a user to create records in list view. When it is enabled, an empty row appears at the bottom of the list. This field is available for standard lists only.

</td></tr><tr><td>

Remove pagination count

</td><td>

Option to remove pagination count from the list.

</td></tr><tr><td>

Disable Natural Language Query \(NLQ\)

</td><td>

Option to disable the NLQ filter in specific lists when NLQ on lists is enabled in the instance. The NLQ filter enables you to use natural language to filter lists instead of using the condition builder. For more information on NLQ filters, see Natural Language Query.**Note:** When the system property **com.snc.listv2.nlq.lists.enabled**\(com.snc.listv2.nlq.lists.enabled\) is set to **false**, the query destructs. Text entered in the search replaces existing conditions.

</td></tr><tr><td>

Application

</td><td>

Scope of this setting's applicability. Global means that all workspaces can use this setting.

</td></tr><tr><td>

New roles

</td><td>

User roles that can access the **New** button on this list. Leave the field blank to enable all users to access the **New** button. This option does not apply to embedded lists, which do not contain **New** buttons.

</td></tr><tr><td>

Filter roles

</td><td>

User roles required to have the filter appear in the list. This field is available for standard lists only.

</td></tr><tr><td>

Link roles

</td><td>

User roles required to have links generated for fields that reference other files.

</td></tr></tbody>
</table>
**Parent Topic:**[Configuring lists on the ServiceNow AI Platform](../concept/c_ListConfiguration.md)

## Example of configuring list controls

The following example shows how to configure a list of related incidents in a problem record to suit specific business needs.

### Before you begin

Role required: personalize\_control

### About this task

In this example, a related list label is configured to say `Child Incidents`, not just `Incidents`. The related list is also configured to remove the **New** button to prevent users from creating incidents from the Problem form.

### Procedure

1.  Navigate to a problem record.

2.  Open the list context menu in the **Incidents** related list and select **Configure** &gt; **List Control**.

3.  On the List Control form, change the **Label** field to `Child Incidents`.

4.  Select the **Omit new button** check box.

5.  Select **Submit** to save your changes and return to the previous record, in this case, the problem record.

    In the problem record, the label for the embedded incident list has changed and the **New** button is no longer available.


