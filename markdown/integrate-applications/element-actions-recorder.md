---
title: Types of elements and actions for the recorder
description: The actions are the activities that you can perform on an application element such as a text box, button, hyperlinks, and so on. By using these actions, you can build an automation flow in the RPA Desktop Design Studio recorder.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Recording automations, Use, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Types of elements and actions for the recorder

The actions are the activities that you can perform on an application element such as a text box, button, hyperlinks, and so on. By using these actions, you can build an automation flow in the RPA Desktop Design Studio recorder.

<table id="table_acg_33t_1wb"><thead><tr><th>

Type of element

</th><th>

Actions

</th></tr></thead><tbody><tr><td>

Button

</td><td>

-   Click \(default\)
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Table

</td><td>

-   GetTable \(default\)
-   Click
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Hyperlink

</td><td>

-   Click \(default\)
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Textbox

</td><td>

-   SetText \(default\)
-   GetText
-   SendKeys
-   DoubleClick
-   Focus

</td></tr><tr><td>

Text area

</td><td>

-   SetText \(default\)
-   GetText
-   SendKeys
-   DoubleClick
-   Focus

</td></tr><tr><td>

Drop-down list

</td><td>

-   SelectItem \(default\)
-   Click
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Check box

</td><td>

-   Check \(default\)
-   Uncheck
-   Click
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Radio button

</td><td>

-   Click \(default\)
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr><tr><td>

Image

</td><td>

-   GetImage \(default\)
-   SendKeys
-   GetText
-   DoubleClick
-   Focus

</td></tr></tbody>
</table>|Action|Description|
|------|-----------|
|Click|Performs the left-click mouse device operation on an element.|
|Check|Performs the select operation on a check box.|
|DoubleClick|Performs the double-click mouse device operation on an element. If the element has a double-click event that is related to it, then the double-click action is performed.|
|Focus|Sets the focus to the element.|
|GetImage|Retrieves the image from an image element. For example, an icon image.|
|GetTable|Retrieves the table data in a tabular format from a table element.|
|GetText|Retrieves the text from an element. For example, text from the house address field in a web page.|
|SendKeys|Simulates the keyboard key or key combinations that are performed on an element.|
|SelectItem|Selects the item in an element.|
|SetText|Sets the specified text to the element.|
|Uncheck|Clears a check box element.|

**Parent Topic:**[Recording automations](../concept/recording-automations.md)

