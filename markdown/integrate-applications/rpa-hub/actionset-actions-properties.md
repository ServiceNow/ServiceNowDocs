---
title: ActionSet actions properties
description: The ActionSet component performs multiple actions and each action has distinct properties. You can update the properties to modify the behavior of the actions.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Actions \(UI\), Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# ActionSet actions properties

The ActionSet component performs multiple actions and each action has distinct properties. You can update the properties to modify the behavior of the actions.

## Click

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the Click action sets in.|
|Before Delay in Seconds|Specified delay before the Click action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to expose a Data In port that takes the Boolean value. If True, the Click action is performed, else, if False, the Click action is not performed. By default, the option is not selected.|
|Name|Option to update the default name of the action. The default name is Click. The updated name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|X|Option to set the custom location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to set the custom location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.|

## Set Text

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to enable or disable the Data In port that takes the text the component sets in the field. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is SetText. The updated name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|X|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.|

## Get Text

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to enable or disable the Data Out port that returns the captured text. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is GetText. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|X|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.|

## Get Table

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to enable or disable the Data Out port that returns the captured table. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is Table. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|X|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.|
|IgnoreHeader|Option to ignore the header of the table while capturing.|

## Get Image

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to enable or disable the Data Out port that returns the captured image. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is GetImage. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Height|Option to specify the height of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|Width|Option to specify the width of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|X|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the Y-axis relative to the anchor.|

## OCR Read Text

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to disable the Data Out port that returns the extracted text. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is OCR. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Height|Option to specify the height of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|Width|Option to specify the width of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|X|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the Y-axis relative to the anchor.|
|Engine|Engine name that is used for extracting the OCR fields.|
|Language|Teseract engine that can support multiple languages. You can select any language listed here.|
|Line Height Tolerance|Font line height.|
|ChangeDPI|If this is enabled, it changes the Dots Per Inch \(DPI\) of Image as mentioned in DPI property.|
|DPI|DPI value.|
|Extract Words|Text that is extracted in words format. Else, it's plain text.|
|Invert|Image color that is inverted. For example, it inverts black to white.|
|Language|Language used to extract.|
|Scale Image|Scaled image by the given number.|
|Threshold|Converted image out of Grayscale image or noise that is removed as per the Threshold value.|
|Threshold Value|Threshold value.|
|Timeout|Time after which the operation times out.|

## OCR Read Table

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to expose the Data Out port that returns the captured table as an output. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is OcrTable. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Height|Option to specify the height of the OCR Read table icon \(![OCR Read Table icon.](../image/ocr-read-table-icon.png)\).|
|Width|Option to specify the width of the OCR Read table icon \(![OCR Read Table icon.](../image/ocr-read-table-icon.png)\).|
|X|Option to specify the location of the OCR Read table icon \(![OCR Read Table icon.](../image/ocr-read-table-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the custom location of the OCR Read table icon \(![OCR Read Table icon.](../image/ocr-read-table-icon.png)\) along the Y-axis relative to the anchor.|
|FirstRowHeader|Option to specify whether the first row of the captured table is a header.|
|Engine|Engine name that is used for extracting the OCR fields.|

## OCR Click Text

|Property|Description|
|--------|-----------|
|Type|Type of action the mouse device performs after the text is identified.|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to expose the Data Out port that returns the captured table as an output. By default, the port is enabled.|
|Name|Option to update the default name of the action. The default name is OCR Click. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Height|Option to specify the height of the OCR Click Text icon.|
|Width|Option to specify the width of the OCR Read table icon.|
|X|Option to specify the location of the OCR Click Text icon along the X-axis relative to the anchor.|
|Y|Option to specify the location of the OCR Click Text icon along the Y-axis relative to the anchor.|
|Engine|Engine name that is used for extracting the OCR fields.|

## Text Selection

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed. This order is assigned when you add an action from the anchor in the ACTIONSET SETTINGS window. You can change the order by dragging and placing the action at the desired order.|
|Expose Port|Option to expose the Data In port that passes the Boolean value to enable or disable the Set Text action.|
|Name|Option to update the default name of the action. The default name is TextSelection. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Trim|Option to trim the spaces at the start and end of the text.|
|Type|Type of action to perform.|
|Height|Option to specify the height of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|Width|Option to specify the width of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\).|
|X|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the X-axis.|
|Y|Option to specify the location of the green rectangle icon \(![Green rectangle icon.](../image/green-rectangle.png)\) along the Y-axis.|

## Send Keys

<table id="table_o4m_dmz_rsb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

After Delay in Seconds

</td><td>

Specified delay after the action sets in.

</td></tr><tr><td>

Before Delay in Seconds

</td><td>

Specified delay before the action sets in.

</td></tr><tr><td>

Delay between each keypress \(Seconds\)

</td><td>

Specified delay between each key press action.

</td></tr><tr><td>

Clear Existing Value

</td><td>

Option to specify if the action will clear the existing value on a field before setting the text.

</td></tr><tr><td>

Execution Order

</td><td>

Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.

</td></tr><tr><td>

Expose Port

</td><td>

Option to enable or disable the Data In port that takes the string. By default, the port is enabled.

</td></tr><tr><td>

Input Type

</td><td>

You can choose from the following options:-   SendInput: Sets text in the fields.
-   SendKeys: Sends the keyboard shortcuts.

</td></tr><tr><td>

Name

</td><td>

Option to update the default name of the action. The default name is SendKeys. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.

</td></tr><tr><td>

Use mouse click to focus

</td><td>

Option to use the mouse device click to focus on the area in the application where the mouse device inputs will be passed.

</td></tr><tr><td>

X

</td><td>

Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.

</td></tr><tr><td>

Y

</td><td>

Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.

</td></tr></tbody>
</table>## Mouse Actions

|Property|Description|
|--------|-----------|
|After Delay in Seconds|Specified delay after the action sets in.|
|Before Delay in Seconds|Specified delay before the action sets in.|
|Execution Order|Order in which the action is executed when multiple actions are set up. This order is assigned when you add an action from the anchor. You can change the order by dragging and placing the action under its anchor at the desired order on the ACTIONSET SETTINGS window.|
|Expose Port|Option to enable or disable the Data In port that takes the Boolean value. If True, the Mouse Action is performed, else, if False, the Mouse Action is not performed. By default, the option is not checked.|
|Name|Option to update the default name of the action. The default name is MouseAction. The name reflects in the ACTIONS LIST section of the ACTIONSET SETTINGS window.|
|Type|Type of mouse device action. For example, paste.|
|X|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the X-axis relative to the anchor.|
|Y|Option to specify the location of the green plus icon \(![Green plus icon.](../image/green-plus-icon.png)\) along the Y-axis relative to the anchor.|

**Parent Topic:**[Actions \(UI\)](../concept/actions-ui.md)

