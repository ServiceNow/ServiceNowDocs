---
title: Configure content rendering parameter
description: A content rendering parameter functions similarly to video hosting URL parameters, allowing content managers to customize the viewer's experience through an interface element in the Rich Content Editor. Depending on the hosting provider, this can include defining a checkbox for enabling full screen or autoplay, or a textbox for specifying the start time.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Video hosting integrations framework, Setup employee communications, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure content rendering parameter

A content rendering parameter functions similarly to video hosting URL parameters, allowing content managers to customize the viewer's experience through an interface element in the Rich Content Editor. Depending on the hosting provider, this can include defining a checkbox for enabling full screen or autoplay, or a textbox for specifying the start time.

## Before you begin

-   Role required: sn\_cd.content\_admin
-   Complete the steps to [Configure content provider and mapping](configure-content-provider.md)

## Procedure

1.  If you have already opened a Content Provider, click the Content Provider Mapping **Preview record** icon, click **Open Record**, then open the **Content Rendering Parameters** related list.

    Navigate to **All** &gt; **Content Publishing** &gt; **Content Provider Configs** &gt; **Content Rendering Parameters**.

2.  Click **New**.

    Fill in the form fields:

<table id="table_z4f_r4p_lzb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Provider mapping

</td><td>

Select the Content provider that connects Content Publishing to the video hosting service

</td></tr><tr><td>

Label

</td><td>

Appears in the Settings panel to identify the element for Content Managers \(for example, autoplay or loop\)

</td></tr><tr><td>

Type

</td><td>

Choose from:-   Checkbox
-   Text


</td></tr><tr><td>

Render checked on UI?\(Appears when you select checkbox\)

</td><td>

Determines whether this check box is selected by default in the Rich Content Editor.

</td></tr><tr><td>

Append this query parameter to content URL

</td><td>

The query parameter that controls the element \(for example autoplay or loopvideo\)

</td></tr><tr><td>

Default Value

</td><td>

Sets the default value for the Content Library interface

</td></tr><tr><td>

Active

</td><td>

Makes this element available for use in the Content Library interface

</td></tr><tr><td>

Hide parameter

</td><td>

Hides this parameter from the Rich Content Editor interface, preventing it from being modified

</td></tr><tr><td>

Order

</td><td>

Where this element appears in relation to other custom elements, with the lowest value appearing higher on the screen

</td></tr></tbody>
</table>3.  Click **Save**.


