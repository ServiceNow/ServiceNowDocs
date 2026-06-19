---
title: SAP Connector methods
description: The SAP connector provides various methods that you can use to automate workflows on SAP graphical user interface \(GUI\) interfaces. SAP connector methods are available at different levels - connector, screen, and element.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/sap-connector-methods.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [SAP connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# SAP Connector methods

The SAP connector provides various methods that you can use to automate workflows on SAP graphical user interface \(GUI\) interfaces. SAP connector methods are available at different levels - connector, screen, and element.

## SAP Connector methods

The SAP Connector methods are available at three levels.

-   **Application**: You can find these methods when you double-click the SAP connector object. To access these methods, do the following steps:
    1.  Add the SAP connector under the **Global Objects** in the **Project Explorer** pane.

        For more information, see [Configure the SAP connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-the-sap-connector.md).

    2.  Double-click the SAP connector object.

        The methods appear in the Object Explorer pane.

-   **Screen**: Use these methods to automate tasks on an SAP application screen that you have added. For example, automate the maximizing of an application window. To access these methods, do the following steps:
    1.  Add one or more SAP application screens. To learn to configure, see [Configure the SAP connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-the-sap-connector.md).
    2.  Double-click the screen that you've added.

        The methods appear in the Object Explorer pane.

-   **Element**: Use these methods to automate actions on the SAP screen UI elements, for example, a button or a check box. For example, automate the selecting of a button. To access these methods, do the following steps:
    1.  Add one or more SAP application screens. To learn to configure, see [Configure the SAP connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-the-sap-connector.md).
    2.  Capture one or more screen elements. To learn to capture, see [Use the Capture element dialog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-context-dialog.md).

        The screen elements appear under the captured SAP screen.

    3.  Double-click the screen element.

        The methods appear in the Object Explorer pane.


## Use the methods

To create an automation by using the methods, drag them from the Object Explorer pane to the Design surface and connect them.

\[Omitted image "SAP-connector-methods-connected.png"\] Alt text: Methods connected.

## Application-level methods

-   **OpenConnection**

    Establishes a connection between the connector and the SAP application. You must first use this method before executing an automation.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |name|Name of the connection.|Data In|String|None|Yes|
    |username|User name for making the connection.|Data In|String|None|Yes|
    |password|Password for making the connection.|Data In|String|None|Yes|

-   **SetDefaultSession**

    Makes the selected session a default session.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |sessionId|Unique Id of the session that you want to set as default.|Data In|String|None|Yes|

-   **CloseConnection**

    Closes the connection between the connector and the SAP application.


## Screen-level methods

-   **ClickMenuItem**

    Selects the menu item that you specify the ID of on the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuId|The ID of the menu that must be selected.|Data In|String|None|Yes|

-   **Close**

    Closes the session of the SAP screen.

-   **CreateSession**

    Creates a session of the SAP screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |tCode|Transaction code that enables you to access specific part of the SAP application.|Data In|String|NA|Yes|
    |Return|Returns the Id of the session created.|Data Out|String|NA|NA|

-   **EndSession**

    Ends the open session.

-   **EndTransaction**

    Ends a transaction.

-   **Focus**

    Sets the focus on the open session.

-   **GetMenuItem**

    Gets the name of the specified menu item.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuId|ID of the menu item to get the name.|Data In|String|None|Yes|
    |Return|Returns the name of the menu item|Data Out|String|None|NA|

-   **GetMenuItemsIdsByName**

    Retrieves the ID of the menu that you specify by its name.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |menuItemName|Name of the menu item.|Data Out|List|None|NA|

-   **GetWindowHandle**

    Returns the window handle of the SAP application screen.

-   **IsCreated**

    Returns `true` if the session is created, `false` if the session isn’t created.

-   **IsSessionBusy**

    Returns `true` if the session is busy, and `false` if the session isn’t busy.

-   **Maximise**

    Maximizes the SAP screen.

-   **Minimise**

    Minimizes the SAP screen.

-   **Resize**

    Resizes the SAP screen according to the dimensions specified.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |xPos|Position of the screen along the X-axis.|Data In|Integer|None|Yes|
    |yPos|Position of the screen along the Y-axis.|Data In|Integer|None|Yes|
    |Width|Width of the screen.|Data In|Integer|None|Yes|
    |Height|Height of the screen.|Data In|Integer|None|Yes|

-   **Restore**

    Restores the screen to its original dimensions.

-   **ScreenId**

    Returns the ID of the SAP application screen as a string.

-   **SendKeys**

    Sends the keyboard strokes to the SAP application screen.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |Keys|Keyboard strokes that you want to send to the SAP screen.|Data In|String|NA|Yes|

-   **StartTransaction**

    Starts a transaction.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |tCode|Transaction code that enables you to access specific part of the SAP application.|Data In|String|NA|Yes|

-   **WaitForCreate**

    Waits for the specified duration while the screen is being created. This enables all the dynamic controls to load after the screen is created.

    |Parameter|Description|Data port entry type|Data type|Default value|Mandatory?|
    |---------|-----------|--------------------|---------|-------------|----------|
    |timeoutInSeconds|Duration after which the method times out.|Data In|Integer|None|Yes|
    |MatchAllChildren|Option to indicate whether before loading the screen, the method matches all the captured children screens and elements with the screen.|Data In|Boolean|False|No|


## Element-level methods

In the SAP connector, you can use these element-level methods to identify elements, verify their presence on the screen, or define actions to be performed on the elements.

The following tables include elements and their available methods. For the description of these methods and their parameters, see [SAP Connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-connector-methods.md).

|Element|Methods|
|-------|-------|
|GuiButton|[Click](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiCheckBox|[Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsChecked](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Uncheck](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiComboBox|[Get](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetIconName](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetList](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiCtrlGridView|[ClickButtonCell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ClickCell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[DeselectAllRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetCellType](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetCellValue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetColumns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetColumnsKeyValuePair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetRowCount](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetRowsByColumn](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetSelectedColumns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetSelectedRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetSingleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetVisibleRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectAllRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectCell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemById](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemByPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemByText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectSingleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectToolbarMenuItemById](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectToolbarMenuItemByPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectToolbarMenuItemByText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetCellValue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiLabel|[GetText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiPassword|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetCaretPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiRadioButton|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsChecked](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Select](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiStatusBar|[GetStatus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiTab|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectTab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiTableControl|[DeselectAllVisibleRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[DeselectRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[DeselectVisibleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetAllVisibleRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetColumnNames](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetMaximumScrollOffset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetScrollPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetSingleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetTable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetVisibleRowCount](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollDownByOneRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToHorizontalPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToNextPage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToPreviousPage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToVerticalPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollUpByOneRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectAllRows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectSingleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectVisibleRow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiTextBox|[GetText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetCaretPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiTree|[Check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ClickNodeItem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[CollapseNodeItem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[DoubleClickNode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[DoubleClickNodeItem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetColumnsKeyValuePair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetTreeType](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetNodeKeyByPath](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetNodeKeyByText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetNodeItemText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetSelectedNodes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[GetNodeItemCheckBoxState](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[PressNodeItemButton](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectTab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectNodeItem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectNode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemById](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemByText](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SelectContextMenuItemByPosition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[Uncheck](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

|Element|Methods|
|-------|-------|
|GuiUserArea|[Highlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[IsCreated](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[MouseClick](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToNextPage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[ScrollToPreviousPage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SendKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetFocus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetHorizontalScroll](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[SetVerticalScroll](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|
|[WaitForCreate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/sap-element-methods.md)|

