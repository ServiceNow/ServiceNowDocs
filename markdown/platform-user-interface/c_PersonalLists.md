---
title: Personal lists
description: You can create personal lists to customize which columns appear and the order in which they appear. Personal lists modify a specific list view according to your individual preferences.You can personalize a specific list view based on your individual preferences.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Personal lists

You can create personal lists to customize which columns appear and the order in which they appear. Personal lists modify a specific list view according to your individual preferences.

Personal list customizations don’t affect what other users see in their lists. Administrators can [manage](https://www.servicenow.com/docs/access?context=c_AdministeringPersonalLists&version=australia&pubname=australia-platform-administration&ft:locale=en-US) the personal lists function.

**Parent Topic:**[Lists in the classic environment](c_UseLists.md)

## Personalize a list

You can personalize a specific list view based on your individual preferences.

### Before you begin

Role required: personalize\_list or admin

### Procedure

1.  Open the list.

2.  Select the personalize list icon \(![Personalize list icon](../image/PersonalizeListIcon.png)\) in the right corner.

3.  Select the columns and the desired order.

    ![Personalize list columns](../image/PersonalizeListColumns.png)

    **Note:**

    -   Values in the first column appear as links. If the first column isn’t a reference field, the link opens the record from the list, as expected. If the first column is a reference field, the link opens the record from the referenced table. This behavior can be confusing. For this reason, avoid using a reference field as the first column.
    -   If an inactive field is removed from an admin-configured default view, any personal lists will reset to follow the default view, thus removing the inactive field from the personal list.
4.  Select display options.

    **Note:** These options apply to all lists, not just the view you’re personalizing.

<table id="choicetable_qgk_vbz_3r"><tbody><tr><td id="d42208e171">

**Display long text on more than one line**

</td><td>

Select the **Wrap column text** check box. Clear the check box to display text on one line.In Core UI, this option is also available in the **Lists** section of the [system settings](../../../administer/navigation-and-ui/reference/r_UI16BannerFrame.md).

</td></tr><tr><td id="d42208e202">

**Condense the vertical space between rows**

</td><td>

Select the **Compact rows** check box. Clear the check box to use standard row spacing.

</td></tr><tr><td id="d42208e214">

**Highlight list rows as the cursor passes over them**

</td><td>

Select the **Active row highlighting** check box. Clear the check box to restore the static, alternate row highlighting.

</td></tr><tr><td id="d42208e226">

**Use updated field status indicators**

</td><td>

Select the **Modern cell coloring** check box.In Core UI, this option is also available in the **Lists** section of the [system settings](../../../administer/navigation-and-ui/reference/r_UI16BannerFrame.md).

</td></tr></tbody>
</table>5.  Select list editing options \(requires you to configure the list editor\).

    **Note:** These options apply to all lists, not just the view you’re personalizing.

<table id="choicetable_ofx_lcz_3r"><tbody><tr><td id="d42208e272">

**Allow the list editor to open for the list**

</td><td>

Select the **Enable list edit** check box. Clear the check box to prevent the list editor from opening for the list.

</td></tr><tr><td id="d42208e284">

**Open the list editor with a double-click**

</td><td>

Select the **Double click to edit** check box. Clear the check box to open the list editor using a single select.

</td></tr></tbody>
</table>6.  Select **OK**.

    The list reloads to show the changes.


### What to do next

To reset a list to the default layout, select the personalize list icon and select the **Reset to column defaults** button.

