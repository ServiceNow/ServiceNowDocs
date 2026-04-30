---
title: Java connector methods
description: The Java connector exposes methods at the connector, screen, and element levels. While all types of elements have common methods, they also have different methods.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Java, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Java connector methods

The Java connector exposes methods at the connector, screen, and element levels. While all types of elements have common methods, they also have different methods.

## Connector level methods

## Start

Starts the Java application from its location and brings it to focus.

**Note:** You must execute this method first.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Path|Path to the Java application in the local drive.|Data in|String|None|Yes|
|Args|Arguments for the path.|Data in|String|None|No|

## GetMainWindowHandle

Returns the window handle of the Java application launched by the Start method.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the Window handle of the application.|Data out|Integer|None|Not applicable|

## GetMainWindowTitle

Returns the title of the Java application window.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the title of the window of the application.|Data out|String|None|Not applicable|

## CloseMainWindow

Closes the main Java application window.

## Terminate

Terminates the main Java application window.

## Screen level methods

## Close

Closes the active Java application window.

## Focus

If the Java application window is minimized or running in the background, the method restores the focus.

## GetFields

Gets the data from the text fields in a Java application. You must first configure the text fields. To configure, do the following steps.

1.  [Configure the Java connector](../task/configure-java-connector.md) and capture one or more text fields.
2.  Expose the screen level methods. See [Use connector method](../task/use-connector-method.md).
3.  From the Object Explorer pane, drag the GetFields method to the Design surface.
4.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
5.  Select one or more text fields.
6.  Update the data type of the text field.
7.  To close the CHOOSE FORM ELEMENTS window, click **OK**.

    A Data Out port is created for each text field you select.


The GetFields method can now return the data contained in the text fields.

## GetInstanceCount

Returns the total number of instances of the Java application open.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the total number of instances of the Java application open.|Data out|Integer|None|Not applicable|

## GetScreenShot

Captures and returns the screenshot of the Java application screen.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the screenshot of the Java application screen.|Data out|Bitmap|None|Not applicable|

## GetWindowHandle

Returns the Windows handle number of the Java application screen window.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the Windows handle number of the Java application screen window.|Data out|Integer|None|Not applicable|

## IsCreated

Returns the Boolean response based on whether the rules for a configured window match. When you configure a Java application screen, the MATCH RULES section of the Java connector window shows certain rules that match the screen configured. The method matches the same rules.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|Notes|
|---------|-----------|--------------|---------|-------------|----------|-----|
|MatchAllChildren|Returns the Boolean response after matching the rules of the elements of the screen.|Data in|Boolean|None|No|This parameter is relevant if you capture one or more elements.|
|Return|Returns the Boolean response to whether the rules of the Java application screen you configured matched.|Data out|Boolean|Null|Not applicable| |

## Maximize

Maximizes the Java application window.

## Minimize

Minimizes the Java application window.

## MouseAction

Performs different mouse device actions on the Java application such as left-click, right-click, and middle-click.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Action|Specifies the mouse device action.|Data in|Mouse device input|None|Yes|
|ClickMiddle|Whether a middle-click will be performed.|Data in|Boolean|None|No|

## Resize

Changes the width, height, and the position of the Java application window along the X and Y axis.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|xPos|Position of the window on the screen along the X-axis.|Data in|Integer|None|No|
|yPos|Position of the window on the screen along the Y-axis.|Data in|Integer|None|No|
|Width|Width of the window.|Data in|Integer|None|No|
|Height|Height of the window.|Data in|Integer|None|No|

## Restore

Restores the original dimensions of the Java application window. You can use the method after you have executed methods like Maximize and Minimize.

## SendKeys

Send any data or keyboard input to the active field on the Java application. For example, you can send a string data "RPA" or a keyboard input \[Space\] to clear a check box.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Keys|Sends the data or keyboard input to the active field.|Data in|String|None|Yes|
|ClearExistingValue|Before sending any data or keyboard input, clears any existing value in the active field.|Data in|Boolean|None|No|
|TypeDelay|Sets a delay before sending any data or keyboard input to the active field.|Data in|Integer|None|No|

## SetFields

Set custom text in the text field elements captured from the Java application screen.

To use the method, do the following steps.

1.  From the Object Explorer, drag the SetFields method to the Design surface.
2.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
3.  Select one or more text fields.
4.  Update the data type of the text field.
5.  Click **OK**.

    A Data In port is created for each text field you select. You can pass the string to set in the fields of the Java application.

    To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).


## WaitForCreate

Each screen you configure in the Java connector is identified by some rules, displayed under the MATCH RULES section of the Java Connector window. The method returns a Boolean response based on whether the rules of the screen you had configured matches.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|timeoutinSeconds|Time after which the operation of the method times out.|Data in|Integer|None|No|
|MatchAllChildren|Returns the Boolean response after matching the rules of the elements of the screen.|Data in|Boolean|None|No|
|Return|Returns the Boolean response to whether the rules of the Java application screen you configured matched.|Data out|Boolean|None|No|

## Element level methods

## GetAccessibleActions

Returns the list of actions that you can perform on an element. For example, for a button, it returns `Click`.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the list of actions that you can perform on an element.|Data out|List|None|Not applicable|

## GetInstanceCount

Returns the total count of an element type in the Java application. For example, if there are three text boxes in an application, the instance count is 3.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the instance count of an element type in the application.|Data out|Integer|None|Not applicable|

## GetText

Returns the text from the captured text box element in the Java application. To capture multiple texts from multiple text boxes, you must configure multiple text box elements.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Text|Returns the text contained in the text box of the Java application.|Data out|String|None|Not applicable|

## IsCreated

Returns the Boolean response depending on whether the rules of the element you had configured match.

|Parameter|Description|Data port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the Boolean response depending on whether the rules of the element you had configured match.|Data out|Boolean|null|Not applicable|

## MouseClick

Performs a left mouse-click on the captured element.

## PerformAction

Performs the specified action on an element. For example, click on a button. Each element allows a set of actions that you can get by executing the GetAccessibleActions method.

To provide inputs to the parameters, see [Configure port properties](../task/configure-input-port-properties.md).

<table id="table_wpx_2wj_4tb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Action

</td><td>

Accepts the action to be performed on the element.

</td><td>

Data in

</td><td>

String

</td><td>

None

</td><td>

Yes

</td><td>

You must specify the action exactly in the format as given by the GetAccessibleActions method.

</td></tr><tr><td>

Return

</td><td>

Returns True if the action was performed, else, False.

</td><td>

Data out

</td><td>

Boolean

</td><td>

None

</td><td>

Not applicable

</td><td>

 

</td></tr></tbody>
</table>## SetPassword

Automate entering password securely in the password field of a Java application.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md).

<table id="table_jrs_nts_vzb"><thead><tr><th>

Parameter

</th><th>

Description

</th><th>

Data Port type

</th><th>

Data type

</th><th>

Default value

</th><th>

Mandatory?

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Password

</td><td>

Accepts the password as a secured string.

</td><td>

Data In

</td><td>

Secured string

</td><td>

None

</td><td>

Yes

</td><td>

Since it accepts the password as a secured string, it only shows the length of the string when you right-click on the parameter and then click **Preview Data**.

</td></tr><tr><td>

UseSendKeys

</td><td>

SendKeys is a method used to send keyboard inputs such as characters, numbers, and symbols to text boxes inside an application.

</td><td>

Data In

</td><td>

Boolean

</td><td>

False

</td><td>

Yes

</td><td>

**Tip:** If the **SetPassword** method fails to input the password in the password field, set the value to **True** and execute the method again.

</td></tr></tbody>
</table>**Parent Topic:**[Java](../concept/java-connector.md)

