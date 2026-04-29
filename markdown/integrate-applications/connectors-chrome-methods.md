---
title: Chromium connector methods
description: The Chromium connector methods do different tasks on the applications, screens, and the elements on the screens of the Google Chrome and the Microsoft Edge browsers.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Chromium connector, Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
---

# Chromium connector methods

The Chromium connector methods do different tasks on the applications, screens, and the elements on the screens of the Google Chrome and the Microsoft Edge browsers.

## Chromium connector method levels

[Application level methods](connectors-chrome-methods.md#chrome-screen-level-methods)

[Screen level methods](connectors-chrome-methods.md#chrome-screen-level-methods)

[Element level methods](connectors-chrome-methods.md#chrome-element-level-methods)

## Application level methods

## Navigate

Launches the web page based on the URL specified.

To provide inputs, see [Configure port properties](../task/configure-input-port-properties.md)

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Url|URL of the web page.|Data In|String|No default value|No|
|Timeout|Option to specify the time in seconds after which the operation times out.|Data In|Integer|No default value|No|
|Return|If True, the web page has launched. Else, if False, the web page hasn't launched.|Data Out|Boolean|Not applicable|Not applicable|

## WaitForAnyScreen

Sets a delay before the specified screens load.

To specify the screen, do the following steps:

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  On the CHOOSE SCREENS window, select the required screen.
3.  Click **OK**.

To provide inputs to the fields, see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|Notes|
|---------|-----------|--------------|---------|-------------|----------|-----|
|MatchAllChildren|If True, before loading the screen, the method matches the captured elements from the web page. Else, if False, the method doesn't match any element.|Data In|Boolean|No default value|No|The elements can be found in the MATCH CHILDREN section of the Chromium Connector window.|
|Timeout|Specifies the time in seconds after which the operation times out.|Data In|Integer|No default value|No| |

## Screen level methods

## Close

Closes the captured screen window.

## Focus

Sets the focus on the captured window.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|If True, the focus was set on the captured window. Else, if False, the focus wasn't set on the captured window.|Data out|Boolean|No default value|Not applicable|

## GetFields

Returns the values of the specified fields or elements. For example, it can return the text in a button.

To specify the fields, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  In the CHOOSE FORM ELEMENTS window, select the required fields.
3.  Click **OK**.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Name of the field or element|Field or element for which the method returns the value.|Data out|String|No default value|Not applicable|

## GetInnerHtml

Returns the inner HTML of the captured screen.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the inner HTML of the captured screen.|Data out|Object|Not applicable|Not applicable|

## GetPageSource

Returns the page source of the captured screen.

|Parameter|Description|Data Port Type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the page source of the captured screen.|Data Out|String|Not applicable|Not applicable|

## GetScreenShot

Returns the screenshot of the configured screen.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the screenshot of the configured screen.|Data out|Bitmap|No default value|Not applicable|

## GetTitle

Returns the title of the web page captured.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the title of the web page captured.|Data out|String|No default value|Not applicable|

## GetURL

Returns the URL of the web page that was captured.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the URL of the web page that was captured.|Data out|String|No default value|Not applicable|

## GetValueByXPath

Returns the value within an XML node from the specified XML path.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|XPath|XPath of the web page captured.|Data In|String|No default value|No|
|Return|Returns the value from the XML node.|Data out|String|Not applicable|Not applicable|

## IsCreated

Returns the Boolean value based on whether the screen is rendered successfully on the web application.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data Port type|Data type|Default type|Mandatory?|Notes|
|---------|-----------|--------------|---------|------------|----------|-----|
|MatchAllChildren|If True, before the screen is rendered, the method attempts to match all captured elements. Else, if False, no match is done.|Data In|Boolean|No default value|No|You can find the captured elements in the MATCH CHILDREN section of the Chromium Connector window.|
|Return|If True, the screen is rendered successfully. Else, if False, the screen has failed to render successfully.|Data out|Boolean|Not applicable|Not applicable| |

## Element level methods

## Click

Performs a click operation on the element.

## Focus

Sets the focus on the element.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|scrollIntoView|If True, the method uses the scrollbar to navigate to the captured element on the web page. Else, if False, it doesn't scroll to the captured element.|Data In|Boolean|No default value|No|
|Return|If True, the method sets focus on the element. Else, if False, the method has failed to set focus on the element.|Data Out|Boolean|Not applicable|Not applicable|

## GetInnerHTML

Returns the inner HTML of the captured element.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the inner HTML of the captured element.|Data Out|String|No default type|Not applicable|

## GetInnerText

Returns the inner text in the captured element.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the inner text in the captured element.|Data Out|String|Not applicable|Not applicable|

## GetOuterHTML

Returns the HTML element and its attributes, start, and end tags of the captured element.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the outer HTML of the captured element.|Data out|String|No default value|Not applicable|

## GetOuterText

Returns the text content of the captured element.

|Parameter|Description|Data Port Type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|Returns the text content of the captured element.|Data out|String|No default value|Not applicable|

## IsCreated

Returns the Boolean status of whether the captured element has loaded.

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Return|If True, the captured element has loaded. Else, if False, the captured element has failed to load.|Data out|Boolean|No default value|Not applicable|

## SetPassword

Automate entering password securely in the password field of a web-based application, for example securely enter password in the password field of a login form.

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
</table>## SendKeys

Passes shortcut keys to the captured element.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md).

|Parameter|Description|Data Port type|Data type|Default value|Mandatory?|
|---------|-----------|--------------|---------|-------------|----------|
|Keys|Takes the shortcut keys.|Data In|String|No default value|No|
|ClearExistingValue|If True, the method clears any existing value in the field. Else, if False, it doesn't clear the existing value.|Data In|Boolean|No default value|No|
|TypeDelay|Sets the typing delay between each key.|Data In|Double|No default value|No|

## GetInstanceCount

Returns a count of the number of instances where the element is available.

## GetOuterHTML

Gets the outer HTML of the captured element.

## SendKeys

Simulates keystrokes on web pages and windows.

-   **Inputs**

    [ClearExistingValue](../reuse/element-level-method-parameters.md#parameters-common-input-clearexistingvalue)

    [TypeDelay](../reuse/element-level-method-parameters.md#parameters-common-input-typedelay)


## SimulateMouseEvent

Simulates the mouse event you specify on an element on a web-based application. For example, simulate a right mouse-click on an element.

**Important:** To simulate a mouse event on an element, it must already have that specific event defined in the web page HTML. For example, to simulate the `contextmenu` event on an element, the element must already have the `contextmenu` event defined in the HTML.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md)

<table id="table_kqf_hxc_xzb"><thead><tr><th>

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

MouseEvent

</td><td>

Mouse event that occurs on the captured web page element. At the time of the mouse event occurring on a web page element, that element must already have the mouse event defined in the HTML.

</td><td>

Data In

</td><td>

MouseEventType

</td><td>

click

</td><td>

Yes

</td><td>

The method supports these mouse events.-   click
-   dblclick
-   mousedown
-   mouseup
-   mouseover
-   mousemove
-   mouseout
-   contextmenu

</td></tr><tr><td>

MouseButton

</td><td>

Simulates the mouse button click on the captured web page element.

</td><td>

Data In

</td><td>

MouseButtonType

</td><td>

Left

</td><td>

Yes

</td><td>

The method supports these mouse button actions.-   left
-   middle
-   right

</td></tr></tbody>
</table>## SimulateEvent

Simulates the HTML event that you specify on a Google Chrome page or an element on the page.

To provide inputs to the fields see [Configure port properties](../task/configure-input-port-properties.md)

<table id="table_zlh_5kw_rzb"><thead><tr><th>

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

</th></tr></thead><tbody><tr><td>

EventName

</td><td>

Name of the HTML event. The method supports the events provided and you must enter the name of the event exactly as specified.HTML events

-   load
-   unload
-   abort
-   error
-   select
-   change
-   submit
-   reset
-   focus
-   blur
-   resize
-   scroll

</td><td>

Data In

</td><td>

String

</td><td>

None

</td><td>

Yes

</td></tr></tbody>
</table>**Parent Topic:**[Chromium connector](../concept/chrome-connector.md)

