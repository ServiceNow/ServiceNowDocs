---
title: Methods and events of an attended automation form
description: Learn about the methods and events of an attended automation form in RPA Desktop Design Studio.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [RPA Desktop Design Studio reference, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Methods and events of an attended automation form

Learn about the methods and events of an attended automation form in RPA Desktop Design Studio.

The methods and events of the attended automation form are displayed in the Object Explorer pane.

## Methods

<table id="table_bmt_41m_rrb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GetFields

</td><td>

Gets the text from the selected fields.

</td></tr><tr><td>

Hide

</td><td>

Hides the form.

</td></tr><tr><td>

SetFields

</td><td>

Sets the text for the selected fields.

</td></tr><tr><td>

SetTitle

</td><td>

Sets the title of the designed form.

</td></tr><tr><td>

Show

</td><td>

Displays the designed form.

</td></tr><tr><td>

ShowBusy

</td><td>

Displays the Busy icon.-   If True, displays that the designed form is in busy mode with message, if any.
-   If False, displays that the designed form is in normal mode.

</td></tr><tr><td>

ShowPopup

</td><td>

Displays a message in a pop-up window.

</td></tr><tr><td>

UpdateProgress

</td><td>

Provides visual feedback in the form as a progress bar. Set the percentage of the progress as required.

</td></tr></tbody>
</table>## Events

|Method|Description|
|------|-----------|
|OnOpen|Occurs when the form is opened.|
|OnClose|Occurs when the form is closed.|

**Parent Topic:**[RPA Desktop Design Studio reference](rpa-studio-reference.md)

**Related topics**  


[Create an attended automation form in RPA Desktop Design Studio](../task/create-rda-form.md)

