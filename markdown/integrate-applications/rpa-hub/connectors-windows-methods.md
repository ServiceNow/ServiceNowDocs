---
title: Windows Connector methods
description: The Windows methods in RPA Desktop Design Studio interact with the Windows applications to perform various tasks. The connector provides methods at different levels of the Windows applications.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Windows connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Windows Connector methods

The Windows methods in RPA Desktop Design Studio interact with the Windows applications to perform various tasks. The connector provides methods at different levels of the Windows applications.

## Windows connector method levels

[Connector level methods](connectors-windows-methods.md#connector-level-windows)

[Window level methods](connectors-windows-methods.md#windows-screen-level-methods)

[Element level methods](connectors-windows-methods.md#windows-element-level-methods)

## Connector level methods

## CloseMainWindow

Closes the active window of the application.

## GetMainWindowHandle

Retrieves the handle ID of the active window of the application.

## GetMainWindowTitle

Retrieves the title of the active window of the application.

## SetWorkingDirectory

Sets the working directory of the application for all file operations through the application to be performed in the specified directory.

-   **Input**

    [Path](method-parameter-windows.md#Path-windows)


## Start

Starts the application.

-   **Input**

    [Path](method-parameter-windows.md#Path-windows) [Args](method-parameter-windows.md#Args-windows)


## Terminate

Terminates the application.

## Window level methods

## Focus

Sets the focus on a window that is inactive, minimized, or in the background.

## GetFields

Returns the data in the form fields of the screen. You must configure the method before using.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

-   **Output**

    [Form element data](method-parameter-windows.md#GetFields-output-formelementdata)


## GetScreenShot

Captures the screenshot of the screen.

-   **Output**

    [Return \(Bitmap\)](method-parameter-windows.md#GetScreenShot-return-Bitmap)


## IsCreated

Returns the Boolean response depending on whether a specific window matches the rules set in the MATCH CHILDREN section of the configuration window.

-   **Inputs**

    [MatchAllChildren](../reuse/application-level-method-parameters.md#common-parameter-input-matchallchildren)

-   **Outputs**

    [Return \(Boolean\)](../reuse/application-level-method-parameters.md#common-parameter-output-return-boolean-iscreated)


## Maximize

Maximizes the window.

## Minimize

Minimizes the window.

## SendKeys

Simulates keystrokes on web pages and windows.

-   **Inputs**

    [Keys](../reuse/application-level-method-parameters.md#common-parameter-inputs-keys)

    [ClearExistingValue \(Boolean\)](../reuse/application-level-method-parameters.md#common-parameter-input-ClearExistingValue)

    [TypeDelay](../reuse/application-level-method-parameters.md#common-parameter-input-typedelay)


## SetFields

Sets data in form field types. To set the form fields, you must first configure the method. To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

-   **Input**

    [Form data field](method-parameter-windows.md#setfields-input-Formdatafield)


## WaitForCreate

Sets delay before a web page or a window loads.

-   **Inputs**

    [timeoutInSeconds](../reuse/application-level-method-parameters.md#common-parameter-input-timeoutInSeconds)

    [MatchAllChildren](../reuse/application-level-method-parameters.md#common-parameter-input-matchallchildren)

-   **Outputs**

    [Return \(Boolean\)](../reuse/application-level-method-parameters.md#common-parameter-output-Return-Boolean-waitforcreate)


## Element level methods

These methods are exposed when you double-click an application element under the Global Objects in the Project Explorer.

## Click

Performs a click operation.

## IsCreated

Checks whether an element matches the rules set in the MATCH CHILDREN window.

-   **Outputs**

    [Return \(Boolean\)](../reuse/element-level-method-parameters.md#parameter-common-output-iscreated)


## SendKeys

Simulates keystrokes on web pages and windows.

-   **Inputs**

    [Keys \(String\)](../reuse/element-level-method-parameters.md#parameter-common-sendkeys-keys-string)

    [ClearExistingValue](../reuse/element-level-method-parameters.md#parameters-common-input-clearexistingvalue)

    [TypeDelay \(Double\)](../reuse/element-level-method-parameters.md#parameters-common-input-typedelay)


## SetPassword

Automate entering password securely in the password field of a Windows application.

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
</table>**Parent Topic:**[Windows connector](../concept/windows-connector.md)

