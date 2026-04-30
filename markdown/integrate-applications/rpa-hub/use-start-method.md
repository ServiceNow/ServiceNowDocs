---
title: Use the Start method for Universal App Connector
description: Use the Start method to launch a browser or an application for the Universal App Connector \(UAC\) object. You can use this method if you want a browser or application to start before interacting with any application screens or elements.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the Start method for Universal App Connector

Use the Start method to launch a browser or an application for the Universal App Connector \(UAC\) object. You can use this method if you want a browser or application to start before interacting with any application screens or elements.

## Before you begin

Role required: None

## About this task

**Note:** If the application type that you select for the Start method is Google Chrome or Microsoft Edge browser, then the same browser must be selected from the **Browser** list in the Configure screen and elements window of UAC.

## Procedure

1.  In the Toolbox pane, navigate to **Connectors** and drag **Universal App Connector** to **Global Objects** in Project Explorer.

    The connector is added as a **Universal Application** object in Global Objects. You can rename this UAC object from here.

2.  Double-click the UAC object and drag the **Start** method from the Object Explorer to the Design surface.

3.  Complete the following parameters in the Start component:

<table id="table_ucm_psl_fwb"><thead><tr><th>

Parameter name

</th><th>

Parameter description

</th><th>

Required?

</th></tr></thead><tbody><tr><td>

AppType

</td><td>

Opens the Port Properties dialog. The options available are **Chrome**, **Edge**, and **Application**.If you select **Chrome** or **Edge** from the **Static Value** list, the selected browser opens in a new tab. For more information on how to configure port properties, see [Configure port properties](configure-input-port-properties.md).

 If you select **Application** from the **Static Value** list, you must provide the full path of the application in the **Path** parameter of the Start method.

</td><td>

Yes

</td></tr><tr><td>

Path

</td><td>

Full navigation path of the application that you want to open. The path is entered in string format.For example, `D:\TestApps\JavaTest.jar`

</td><td>

No

</td></tr><tr><td>

StartParams

</td><td>

Arguments for the launch application. For example, if you select Google Chrome as the application and provide `google.com` as the argument, the Google web page is opened when the browser is launched.

</td><td>

No

</td></tr></tbody>
</table>4.  Double-click the required application screen or element and the Object Explorer pane is displayed listing the related methods.

    For example, if you select a Java application screen or element, the Java connector methods are displayed in Object Explorer.

    -   For more information on Java connector methods, see [Java connector methods](../reference/java-connector-methods.md).
    -   For more information on Google Chrome and Microsoft Edge connector methods, see [Chromium connector methods](../reference/connectors-chrome-methods.md).

    -   For more information on Windows connector methods, see [Windows Connector methods](../reference/connectors-windows-methods.md).
    -   If you have captured a web application screen and you want to execute a custom JavaScript on it, you can use the ExecuteJavascript method.


## Start method for Universal App Connector

You have a list of employee salary records in an Excel sheet, and you want your RPA robot to automatically calculate taxes using a public web-based tax calculator. Before the bot can interact with the calculator's UI, it needs to launch the browser and open the specific tax calculator page.

1.  Use the Data Table connector to import rows from the Excel file.
2.  Drag a For Each component onto the design surface to iterate over the list of employee salary records.
3.  Inside the loop:
    -   Extract fields from the current record.
    -   Set up the Universal App Connector to open the Chrome browser.
    -   Use the Start method to launch the browser and navigate to the tax calculator URL:

        `https://example.com/tax-calculator`

    -   Use WaitForAnyScreen or a Wait component to ensure the tax calculator interface is fully loaded and ready.
4.  Use other UAC methods or UI automation to:
    -   Enter salary and deduction values from the Excel row.
    -   Trigger the calculation.
    -   Capture the calculated tax amount.

**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

