---
title: Using tags
description: Use tags to filter records and view tagged documents. Remove a tag when it is no longer useful.You can filter records on a table by tags you have access to.The Tagged Documents page displays recently viewed documents or user-tagged documents in the content frame.There are many ways to remove a tag from a record.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-04-04"
reading_time_minutes: 3
breadcrumb: [Tags, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Using tags

Use tags to filter records and view tagged documents. Remove a tag when it is no longer useful.

**Note:** Conditions that use the **Tags** field are not supported in reports or data visualizations based on database views.

**Parent Topic:**[Tags](c_Tags.md)

## Filter records by tag

You can filter records on a table by tags you have access to.

### Before you begin

Role required: none

### Procedure

1.  Filter records by tag in any of the following ways.

<table id="choicetable_fnf_gvq_fs"><tbody><tr><td id="d52626e113">

**Filter from the form view**

</td><td>

Select the more options icon \(![More options icon.](../../using-forms/image/IconUI16MoreOptions.png)\), and then select the tag in the menu that opens. A new tab or window opens and displays a list of records that contain the tag.

</td></tr><tr><td id="d52626e131">

**Filter from the list view using the __Tags__ column**

</td><td>

With the **Tags** column visible, select the tag name. Selecting two or more tags filters the tags together with the AND operator and shows records containing all the selected tags.

</td></tr><tr><td id="d52626e146">

**Filter from the list view using the list filter**

</td><td>

Select the show/hide filter icon \(![Show or hide a filter.](../../using-lists/image/Icon-Condition_builder_UI15.png)\), select **Tags** from the field list and enter the tag name.

</td></tr></tbody>
</table>
## View tagged documents

The Tagged Documents page displays recently viewed documents or user-tagged documents in the content frame.

### Before you begin

Role required: none

### About this task

An administrator can configure the fields that appear on the tagged document cards by configuring the mobile view of the task, for example, the mobile view of the Incident form. If there isn’t a mobile view available for the page, the record reverts to the default view. For more information, see [Create and delete views](../../../administer/navigation-and-ui/task/create-delete-view.md).

### Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Tagged Documents**.

2.  Select **Show Global Tags** to display global tags.

3.  Perform one of the following actions.

<table id="choicetable_gmj_pjw_fs"><tbody><tr><td id="d52626e260">

**Display most recently viewed documents**

</td><td>

Select **Most Recent** in the sidebar.

</td></tr><tr><td id="d52626e272">

**Display documents associated with a tag**

</td><td>

Select the tag name in the sidebar.

</td></tr><tr><td id="d52626e281">

**Remove a tag from a record**

</td><td>

Select the **x** in the corner of the document preview.

</td></tr><tr><td id="d52626e293">

**Open the form for a tagged document**

</td><td>

Select the title of the document preview.

</td></tr></tbody>
</table>
## Remove a tag from a record

There are many ways to remove a tag from a record.

### Before you begin

Role required: none

**Note:** Anyone with access granted to a tag can add or remove the tag from a record.

### Procedure

1.  Perform any of the following actions.

<table id="choicetable_as5_vkw_fs"><tbody><tr><td id="d52626e356">

**Remove a tag from a record in the list view using the __Tags__ column**

</td><td>

Confirm that the **Tags** column is visible and select the remove tag icon \(**x**\) beside the tag name.

</td></tr><tr><td id="d52626e374">

**Remove a tag from one or more records in the list view using the action menu**

</td><td>

Select the check box for one or more records, then select **Actions on selected rows** &gt; **Remove Tag:** &gt; **\[Tag name\]**.

</td></tr><tr><td id="d52626e395">

**Remove a tag from a record in the form view**

</td><td>

Select the more options icon \(![More options icon.](../../using-forms/image/IconUI16MoreOptions.png)\) in the form header, then select the remove tag icon \(**x**\).

</td></tr><tr><td id="d52626e413">

**Remove a tag from a record in the Tagged Documents page**

</td><td>

Select the removed tag icon \(**x**\) in the corner of the document preview.

</td></tr></tbody>
</table>    If a tag is automatically applied to a record based on specific conditions, the tag is automatically removed when those conditions no longer apply. For more information, see [Administering tags](administering-tags.md#).


