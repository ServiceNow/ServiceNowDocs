---
title: Use the Start method for Universal App Connector
description: Use the Start method to launch a browser or an application for the Universal App Connector \(UAC\) object. You can use this method if you want a browser or application to start before interacting with any application screens or elements.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Universal app connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
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

Full navigation path of the application that you want to open. The path is entered in string format.For example, D:\\TestApps\\JavaTest.jar

</td><td>

No

</td></tr><tr><td>

StartParams

</td><td>

Arguments for the launch application. For example, if you select Google Chrome as the application and provide `google.com` as the argument, the Google web page is opened when the browser is launched.

</td><td>

No

</td></tr></tbody>
</table>
**Parent Topic:**[Universal app connector](../concept/universal-app-connector.md)

