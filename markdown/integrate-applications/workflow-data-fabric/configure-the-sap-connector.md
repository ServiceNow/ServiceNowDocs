---
title: Configure the SAP connector
description: Capture one or more SAP application screens, UI elements on the screen, and then expose the methods at the application, screen, or element levels by configuring the SAP connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/configure-the-sap-connector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [SAP connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Configure the SAP connector

Capture one or more SAP application screens, UI elements on the screen, and then expose the methods at the application, screen, or element levels by configuring the SAP connector.

## Before you begin

Ensure that the SAP plugin on the RPA Desktop Design Studio is installed. For more information, see [Manage plugins in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/install-plugins-rpa-studio.md).

Ensure that at least one SAP application window is active or open on your machine.

The SAP application must support these environments:

-   Windows – Windows 10, Windows 11, Windows Server 2016, Windows Server 2019
-   SAP ECC EH8 Client
-   .Net 4.7.1

Role required: none

## Procedure

1.  Navigate to **Connectors** &gt; **SAP**.

2.  Drag the SAP connector under the Global Objects in the Project Explorer pane.

    To learn more about how to add the SAP connector, see [Use a connector in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-connector.md).

    The SAP Application object is added under the Global Objects.

    \[Omitted image "SAP-object-added.png"\] Alt text: SAP Application object added under Global Objects.

3.  Under the Global Objects, right-click the SAP Application and select **Configure**.

4.  In the **SAP Connector** window, select the drop-down and then select the SAP application screen.

    \[Omitted image "SAP-connector-drop-down.png"\] Alt text: SAP screen selection drop down.

    **Note:** To load any SAP application window that you have opened after opening the **SAP Connector** window, select the Refresh icon \(\[Omitted image "SAP-connector-refresh.png"\] Alt text: Refresh icon.\).

5.  Select **Add Window**.

    The application screen appears in the WINDOWS pane.

6.  To close the SAP Connector window, select **OK**.

    The SAP application screens that you added appear under the Global Objects in the Project Explorer pane.

    \[Omitted image "SAP-screens-added-under-connector.png"\] Alt text: SAP applications added under SAP application object.

7.  To expose the application-level methods, double-click the SAP application object under Global Objects in the Project Explorer pane.

    The application-level methods appear under the Object Explorer pane.

8.  To expose the screen-level methods, select the SAP Application object expand icon \(\[Omitted image "SAP-connector-expand-icon.png"\] Alt text: Expand icon.\) and double-click the SAP application.

    \[Omitted image "SAP-connector-expose-screen-methods.png"\] Alt text: Expand and double-click SAP screen.

    The screen-level methods appear under the Object Explorer pane.

9.  To expose the element-level methods, do the following steps.

    1.  In the Project Explorer pane, under Global Objects, right-click the SAP Connector object.

    2.  Select **Configure**.

    3.  In the **SAP Connector** window, in the WINDOWS pane, right-click the SAP application screen that you had added.

    4.  Select **Add Element**.

        The Capture element dialog appears.

    5.  Use the Capture element dialog to capture one or more SAP application screen elements.

        For more information about how to use the Capture element dialog, see [Use the Capture element dialog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/use-context-dialog.md).

    6.  To expose the element-level methods, in the Project Explorer pane, expand the SAP Connector under Global Objects.

    7.  Under SAP Connector, expand the name of the screen you had captured.

    8.  Double-click the screen element that you had captured.

        The screen element-level methods appear under the Object Explorer pane.


