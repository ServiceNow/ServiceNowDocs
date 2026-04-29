---
title: Configure when a related list loads
description: If there are many related lists on a form or many records in the related lists, the form may load slowly. You can improve form response times by configuring related lists to load manually, on demand, or automatically, after the rest of the form loads.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure when a related list loads

If there are many related lists on a form or many records in the related lists, the form may load slowly. You can improve form response times by configuring related lists to load manually, on demand, or automatically, after the rest of the form loads.

## Before you begin

Role required: none

## About this task

## Procedure

1.  Navigate to ![User menu icon.](../../../get-started/servicenow-overview/image/user-menu-icon.png) **User Menu** &gt; **Preferences** &gt; **Display**.

2.  Select one of the following options from the **Loads related lists in classic forms** menu.

<table id="choicetable_rmk_dk5_1r"><tbody><tr><td id="d79912e86">

**With the Form**

</td><td>

Related lists load when you open the form, which is the default setting. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `default`.

</td></tr><tr><td id="d79912e101">

**After Form Loads**

</td><td>

Related lists load after the rest of the form loads. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `deferred`.

</td></tr><tr><td id="d79912e116">

**On-demand**

</td><td>

Related lists load on demand. When this option is selected, a **Load Related Lists** button appears at the bottom of each form that contains related lists. Select the button to load related lists. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `ondemand`.

</td></tr></tbody>
</table>3.  Close the display preferences menu.


**Parent Topic:**[Related lists](../concept/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list](t_SelectRelatedRecords.md)

[Create a default filter for a related list](t_CreateADefaultFilter.md)

[Configure the edit option](t_ConfigureTheEditOption.md)

[Create defined related lists](../../../administer/form-administration/task/t_CreateDefinedRelatedLists.md)

[Add fields to selections in a related list](../../../administer/form-administration/task/t_AddingFieldsToARelatedList.md)

[Create a default filter for list selector records](../../../administer/form-administration/task/t_CreateDefaultRelatedRecSecFilter.md)

