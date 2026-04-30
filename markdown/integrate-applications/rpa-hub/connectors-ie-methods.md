---
title: IE Connector methods
description: The IE connector methods perform different tasks on the IE connector, screens, and the elements on the screens. The methods are available at the connector, screen, and the element levels and you can expose the methods by completing appropriate steps.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [IE connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# IE Connector methods

The IE connector methods perform different tasks on the IE connector, screens, and the elements on the screens. The methods are available at the connector, screen, and the element levels and you can expose the methods by completing appropriate steps.

## IE connector method levels

[Connector level methods](connectors-ie-methods.md#IE-connector-level-methods)

[Screen level methods](connectors-ie-methods.md#IE-screen-level-methods)

[Element level methods](connectors-ie-methods.md)

## Connector level methods

## Navigate

Opens a web page based on the URL you specify and returns the Boolean response.

-   **Input**

    [URL](method-parameter-ie.md#URL-IE)

-   **Output**

    [Return \(Boolean\)](method-parameter-ie.md#navigate-output-return-boolean)


## WaitForAnyScreen

The method executes a wait period before a screen loads up. You can specify a timeout after which the method times out the request.

**Input**

[MatchAllChildren](method-parameter-ie.md#MatchAllChildren)

[Timeout](method-parameter-ie.md#Timeout-ie)

## Screen level methods

## DownloadFile

Downloads a file from the screen or web page based on the URL and file name you specify.

-   **Input**

    [Url](method-parameter-ie.md#downloadfile-input-url)

    [fileName](method-parameter-ie.md#downloadfile-input-filename)

-   **Output**

    [Return \(Boolean\)](method-parameter-ie.md#downloadfile-output-return-boolean)


## ExecuteJavaScript

Executes custom JavaScript on an application or website open on the IE browser. You must configure the method before executing.

To configure the JavaScript, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Enter the custom script under the JAVA SCRIPT section.
3.  To add parameter to the script, click the add parameter icon \(![Add parameter icon.](../image/add-image-icon.png)\) under the PARAMETER heading.

    **Note:** A Data In port is added with each parameter.

4.  Click **OK**.

-   **Input**

    [Parameter](method-parameter-ie.md#executejavascript-input-parameter)

-   **Output**

    [Return \(Object\)](method-parameter-ie.md#executejavascript-output-return-object)


## GetValueByXPath

Converts an XPath and returns the output as a string.

-   **Input**

    [XPath \(String\)](method-parameter-ie.md#getvaluebyxpath-input-xpath)

-   **Output**

    [Return \(String\)](method-parameter-ie.md#getvaluebyxpath-output-return)


## GetValuesByXPath

Returns the values within columns based on the specified XPath expression.

**Input**

You must configure the XPath expressions before executing the method. To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Update the name of the column.
3.  Define the XPath expression.
4.  Click **OK**.

**Output**

Returns the data table after the operation.

## Hide

Hides the active browser window.

## Restore

Restores the browser window hidden using the Hide method.

## GetURL

Returns the URL of the website or web page.

**Output**

[Return \(String\)](method-parameter-ie.md#geturl-output-return)

## WaitForCreate

Sets a delay before a web page or a window loads.

**Inputs**

[timeoutInSeconds](method-parameter-ie.md#waitforcreate-input-timeoutinseconds)

[MatchAllChildren](method-parameter-ie.md#MatchAllChildren)

**Outputs**

[Return \(Boolean\)](method-parameter-ie.md#waitforcreate-output-return-boolean)

## SetFields

Sets the data in form field types.

## SendKeys

Simulates the keystrokes on web pages and windows.

**Inputs**

[Keys](method-parameter-ie.md#sendkeys-input-keys)

[MatchAllChildren](method-parameter-ie.md#sendkeys-input-matchallchildren)

[TypeDelay](method-parameter-ie.md#sendkeys-input-TypeDelay)

## Minimize

Minimizes the window.

## Maximize

Maximizes the window.

## IsReady

Returns the Boolean response to the request to check whether the website is ready to accept requests from methods.

**Output**

[Return \(Boolean\)](method-parameter-ie.md#isready-output-return-boolean)

## MatchChildren

Matches all elements of a web page that you have captured and returns a Boolean response accordingly. You can configure whether the method should match all children.

**Input**

[matchAllChildren](method-parameter-ie.md#matchallchildren-input-matchAllChildren)

**Output**

[Return \(Boolean\)](method-parameter-ie.md#matchallchildren-output-return-boolean)

## IsCreated

Returns the Boolean response to the request to find whether a website on an Internet Explorer browser is open. You can optionally have the method check whether all captured elements of the website matches.

-   **Inputs**

    [MatchAllChildren](method-parameter-ie.md#MatchAllChildren)

-   **Output**

    [Return \(Boolean\)](method-parameter-ie.md#iscreated-output-boolean)


## Refresh

Reloads the contents of the active web page.

## SaveAs

Saves the active web page to the local disk.

## Print

Prints the active web page in the browser.

**Input**

[NoPrompt](method-parameter-ie.md#print-input-noprompt)

## GetPageSource

Returns the page source of the active window open on the IE browser.

**Output**

[Return \(String\)](method-parameter-ie.md#getpagesource-output-return)

## GetScreenShot

Returns the screen shot of a window or area in a window.

**Output**

[Return \(Bitmap\)](method-parameter-ie.md#getscreenshot-output-return-bitmap)

## GetTitle

Returns the title of a window open in the IE browser.

**Output**

[Return \(String\)](method-parameter-ie.md#gettitle-output-string)

## GetFields

Accesses data in the forms returns the data as output. You must configure the method before executing.

To configure, do the following steps.

1.  Click the method settings icon \(![Method settings icon.](../image/component-settings-icon.png)\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

**Output**

[Form field](method-parameter-ie.md#getfields-output-formfield)

## Focus

Sets the focus on a window that is running in the background or minimized and makes it active.

**Output**

[Return \(Boolean\)](method-parameter-ie.md#focus-output-return-boolean)

## Close

Closes the active window.

## Element level methods

These methods are exposed when you double-click an application element under the Global Objects in the Project Explorer.

## Click

Performs a click operation on the element.

## GetInnerHTML

Gets the inner HTML of the element.

**Output**

[Return \(String\)](method-parameter-ie.md#GetInnerHTML-output-return-string)

## GetInnerText

Gets the inner text of an element.

**Output**

[Return \(String\)](method-parameter-ie.md#GetInnerText-output-return-string)

## GetOuterHTML

Gets the outer HTML of the element.

**Output**

[Return \(String\)](method-parameter-ie.md#GetOuterHTML-output-return-string)

## GetURL

Gets the URL of the element.

**Output**

[Return \(String\)](method-parameter-ie.md#GetURL-output-return-string)

**Parent Topic:**[IE connector](../concept/internet-explorer-connector.md)

