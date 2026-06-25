---
title: Configure when a related list loads
description: If there are many related lists on a form or many records in the related lists, the form may load slowly. You can improve form response times by configuring related lists to load manually, on demand, or automatically, after the rest of the form loads.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/t\_ConfigureWhenARelatedListLoads.html
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

1.  Navigate to \[Omitted image "user-menu-icon.png"\] Alt text: User menu icon. **User Menu** &gt; **Preferences** &gt; **Display**.

2.  Select one of the following options from the **Loads related lists in classic forms** menu.

<table id="choicetable_rmk_dk5_1r"><tbody><tr><td id="d87156e86">

**With the Form**

</td><td>

Related lists load when you open the form, which is the default setting. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `default`.

</td></tr><tr><td id="d87156e101">

**After Form Loads**

</td><td>

Related lists load after the rest of the form loads. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `deferred`.

</td></tr><tr><td id="d87156e116">

**On-demand**

</td><td>

Related lists load on demand. When this option is selected, a **Load Related Lists** button appears at the bottom of each form that contains related lists. Select the button to load related lists. When selected, it sets the value of the glide.ui.related\_list\_timing user preference to `ondemand`.

</td></tr></tbody>
</table>3.  Close the display preferences menu.


**Parent Topic:**[Related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list]()

[Create a default filter for a related list]()

[Configure the edit option]()

[Create defined related lists]()

[Add fields to selections in a related list]()

[Create a default filter for list selector records]()

