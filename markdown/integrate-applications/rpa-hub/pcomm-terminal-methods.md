---
title: IBM Personal Communications emulator methods
description: Use the IBM Personal Communications emulator methods to perform various automation tasks on the IBM Personal Communications emulator.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Terminal connector methods, Terminal \(Mainframe\) connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# IBM Personal Communications emulator methods

Use the IBM Personal Communications emulator methods to perform various automation tasks on the IBM Personal Communications emulator.

## Screen-level methods

Use screen-level methods to perform the automation tasks on the emulator screen. For example, you can simulate a command on the screen or get text from the screen.

## GetFieldText

Returns the text that a field contains after it identifies the field by the row and column number that you specify. The row and column that you specify are the starting point of the field. The method identifies the whole field and then returns the text in the field. In the following example, `H` is the first letter and the starting point in the field and `Host OS :` is the complete text in the field.

![Screen that shows the first letter in the field and the complete text in the field.](../image/terminal-connector-getfieldtext.png)

![The GetFieldText method with its parameters.](../image/terminal-conn-getfieldtext.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Row|Field row number that identifies the field.|Data In|Integer|NA|Yes| |
|Column|Field column number that identifies the field.|Data In|Integer|NA|Yes| |
|Return|Returns the text in the field.|Data Out|String|NA|NA| |

## GetTextFromRect

Returns the text in all the fields of a rectangular area that you define on the screen. You define an area by providing the starting and ending rows and column numbers. The method locates and identifies the first and the last fields and returns all the text in all the fields within that area. The following example shows the area that you defined.

![Area that you defined to show the first cell of the first field and the last cell of the last field.](../image/gettextfromrectmethod.png)

![GetTextFromRect method image.](../image/terminal-conn-gettextfromrect.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|StartRow|Row number that indicates the first character of the first field in the rectangular area.|Data In|Integer|NA|Yes| |
|StartCol|Column number that contains the first character of the first field in the rectangular area.|Data In|Integer|NA|Yes| |
|EndRow|Row number that contains the last character of the last field in the rectangular area.|Data In|Integer|NA|Yes| |
|EndCol|Column number that contains the last character of the last field in the rectangular area.|Data In|Integer|NA|Yes| |
|Return|Returns the text from all the fields within the rectangular area.|Data Out|String|NA|NA| |

## IsCreated

Verifies whether the emulator screen exists based on the screen match rule and can accept inputs from the user. After verification, the method returns the appropriate Boolean value.

![IsCreated method.](../image/terminal-conn-iscreated.png)

<table id="table_scg_qsc_51c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port entry type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

MatchAllChildren

</td><td>

Option to find the emulator screen by matching the child elements that you have captured.

</td><td>

Data In

</td><td>

Boolean

</td><td>

False

</td><td>

Yes

</td><td>

**Warning:** Using this option may slow down the method.

</td></tr><tr><td>

Return

</td><td>

Returns the Boolean value depending on whether emulator screen exists based on the screen match rule and can accept inputs from the user.

</td><td>

Data Out

</td><td>

Boolean

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr></tbody>
</table>## SearchText

Returns the numbers of the row and column that holds the first character of the text that you specify. For example, if you specify the string `emulator`, the method returns the row and column numbers of the starting point of the word `emulator` which is `e`.

**Note:** If you provide the text that spans multiple fields, the Row and Col ports return 0 because the method supports the text only from a single field.

![SearchText method.](../image/terminal-conn-search-text.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Text|Text that the method searches.|Data In|String|NA|Yes|The text you specify may be case-sensitive depending on the emulator you use.|
|Row|Row number that has the first character of the text you specify.|Data Out|Integer|NA|NA|If the text that you specify occurs at multiple rows and columns, the method returns the first row and column that contains the text.|
|Col|Column number that has the first character of the text that you specify.|Data Out|Integer|NA|NA|If the text that you specify occurs at multiple rows and columns, the method returns the first row and column that contains the text.|

## SendKeys

Simulates the keystrokes that you enter from the keyboard at the mouse device position on the emulator screen. For example, you can simulate the **\[enter\]** keystroke on the screen.

![SendKeys method.](../image/terminal-conn-sendkeys.png)

<table id="table_qwx_cdc_w1c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port entry type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Keys

</td><td>

Keystrokes that you enter from your keyboard.

</td><td>

Data In

</td><td>

String

</td><td>

None

</td><td>

Yes

</td><td>

**Tip:** To learn about the keystrokes, refer the respective terminal emulator documentation.

</td></tr></tbody>
</table>## SendKeysSecure

Simulates the keystrokes that is a secured string at the mouse device position on the emulator screen.

![SendKeysSecure method.](../image/terminal-conn-sendkeyssecure.png)

<table id="table_ews_ps4_w1c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port entry type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Keys

</td><td>

Keystrokes that you enter as a secured string.

</td><td>

Data In

</td><td>

Secured String

</td><td>

None

</td><td>

Yes

</td><td>

**Tip:** To learn about the keystrokes, refer to the respective terminal emulator documentation.

</td></tr></tbody>
</table>## SetCursorPosition

Attempts to set the mouse device at the row and column number that you specify.

![SetCursorPosition method.](../image/setcursorposition-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Row|Option to provide the number of the row based on which the method attempts to set the mouse device on the screen.|Data In|Integer|NA|NA|The row number must be positive and within the size of the emulator screen. For example, if the screen size is 24X80, the maximum value that you can provide for a row is 24.|
|Col|Option to provide the number of the row based on which the method attempts to set the mouse device on the screen.|Data In|Integer|NA|NA|The column number must be positive and within the size of the emulator screen. For example, if the screen size is 24X80, the maximum value that you can provide for a column is 80.|

## WaitForCreate

Waits for the duration that you specify while the connector uses the screen match rule to find whether the screen exists.

![WaitForCreate method.](../image/waitforcreate-method.png)

<table id="table_trs_cwc_51c"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port entry type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

timeoutinSeconds

</td><td>

Option to provide the number of seconds for which the method waits while the connector uses the screen match rule to find if the screen exists.

</td><td>

Data In

</td><td>

Integer

</td><td>

30

</td><td>

Yes

</td><td>

 

</td></tr><tr><td>

MatchAllChildren

</td><td>

Option to match all screen elements that you had captured to find if the screen exists.

</td><td>

Data In

</td><td>

Boolean

</td><td>

False

</td><td>

Yes

</td><td>

**Warning:** Using this option may delay the execution of the method.

</td></tr><tr><td>

Return

</td><td>

Returns the Boolean value based on whether the emulator screen was found.

</td><td>

Data Out

</td><td>

Boolean

</td><td>

NA

</td><td>

NA

</td><td>

 

</td></tr></tbody>
</table>## Element-level methods

Element-level methods perform automation tasks on the emulator screen elements that you add from the Terminal Connector screen. You can add a screen element as a field or a table.

## GetAsTable

Returns the text that you captured as a data table object. Use this method when you capture the data from a screen as a table. However, you can also use the method for the data that you capture as a field. To learn how to capture the data as a table, see [Configure the IBM Personal Communications emulator](../task/pcomm-emulator.md).

![GetAsTable method.](../image/GetAsTable-element-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Return|Returns the captured text from the terminal screen as a data table object.|Data Out|Data Table|NA|NA|To view the table, right-click the parameter and select **Preview Data**.|

## GetText

Returns the text in the field that you captured from the emulator screen. If you use this method for a table that you captured, it returns the text in the first field of the rectangle.

![GetText method.](../image/gettext-element-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|Notes|
|---------|-----------|--------------------|---------|-------------|----------|-----|
|Return|Returns the text from the captured field.|Data Out|String|NA|NA| |

## IsCreated

Matches the rules and verifies whether the captured element exists.

![IsCreated method.](../image/iscreated-element-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Return|Returns the Boolean value based on whether the element is active.|Data Out|Boolean|NA|NA| |

## SetText

Attempts to set the text to the field.

![SetText method.](../image/settext-element-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|Text|Option to specify the text that the method attempts to set in the field.|Data In|String|NA|Yes|You can't use this method on protected emulator screens.|

## WaitForCreate

Waits for the duration that you specify while the connector uses the match rule to find whether the element exists.

![WaitForCreate method.](../image/waitforcreate-element-method.png)

|Parameter|Description|Data port entry type|Data type|Default value|Mandatory|Notes|
|---------|-----------|--------------------|---------|-------------|---------|-----|
|timeoutinSeconds|Option to provide the number of seconds for which the method waits while the connector uses the match rule to find whether the element exists.|Data In|Integer|30|Yes| |
|Return|Returns the Boolean value depending on whether the element was found.|Data Out|Boolean|NA|NA| |

**Parent Topic:**[Terminal connector methods](connectors-terminal-methods.md)

