---
title: Save and use filters in a list view
description: Depending on your access rights, you may save filters for everyone, a user group, or yourself. You can apply saved filters and edit or delete them.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Save and use filters in a list view

Depending on your access rights, you may save filters for everyone, a user group, or yourself. You can apply saved filters and edit or delete them.

## Before you begin

Role required: varies depending on action. See procedure.

**Note:** A new Create ACL allows all users to save filters by default. This ACL overrides any custom ACLs in place if administrators are restricting filter access. The new ACL gives all users access to the User field by default, and access to the Group field only if users have the filter\_group role and are in the currently selected group.

## Procedure

1.  Navigate to a list and create or modify a filter as described in [Create a filter in List](t_CreatingFilters.md).

2.  Select **Save...**.

    Additional options for saving the filter display.

    ![Save filter options](../image/save_filters.png)

3.  Enter a name for the filter in the **Save as:** field.

4.  Select one of the following visibility options.

<table id="choicetable_v1q_3x2_pv"><tbody><tr><td id="d51171e109">

**Me**

</td><td>

Creates a personal filter, which only you can access. If you don’t have Write access to the User field, this option isn't available. See your administrator for more information.

</td></tr><tr><td id="d51171e121">

**Everyone**

</td><td>

Creates a global filter, which all users can access. This option is available to users with the filter\_global role.

</td></tr><tr><td id="d51171e130">

**Group**

</td><td>

Creates a group filter, which only members of the user group you select can access. This option is available to users with the filter\_group role. If you don’t have Write access to the Group field, this option isn’t available. See your administrator for more information.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  To use your saved filter, return to the list, select the List control menu \(![](../image/list-control-menu.png)\), and select your filter from the Filters submenu.

7.  To edit or delete your personal filters, return to the list, select the List control menu \(![](../image/list-control-menu.png)\), and select **Edit personal filters** from the Filters menu.

    1.  Review the Filters list and select the title of the filter to edit.

        If no results display, select the Show/hide filter icon \(![](../image/show-hide-filters.png)\) and remove any applied filters.

    2.  Update the filter title or add or remove conditions.

    3.  To delete the filter, select **Delete** and confirm deletion.

    4.  If you edited the filter, select **Update**.


**Parent Topic:**[Filters and breadcrumbs](../concept/c_UsingFiltersAndBreadcrumbs.md)

