---
title: Windows Connector methods
description: The Windows methods in RPA Desktop Design Studio interact with the Windows applications to perform various tasks. The connector provides methods at different levels of the Windows applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/connectors-windows-methods.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Windows connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Windows Connector methods

The Windows methods in RPA Desktop Design Studio interact with the Windows applications to perform various tasks. The connector provides methods at different levels of the Windows applications.

## Windows connector method levels

[Connector level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-windows-methods.md)

[Window level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-windows-methods.md)

[Element level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-windows-methods.md)

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

    [Path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md)


## Start

Starts the application.

-   **Input**

    [Path](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md) [Args](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md)


## Terminate

Terminates the application.

## Window level methods

## Focus

Sets the focus on a window that is inactive, minimized, or in the background.

## GetFields

Returns the data in the form fields of the screen. You must configure the method before using.

To configure, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon.\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

-   **Output**

    [Form element data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md)


## GetScreenShot

Captures the screenshot of the screen.

-   **Output**

    [Return \(Bitmap\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md)


## IsCreated

Returns the Boolean response depending on whether a specific window matches the rules set in the MATCH CHILDREN section of the configuration window.

-   **Inputs**

    [MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)

-   **Outputs**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)


## Maximize

Maximizes the window.

## Minimize

Minimizes the window.

## SendKeys

Simulates keystrokes on web pages and windows.

-   **Inputs**

    [Keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)

    [ClearExistingValue \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)

    [TypeDelay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)


## SetFields

Sets data in form field types. To set the form fields, you must first configure the method. To configure, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon.\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

-   **Input**

    [Form data field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/method-parameter-windows.md)


## WaitForCreate

Sets delay before a web page or a window loads.

-   **Inputs**

    [timeoutInSeconds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)

    [MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)

-   **Outputs**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/application-level-method-parameters.md)


## Element level methods

These methods are exposed when you double-click an application element under the Global Objects in the Project Explorer.

## Click

Performs a click operation.

## IsCreated

Checks whether an element matches the rules set in the MATCH CHILDREN window.

-   **Outputs**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/element-level-method-parameters.md)


## SendKeys

Simulates keystrokes on web pages and windows.

-   **Inputs**

    [Keys \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/element-level-method-parameters.md)

    [ClearExistingValue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/element-level-method-parameters.md)

    [TypeDelay \(Double\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/element-level-method-parameters.md)


## SetPassword

Automate entering password securely in the password field of a Windows application.

To provide inputs to the fields see [Configure port properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-input-port-properties.md).

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
</table>**Parent Topic:**[Windows connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/windows-connector.md)

