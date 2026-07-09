---
title: IE Connector methods
description: The IE connector methods perform different tasks on the IE connector, screens, and the elements on the screens. The methods are available at the connector, screen, and the element levels and you can expose the methods by completing appropriate steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/connectors-ie-methods.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [IE connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# IE Connector methods

The IE connector methods perform different tasks on the IE connector, screens, and the elements on the screens. The methods are available at the connector, screen, and the element levels and you can expose the methods by completing appropriate steps.

## IE connector method levels

[Connector level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connectors-ie-methods.md)

[Screen level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connectors-ie-methods.md)

[Element level methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connectors-ie-methods.md)

## Connector level methods

## Navigate

Opens a web page based on the URL you specify and returns the Boolean response.

-   **Input**

    [URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

-   **Output**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)


## WaitForAnyScreen

The method executes a wait period before a screen loads up. You can specify a timeout after which the method times out the request.

**Input**

[MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

[Timeout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## Screen level methods

## DownloadFile

Downloads a file from the screen or web page based on the URL and file name you specify.

-   **Input**

    [Url](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

    [fileName](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

-   **Output**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)


## ExecuteJavaScript

Executes custom JavaScript on an application or website open on the IE browser. You must configure the method before executing.

To configure the JavaScript, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon.\).
2.  Enter the custom script under the JAVA SCRIPT section.
3.  To add parameter to the script, click the add parameter icon \(\[Omitted image "add-image-icon.png"\] Alt text: Add parameter icon.\) under the PARAMETER heading.

    **Note:** A Data In port is added with each parameter.

4.  Click **OK**.

-   **Input**

    [Parameter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

-   **Output**

    [Return \(Object\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)


## GetValueByXPath

Converts an XPath and returns the output as a string.

-   **Input**

    [XPath \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

-   **Output**

    [Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)


## GetValuesByXPath

Returns the values within columns based on the specified XPath expression.

**Input**

You must configure the XPath expressions before executing the method. To configure, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon.\).
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

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## WaitForCreate

Sets a delay before a web page or a window loads.

**Inputs**

[timeoutInSeconds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

[MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

**Outputs**

[Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## SetFields

Sets the data in form field types.

## SendKeys

Simulates the keystrokes on web pages and windows.

**Inputs**

[Keys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

[MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

[TypeDelay](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## Minimize

Minimizes the window.

## Maximize

Maximizes the window.

## IsReady

Returns the Boolean response to the request to check whether the website is ready to accept requests from methods.

**Output**

[Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## MatchChildren

Matches all elements of a web page that you have captured and returns a Boolean response accordingly. You can configure whether the method should match all children.

**Input**

[matchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

**Output**

[Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## IsCreated

Returns the Boolean response to the request to find whether a website on an Internet Explorer browser is open. You can optionally have the method check whether all captured elements of the website matches.

-   **Inputs**

    [MatchAllChildren](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

-   **Output**

    [Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)


## Refresh

Reloads the contents of the active web page.

## SaveAs

Saves the active web page to the local disk.

## Print

Prints the active web page in the browser.

**Input**

[NoPrompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetPageSource

Returns the page source of the active window open on the IE browser.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetScreenShot

Returns the screen shot of a window or area in a window.

**Output**

[Return \(Bitmap\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetTitle

Returns the title of a window open in the IE browser.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetFields

Accesses data in the forms returns the data as output. You must configure the method before executing.

To configure, do the following steps.

1.  Click the method settings icon \(\[Omitted image "component-settings-icon.png"\] Alt text: Method settings icon.\).
2.  Select the form elements.
3.  Update the form element data type.
4.  Click **OK**.

**Output**

[Form field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## Focus

Sets the focus on a window that is running in the background or minimized and makes it active.

**Output**

[Return \(Boolean\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## Close

Closes the active window.

## Element level methods

These methods are exposed when you double-click an application element under the Global Objects in the Project Explorer.

## Click

Performs a click operation on the element.

## GetInnerHTML

Gets the inner HTML of the element.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetInnerText

Gets the inner text of an element.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetOuterHTML

Gets the outer HTML of the element.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

## GetURL

Gets the URL of the element.

**Output**

[Return \(String\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/method-parameter-ie.md)

**Parent Topic:**[IE connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/internet-explorer-connector.md)

