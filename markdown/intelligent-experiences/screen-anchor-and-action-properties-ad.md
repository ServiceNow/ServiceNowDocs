---
title: Screen, anchor, and step properties in Agentic Desktop
description: Learn about the properties of screens, anchors, and steps. There are multiple types of steps and each step type has distinct properties. You can update the properties to modify the behavior of the steps.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-11-11"
reading_time_minutes: 3
breadcrumb: [Design desktop actions, Agentic Desktop, Enable AI experiences]
---

# Screen, anchor, and step properties in Agentic Desktop

Learn about the properties of screens, anchors, and steps. There are multiple types of steps and each step type has distinct properties. You can update the properties to modify the behavior of the steps.

## Screen

|Property|Description|
|--------|-----------|
|Name|Unique name for the captured screen. The updated name reflects in the Screens and steps panel.|
|Execution order|Order in which the screen is executed when multiple screens are captured. You can drag the screen at the desired order in the Screens and steps panel.|

## Anchor

|Property|Description|
|--------|-----------|
|Name|Unique name of the added anchor. The updated name reflects in the Screens and steps panel.|
|Execution order|Order in which the anchor is executed when multiple anchors are added.|
|X|Location of the top-left corner of the anchor on the screen along the X-axis.|
|Y|Location of the top-left corner of the anchor on the screen along the Y-axis.|
|Width|Width of the area highlighted as anchor.|
|Height|Height of the area highlighted as anchor.|
|Convert to grayscale|Option to convert the captured screen as a grayscale image. The default value is False.|
|Search in Scale|Option to specify whether the component scales the target image before trying to match the source image. The scaling is done in an increment of 10% each between 100% and 150%. The default value is False.|
|Confidence threshold|Specifies the accuracy in matching the image captured before the component performs a step. The value of 1 defines a 100% match while 0.5 defines 50% match. The default value is 0.95 or 95% match.|
|Retry with scroll|Option to scroll the target image before trying to match the source image.|
|Wait for image|Option to specify if the automation must wait for the image to appear on the screen. The default value is True.|
|Max wait time|Number of seconds to wait for the image or application to appear on the screen.|
|Delay before|Delay in number of seconds before the anchor is executed. The automation waits until the specified time elapses before executing the anchor.|
|Delay after|Delay in number of seconds after the anchor is executed. The automation will wait until the specified time elapses before executing the next anchor.|

## Step

-   **Common properties for steps**

    The following properties apply to all steps - Set Text, Click, Mouse Click, Send Keys, Get Text, Get Table, and OCR Read Text.

    |Property|Description|
    |--------|-----------|
    |Name|Unique name of the step. The updated name reflects in the Screens and steps panel.|
    |Execution order|Order in which this step is executed when multiple steps are set up. This order is assigned when you add a step from the anchor. You can drag the step under its anchor at the desired order in the Screens and Steps panel.|
    |Type|Type of the step, such as Set Text, Get Text, Mouse Click.|
    |Description|Helpful description of this step.|
    |X|Location of the green plus icon ![](../image/ad-green-plus-icon.png) along the X-axis relative to the anchor.|
    |Y|Location of the green plus icon ![](../image/ad-green-plus-icon.png) along the Y-axis relative to the anchor.|
    |Delay before|Delay in seconds before the action is executed.|
    |Delay after|Delay in seconds after the action is executed.|

-   **Set Text**

    |Property|Description|
    |--------|-----------|
    |Value|New text to set in the field.|

-   **Mouse Click**

<table id="table_qyf_lk5_ghc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mouse click type

</td><td>

Type of mouse click action to set for this step:-   Left click
-   Left double click
-   Middle click
-   Right click
-   Right double click
-   Move
-   Drag
-   Drop
-   Scroll down
-   Scroll up
-   Paste


</td></tr></tbody>
</table>-   **Send Keys**

    |Property|Description|
    |--------|-----------|
    |Clear existing value|Option to specify if the step clears the existing value on a field before setting the text.|
    |Value|New text to set in the field.|
    |Focus with mouse click|Option to use the mouse click to focus on the area in the application where the mouse inputs are passed.|

-   **OCR Read Text**

    |Property|Description|
    |--------|-----------|
    |Width|Width of the area in image to recognize and get the text.|
    |Height|Height of the area in image to recognize and get the text.|


