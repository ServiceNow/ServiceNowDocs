---
title: Group dashboard elements
description: Improve your layout control and dashboard customization capabilities, by organizing related elements into single visual and logical units. Configure backgrounds and borders according to group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/group-db-elements.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Edit a dashboard, Working with in-line dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Group dashboard elements

Improve your layout control and dashboard customization capabilities, by organizing related elements into single visual and logical units. Configure backgrounds and borders according to group.

## Before you begin

The system property **par.dashboard.widget.group.enabled.dashboards.list** must be enabled on your instance with a value of ALL, -1, or the sys\_id of the dashboard you want to group content on. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md).

Role required: If you have an internal role, you can create dashboards with the inline editor. You must have edit rights on the dashboard to group its content.

**Note:** If you are in a different application than the dashboard you're editing, a message prompts you to choose the correct scope. If you don't change the scope, you are able to change the dashboard, but you won’t be able to save those changes.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the dashboard that you want to group elements on.

3.  Select **Edit**.

4.  Select the first item that you want to group and select the Grouping icon \(\[Omitted image "icon-group-dashboard.png"\] Alt text:\) from the item's header menu.

    \[Omitted image "header-menu-group-option.png"\] Alt text: Selected visualization with arrow pointing to the Group option

    Each element on the dashboard shows a check box that you can select to add that element to the group.

5.  Select the check boxes of the elements that you want to add to the group.

6.  Select **Confirm Group** from the header to complete the grouping.

    \[Omitted image "group-db-elements.png"\] Alt text: Shows check boxes to select to group three dashboard elements

7.  \[Omitted image "modify-group-ungroup-db-elements.png"\] Alt text: Elements group menu with the Modify and Ungroup options highlighted

8.  Specify background and border colors.

9.  Select **Save**.

10. Modify the grouped elements or ungroup them.


## Result

Grouped elements on the dashboard remain together when elements on the dashboard are moved. These elements also share a border and background as though they were one unit.

**Parent Topic:**[Edit Platform Analytics dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/edit-db-in-ac.md)

