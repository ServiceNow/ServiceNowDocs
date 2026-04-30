---
title: Configure the Rocket BlueZone emulator
description: Configure the Rocket BlueZone emulator on the RPA Desktop Design Studio by capturing the Rocket BlueZone emulator screens and their elements. After capturing the screens, you can use the screen and element methods to automate actions on the screens and elements.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure the Terminal connector, Terminal \(Mainframe\) connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Configure the Rocket BlueZone emulator

Configure the Rocket BlueZone emulator on the RPA Desktop Design Studio by capturing the Rocket BlueZone emulator screens and their elements. After capturing the screens, you can use the screen and element methods to automate actions on the screens and elements.

## Before you begin

Add the Terminal connector object to the Global Objects list in the Project Explorer pane so the Terminal connector is available to all the activities, components, and connectors in the automation project.

Start an emulator session and connect it to a server.

Role required: none

## Procedure

1.  Navigate to the Project Explorer pane **&gt; Global Objects** and right-click the **TerminalSession** object.

2.  Select **Configure**.

    ![Configure option that you navigated to in Step 1.](../image/terminal-connector-right-click-object.png)

3.  On the Terminal Connector window, select **Bluezone**.

    ![BlueZone emulator option selection in the Terminal Connector window.](../image/terminal-conn-bluezone-selection.png)

    **Tip:** To load a BlueZone emulator screen that doesn't appear in the list, select the refresh icon \(![Screen refresh icon.](../image/connector-refresh-icon.png)\).

4.  Capture a BlueZone emulator screen.

    1.  In the BlueZone list, select a BlueZone Mainframe emulator screen.

        ![BlueZone emulator session selection.](../image/terminal-conn-bluezone-screen-selection.png)

        **Note:** When the BlueZone emulator establishes a connection with the server, a session is created with the name of the session. For example, the name of the session in the example is A.

    2.  Select **Add Screen**.

        The emulator screen is added and appears in the Screens and elements pane and under the TerminalSession object in the Project Explorer pane.

        ![BlueZone emulator screen added in the terminal Connector window and Project Explorer.](../image/terminal-conn-bluezone-screen-added.png)

        When you capture multiple screens and elements and want to automate tasks on one screen or element, the connector must first find the screen or element by using the match rules. To know about the match rules, see [Use the screen or element match rules](find-the-screen-or-element-to-perform-automation.md).

5.  Capture an element from the BlueZone emulator screen.

    1.  Right-click the screen that you have captured and select **Add Element**.

        ![Add Element option for BlueZone screen.](../image/PCOMM-capture-element.png)

    2.  In the TERMINAL PREVIEW screen, move your mouse device to the element that you want to capture.

        The element displays its information.

        ![BlueZone emulator screen field information.](../image/PCOMM-emulator-text-info.png)

    3.  Add the element as a single field by right-clicking the element and selecting **Add as Field**.

        The data in a Mainframe screen is displayed within fields. The BlueZone emulator screen in the RPA Desktop Design Studio indicates a field with a rectangle. The following image shows a field.

        ![Mainframe screen field.](../image/terminal-conn-mainframe-field.png)

        When you select **Add as Field**, the connector treats the element as a field that displays the data or enables data entry. With this option, you can get the text or data from a field and then enter the data in a form.

    4.  Add fields after selecting them in a tabular format.

        To add fields after selecting them in a tabular format, select the contiguous fields that create a tabular format. The following example shows how you must select the fields to capture them in a tabular format.

        ![Field selection. For the text description, refer to the text that follows this example.](../image/terminal-conn-fields-as-table.png)

        Select the fields.

        1.  Select the first field in the tabular area that you have identified.
        2.  On your keyboard, press **Shift**.
        3.  Select the last field in the tabular area that you have identified.
        Right-click and select **Add as Table**.

    5.  In the context dialog box, enter the name of the field or table in the **NAME** field.

        ![Context dialog box that shows the POSITION, LENGTH, and NAME fields.](../image/terminal-connector-context-dialog.png)

    6.  Select the Add Field icon ![Add field icon.](../image/add-element-icon-RPA.png).

        To capture more elements, you can repeat steps 5a through 5f.

    7.  Close the **TERMINAL PREVIEW** screen by selecting **OK**.

        The element is added and appears in the Screens and elements pane in the Terminal Connector screen under the TerminalScreen\_0 object.

        ![Text field added in the Screens and elements pane under the TerminalSession_0 object.](../image/PCOMM-text-field-added.png)

6.  Use the screen match rules to enable the terminal connector to locate a screen or element.

    When you capture multiple screens, fields, or tables and want to automate tasks on one screen or element, the connector must first find the screen or element. To enable the connector to find the screen or element, use the screen match rules at [Use the screen or element match rules](find-the-screen-or-element-to-perform-automation.md).

7.  View the screen and element methods.

    1.  View the screen-level methods under the TerminalSession object in the Project Explorer pane by double-clicking the screen that you captured.

        The methods appear in the Object Explorer pane.

    2.  View the element-level methods in the Project Explorer pane by navigating to the element under the screen that you captured and double-clicking the element.

        The methods appear in the Object Explorer pane.


**Parent Topic:**[Configure the Terminal connector](../concept/configure-terminal-connector.md)

**Related topics**  


[Rocket BlueZone emulator methods](../reference/bluezone-emulator-methods.md)

